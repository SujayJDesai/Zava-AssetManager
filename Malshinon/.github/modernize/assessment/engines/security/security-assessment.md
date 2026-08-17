# Security Assessment Report

**Generated:** 2026-08-17T09:06:26.0000000Z

## Summary

| Metric | Count |
|--------|-------|
| Total Findings | 7 |
| CVE Vulnerabilities | 0 |
| CWE Vulnerabilities | 7 |
| Total Rules Assessed | 59 |
| Rules Passed | 52 |

### By Severity

| Severity | Count |
|----------|-------|
| mandatory | 1 |
| optional | 4 |
| potential | 2 |

## CVE Findings (Dependency Vulnerabilities)

_No CVE findings met the minimum severity threshold (high)._

## CWE Findings (Code-Level Vulnerabilities)

### CWE-772: Missing Release of Resource after Effective Lifetime
- **Category:** Code Quality
- **Severity:** potential
- **Story Points:** 3
- **Files:** CSV.cs:25-76

In CSV.ImportCsv() (CSV.cs, line 25), a `StreamReader` is created with `new StreamReader(path)` but is never wrapped in a `using` statement or explicitly disposed/closed. If the CSV header is null (line 27-31) the method returns immediately, leaking the open file handle; even in the normal path the reader is never closed after the read loop completes.

### CWE-775: Missing Release of File Descriptor or Handle after Effective Lifetime
- **Category:** Code Quality
- **Severity:** potential
- **Story Points:** 3
- **Files:** CSV.cs:25-76

The same `StreamReader` instance created in CSV.ImportCsv() (CSV.cs, line 25) holds an open file handle on the imported CSV file for the lifetime of the method, but the handle is never released via `Dispose()`/`Close()` or a `using` block, including on the early-return path when the header is empty (lines 27-31).

### CWE-798: Use of Hard-coded Credentials
- **Category:** Credentials & Secrets
- **Severity:** optional
- **Story Points:** 5
- **Files:** DBConnection.cs:13

DBConnection.Connect() (DBConnection.cs, line 13) contains a hard-coded default MySQL connection string `"server=127.0.0.1;uid=root;password=;database=malshinon"` that specifies the database credential (uid=root) directly in source code and is used whenever no connection string is supplied by the caller.

### CWE-22: Improper Limitation of a Pathname to a Restricted Directory ('Path Traversal')
- **Category:** File & Path Security
- **Severity:** optional
- **Story Points:** 8
- **Files:** CSV.cs:14-25

In CSV.ImportCsv() (CSV.cs, lines 14-25), the file path is read directly from user console input via Console.ReadLine() with only a Trim() applied, then passed unchecked to File.Exists() and new StreamReader(path). There is no validation that the resolved path stays within an expected/restricted directory, allowing arbitrary file paths (including those using '..' segments or absolute paths) to be opened and read.

### CWE-23: Relative Path Traversal
- **Category:** File & Path Security
- **Severity:** optional
- **Story Points:** 5
- **Files:** CSV.cs:14-25

The same path read from Console.ReadLine() in CSV.ImportCsv() (CSV.cs, lines 14-25) is not sanitized for relative traversal sequences such as '..', so a user-supplied value like '../../secret.csv' would be accepted and opened via File.Exists()/StreamReader without restriction to a base directory.

### CWE-36: Absolute Path Traversal
- **Category:** File & Path Security
- **Severity:** optional
- **Story Points:** 5
- **Files:** CSV.cs:14-25

CSV.ImportCsv() (CSV.cs, lines 14-25) accepts the raw string entered by the user as a file path with no check that it is a relative path confined to a restricted directory. An absolute path (e.g. 'C:\Windows\win.ini' or '/etc/passwd') supplied at the prompt would be passed directly to File.Exists() and StreamReader without restriction.

### CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **Category:** Injection Attacks
- **Severity:** mandatory
- **Story Points:** 13
- **Files:** DAL/PeopleDAL.cs:36-46, DAL/ReportDAL.cs:47-57

PeopleDAL.InsertNewPeople() (DAL/PeopleDAL.cs, lines 36-37) and PeopleDAL.GetIdBySecretCode() (DAL/PeopleDAL.cs, lines 45-46) build SQL statements via raw string interpolation of user-supplied values (fullName, secretCode read from Console.ReadLine or CSV import) directly into the query text, e.g. `$"INSERT INTO peoples (FullName, SecretCode, IsAgent, IsDangerous) VALUES('{newPeople.GetFullName()}', '{newPeople.GetSecretCode()}', ...)"` and `$@"SELECT id FROM peoples WHERE secretCode = '{secretCode}';"`, which are then passed unparameterized to DBConnection.Execute(). Similarly, ReportDAL.InsertReport() (DAL/ReportDAL.cs, lines 47-56) interpolates reportText and other fields directly into the INSERT statement. None of these use parameterized queries, so a malicious value (e.g. containing a single quote or SQL keywords) can alter the query structure.
