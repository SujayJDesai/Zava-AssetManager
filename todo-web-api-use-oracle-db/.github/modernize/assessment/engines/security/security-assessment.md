# Security Assessment Report

**Generated:** 2026-08-17T09:08:18.0000000Z

## Summary

| Metric | Count |
|--------|-------|
| Total Findings | 35 |
| CVE Vulnerabilities | 33 |
| CWE Vulnerabilities | 2 |
| Total Rules Assessed | 59 |
| Rules Passed | 57 |

### By Severity

| Severity | Count |
|----------|-------|
| mandatory | 33 |
| optional | 2 |
| potential | 0 |

## CVE Findings (Dependency Vulnerabilities)

### GHSA-r7wm-3cxj-wff9: jackson-core: Async parser maxNumberLength bypass via chunked digit accumulation (incomplete fix for GHSA-72hv-8253-57qq)
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:21

[GHSA-r7wm-3cxj-wff9](https://github.com/advisories/GHSA-r7wm-3cxj-wff9): jackson-core: Async parser maxNumberLength bypass via chunked digit accumulation (incomplete fix for GHSA-72hv-8253-57qq)

Severity: HIGH

Affected dependencies:
  - com.fasterxml.jackson.core:jackson-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 2.18.8 or later
  - com.fasterxml.jackson.core:jackson-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 2.21.4 or later
  - tools.jackson.core:jackson-core
    Recommended: upgrade to 3.1.4 or later

### CVE-2026-54513: jackson-databind has an array subtype allowlist bypass in BasicPolymorphicTypeValidator (allowIfSubTypeIsArray)
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:21

[CVE-2026-54513](https://github.com/advisories/GHSA-rmj7-2vxq-3g9f): jackson-databind has an array subtype allowlist bypass in BasicPolymorphicTypeValidator (allowIfSubTypeIsArray)

Severity: HIGH

Affected dependencies:
  - com.fasterxml.jackson.core:jackson-databind (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 2.18.8 or later
  - com.fasterxml.jackson.core:jackson-databind (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 2.21.4 or later
  - com.fasterxml.jackson.core:jackson-databind (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 3.1.4 or later
  - tools.jackson.core:jackson-databind
    Recommended: upgrade to 3.1.4 or later

### CVE-2026-54512: jackson-databind has a PolymorphicTypeValidator bypass via generic type parameters that allows arbitrary class instantiation
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:21

[CVE-2026-54512](https://github.com/advisories/GHSA-j3rv-43j4-c7qm): jackson-databind has a PolymorphicTypeValidator bypass via generic type parameters that allows arbitrary class instantiation

Severity: HIGH

Affected dependencies:
  - com.fasterxml.jackson.core:jackson-databind (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 2.18.8 or later
  - com.fasterxml.jackson.core:jackson-databind (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 3.1.4 or later
  - com.fasterxml.jackson.core:jackson-databind (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 2.21.4 or later
  - tools.jackson.core:jackson-databind
    Recommended: upgrade to 3.1.4 or later

### CVE-2024-57699: Netplex Json-smart Uncontrolled Recursion vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:55

[CVE-2024-57699](https://github.com/advisories/GHSA-pq2g-wx69-c263): Netplex Json-smart Uncontrolled Recursion vulnerability

Severity: HIGH

Affected dependencies:
  - net.minidev:json-smart (transitive, pulled by org.springframework.boot:spring-boot-starter-test at todo-web-api-use-oracle-db/pom.xml:55)
    Recommended: upgrade to 2.5.2 or later

### CVE-2026-41284: Apache Tomcat: Unbounded read in WebDAV LOCK and  PROPFIND handling
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:21

[CVE-2026-41284](https://github.com/advisories/GHSA-gx5v-xp9w-j4cg): Apache Tomcat: Unbounded read in WebDAV LOCK and  PROPFIND handling

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 9.0.118 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 10.1.55 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 11.0.22 or later
  - org.apache.tomcat:tomcat
    Recommended: upgrade to 9.0.118 or later
  - org.apache.tomcat:tomcat
    Recommended: upgrade to 10.1.55 or later
  - org.apache.tomcat:tomcat
    Recommended: upgrade to 11.0.22 or later
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 9.0.118 or later
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 10.1.55 or later
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 11.0.22 or later

### CVE-2026-43512: Apache Tomcat - Digest authenticator will authenticate any unknown user
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:21

[CVE-2026-43512](https://github.com/advisories/GHSA-h6fc-48rj-7qqh): Apache Tomcat - Digest authenticator will authenticate any unknown user

Severity: CRITICAL

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 9.0.118 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 10.1.55 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 11.0.22 or later
  - org.apache.tomcat:tomcat
    Recommended: upgrade to 9.0.118 or later
  - org.apache.tomcat:tomcat
    Recommended: upgrade to 10.1.55 or later
  - org.apache.tomcat:tomcat
    Recommended: upgrade to 11.0.22 or later
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 9.0.118 or later
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 10.1.55 or later
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 11.0.22 or later

### CVE-2026-43513: Apache Tomcat: LockOutRealm treats user names as case-sensitive
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:21

[CVE-2026-43513](https://github.com/advisories/GHSA-5mp6-jrq3-r938): Apache Tomcat: LockOutRealm treats user names as case-sensitive

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 9.0.118 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 10.1.55 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 11.0.22 or later
  - org.apache.tomcat:tomcat
    Recommended: upgrade to 9.0.118 or later
  - org.apache.tomcat:tomcat
    Recommended: upgrade to 10.1.55 or later
  - org.apache.tomcat:tomcat
    Recommended: upgrade to 11.0.22 or later
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 9.0.118 or later
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 10.1.55 or later
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 11.0.22 or later

### CVE-2026-43515: Apache Tomcat - Security constraints not correctly applied
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:21

[CVE-2026-43515](https://github.com/advisories/GHSA-5m62-pw8w-7w9f): Apache Tomcat - Security constraints not correctly applied

Severity: CRITICAL

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 9.0.118 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 10.1.55 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 11.0.22 or later
  - org.apache.tomcat:tomcat
    Recommended: upgrade to 9.0.118 or later
  - org.apache.tomcat:tomcat
    Recommended: upgrade to 10.1.55 or later
  - org.apache.tomcat:tomcat
    Recommended: upgrade to 11.0.22 or later
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 9.0.118 or later
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 10.1.55 or later
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 11.0.22 or later

### CVE-2026-41293: Apache Tomcat - HTTP/2 request headers not validated
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:21

[CVE-2026-41293](https://github.com/advisories/GHSA-r29c-68gh-xp6x): Apache Tomcat - HTTP/2 request headers not validated

Severity: CRITICAL

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 9.0.118 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 10.1.55 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 11.0.22 or later
  - org.apache.tomcat:tomcat
    Recommended: upgrade to 9.0.118 or later
  - org.apache.tomcat:tomcat
    Recommended: upgrade to 10.1.55 or later
  - org.apache.tomcat:tomcat
    Recommended: upgrade to 11.0.22 or later
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 9.0.118 or later
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 10.1.55 or later
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 11.0.22 or later

### CVE-2026-42498: Apache Tomcat - WebSocket authentication header exposure
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:21

[CVE-2026-42498](https://github.com/advisories/GHSA-fv25-8xcx-gqjc): Apache Tomcat - WebSocket authentication header exposure

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 9.0.118 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 10.1.55 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 11.0.22 or later
  - org.apache.tomcat:tomcat
    Recommended: upgrade to 9.0.118 or later
  - org.apache.tomcat:tomcat
    Recommended: upgrade to 10.1.55 or later
  - org.apache.tomcat:tomcat
    Recommended: upgrade to 11.0.22 or later
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 9.0.118 or later
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 10.1.55 or later
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 11.0.22 or later

### CVE-2026-34483: Apache Tomcat has an Improper Encoding or Escaping of Output vulnerability in the JsonAccessLogValve
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:21

[CVE-2026-34483](https://github.com/advisories/GHSA-rv64-5gf8-9qq8): Apache Tomcat has an Improper Encoding or Escaping of Output vulnerability in the JsonAccessLogValve

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 9.0.116 or later
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 10.1.54 or later
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 11.0.21 or later
  - org.apache.tomcat:tomcat
    Recommended: upgrade to 9.0.116 or later
  - org.apache.tomcat:tomcat
    Recommended: upgrade to 10.1.54 or later
  - org.apache.tomcat:tomcat
    Recommended: upgrade to 11.0.21 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 9.0.116 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 10.1.54 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 11.0.21 or later

### CVE-2026-34487: Apache Tomcat vulnerable to Insertion of Sensitive Information into Log File
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:21

[CVE-2026-34487](https://github.com/advisories/GHSA-x4m4-345f-5h5g): Apache Tomcat vulnerable to Insertion of Sensitive Information into Log File

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat:tomcat
    Recommended: upgrade to 9.0.117 or later
  - org.apache.tomcat:tomcat
    Recommended: upgrade to 10.1.54 or later
  - org.apache.tomcat:tomcat
    Recommended: upgrade to 11.0.21 or later
  - org.apache.tomcat:tomcat-tribes
    Recommended: upgrade to 9.0.117 or later
  - org.apache.tomcat:tomcat-tribes
    Recommended: upgrade to 10.1.54 or later
  - org.apache.tomcat:tomcat-tribes
    Recommended: upgrade to 11.0.21 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 9.0.117 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 10.1.54 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 11.0.21 or later

### CVE-2026-24880: Apache Tomcat has an HTTP Request/Response Smuggling vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:21

[CVE-2026-24880](https://github.com/advisories/GHSA-563x-q5rq-57qp): Apache Tomcat has an HTTP Request/Response Smuggling vulnerability

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat:tomcat-coyote
    Recommended: upgrade to 9.0.116 or later
  - org.apache.tomcat:tomcat-coyote
    Recommended: upgrade to 10.1.52 or later
  - org.apache.tomcat:tomcat-coyote
    Recommended: upgrade to 11.0.20 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 9.0.116 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 10.1.52 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 11.0.20 or later

### CVE-2026-24734: Apache Tomcat has an Improper Input Validation vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:21

[CVE-2026-24734](https://github.com/advisories/GHSA-mgp5-rv84-w37q): Apache Tomcat has an Improper Input Validation vulnerability

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat:tomcat-coyote
    Recommended: upgrade to 11.0.18 or later
  - org.apache.tomcat:tomcat-coyote
    Recommended: upgrade to 10.1.52 or later
  - org.apache.tomcat:tomcat-coyote
    Recommended: upgrade to 9.0.115 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 11.0.18 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 10.1.52 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 9.0.115 or later

### CVE-2026-24400: AssertJ has XML External Entity (XXE) vulnerability when parsing untrusted XML via isXmlEqualTo assertion
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:55

[CVE-2026-24400](https://github.com/advisories/GHSA-rqfh-9r24-8c9r): AssertJ has XML External Entity (XXE) vulnerability when parsing untrusted XML via isXmlEqualTo assertion

Severity: HIGH

Affected dependencies:
  - org.assertj:assertj-core (transitive, pulled by org.springframework.boot:spring-boot-starter-test at todo-web-api-use-oracle-db/pom.xml:55)
    Recommended: upgrade to 3.27.7 or later

### CVE-2025-55752: Apache Tomcat Vulnerable to Relative Path Traversal
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:21

[CVE-2025-55752](https://github.com/advisories/GHSA-wmwf-9ccg-fff5): Apache Tomcat Vulnerable to Relative Path Traversal

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat:tomcat
    Recommended: upgrade to 11.0.11 or later
  - org.apache.tomcat:tomcat
    Recommended: upgrade to 10.1.45 or later
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 11.0.11 or later
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 10.1.45 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 11.0.11 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 10.1.45 or later
  - org.apache.tomcat:tomcat
    Recommended: upgrade to 9.0.109 or later
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 9.0.109 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 9.0.109 or later
  - org.apache.tomcat:tomcat
  - org.apache.tomcat:tomcat-catalina
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)

### CVE-2025-48989: Apache Tomcat Improper Resource Shutdown or Release vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:21

[CVE-2025-48989](https://github.com/advisories/GHSA-gqp3-2cvr-x8m3): Apache Tomcat Improper Resource Shutdown or Release vulnerability

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat:tomcat-coyote
    Recommended: upgrade to 11.0.10 or later
  - org.apache.tomcat:tomcat-coyote
    Recommended: upgrade to 10.1.44 or later
  - org.apache.tomcat:tomcat-coyote
    Recommended: upgrade to 9.0.108 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 11.0.10 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 10.1.44 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 9.0.108 or later

### CVE-2025-53506: Apache Tomcat Coyote vulnerable to Denial of Service via excessive HTTP/2 streams
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:21

[CVE-2025-53506](https://github.com/advisories/GHSA-25xr-qj8w-c4vf): Apache Tomcat Coyote vulnerable to Denial of Service via excessive HTTP/2 streams

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat:tomcat-coyote
    Recommended: upgrade to 11.0.9 or later
  - org.apache.tomcat:tomcat-coyote
    Recommended: upgrade to 10.1.43 or later
  - org.apache.tomcat:tomcat-coyote
    Recommended: upgrade to 9.0.107 or later
  - org.apache.tomcat:tomcat-coyote
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 9.0.107 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 10.1.43 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 11.0.9 or later

### CVE-2025-52520: Apache Tomcat Catalina is vulnerable to DoS attack through bypassing of size limits
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:21

[CVE-2025-52520](https://github.com/advisories/GHSA-wr62-c79q-cv37): Apache Tomcat Catalina is vulnerable to DoS attack through bypassing of size limits

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 11.0.9 or later
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 10.1.43 or later
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 9.0.107 or later
  - org.apache.tomcat:tomcat-catalina
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 11.0.9 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 10.1.43 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 9.0.107 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)

### CVE-2025-48988: Apache Tomcat - DoS in multipart upload
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:21

[CVE-2025-48988](https://github.com/advisories/GHSA-h3gc-qfqq-6h8f): Apache Tomcat - DoS in multipart upload

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 11.0.8 or later
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 10.1.42 or later
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 9.0.106 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 11.0.8 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 10.1.42 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 9.0.106 or later
  - org.apache.tomcat:tomcat-catalina
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)

### CVE-2025-24813: Apache Tomcat: Potential RCE and/or information disclosure and/or information corruption with partial PUT
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:21

[CVE-2025-24813](https://github.com/advisories/GHSA-83qj-6fr2-vhqg): Apache Tomcat: Potential RCE and/or information disclosure and/or information corruption with partial PUT

Severity: CRITICAL

Affected dependencies:
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 11.0.3 or later
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 10.1.35 or later
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 9.0.99 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 11.0.3 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 10.1.35 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 9.0.99 or later
  - org.apache.tomcat:tomcat-catalina
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)

### CVE-2024-56337: Apache Tomcat Time-of-check Time-of-use (TOCTOU) Race Condition vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:21

[CVE-2024-56337](https://github.com/advisories/GHSA-27hp-xhwr-wr2m): Apache Tomcat Time-of-check Time-of-use (TOCTOU) Race Condition vulnerability

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 11.0.2 or later
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 10.1.34 or later
  - org.apache.tomcat:tomcat-embed-core
    Recommended: upgrade to 9.0.98 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 11.0.2 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 10.1.34 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 9.0.98 or later

### CVE-2024-50379: Apache Tomcat Time-of-check Time-of-use (TOCTOU) Race Condition vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:21

[CVE-2024-50379](https://github.com/advisories/GHSA-5j33-cvvr-w245): Apache Tomcat Time-of-check Time-of-use (TOCTOU) Race Condition vulnerability

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 11.0.2 or later
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 10.1.34 or later
  - org.apache.tomcat:tomcat-catalina
    Recommended: upgrade to 9.0.98 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 11.0.2 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 10.1.34 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 9.0.98 or later
  - org.apache.tomcat:tomcat-catalina
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)

### CVE-2024-38286: Apache Tomcat Allocation of Resources Without Limits or Throttling vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:21

[CVE-2024-38286](https://github.com/advisories/GHSA-7jqf-v358-p8g7): Apache Tomcat Allocation of Resources Without Limits or Throttling vulnerability

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat:tomcat-coyote
    Recommended: upgrade to 11.0.0-M21 or later
  - org.apache.tomcat:tomcat-coyote
    Recommended: upgrade to 10.1.25 or later
  - org.apache.tomcat:tomcat-coyote
    Recommended: upgrade to 9.0.90 or later
  - org.apache.tomcat:tomcat-coyote
  - org.apache.tomcat:tomcat-coyote
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 11.0.0-M21 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 10.1.25 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 9.0.90 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)

### CVE-2024-34750: Apache Tomcat - Denial of Service
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:21

[CVE-2024-34750](https://github.com/advisories/GHSA-wm9w-rjj3-j356): Apache Tomcat - Denial of Service

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 11.0.0-M21 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 10.1.25 or later
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 9.0.90 or later
  - org.apache.tomcat:tomcat-coyote
    Recommended: upgrade to 11.0.0-M21 or later
  - org.apache.tomcat:tomcat-coyote
    Recommended: upgrade to 10.1.25 or later
  - org.apache.tomcat:tomcat-coyote
    Recommended: upgrade to 9.0.90 or later
  - org.apache.tomcat:tomcat-coyote
  - org.apache.tomcat.embed:tomcat-embed-core (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)

### CVE-2026-41850: Spring Framework Algorithmic Denial of Service via SpEL Expressions
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:21

[CVE-2026-41850](https://github.com/advisories/GHSA-r5w3-xv2f-j59q): Spring Framework Algorithmic Denial of Service via SpEL Expressions

Severity: HIGH

Affected dependencies:
  - org.springframework:spring-expression (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 7.0.8 or later
  - org.springframework:spring-expression (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 6.2.19 or later
  - org.springframework:spring-expression (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
  - org.springframework:spring-expression (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)

### CVE-2026-41845: Spring Framework Cross-site Scripting via JavaScriptUtils
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:21

[CVE-2026-41845](https://github.com/advisories/GHSA-3chg-m5w7-qfv5): Spring Framework Cross-site Scripting via JavaScriptUtils

Severity: HIGH

Affected dependencies:
  - org.springframework:spring-webmvc (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 7.0.8 or later
  - org.springframework:spring-webmvc (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 6.2.19 or later
  - org.springframework:spring-webmvc (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
  - org.springframework:spring-webmvc (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)

### CVE-2026-41842: Spring Framework Denial of Service via Versioned Resources in Spring MVC and WebFlux
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:21

[CVE-2026-41842](https://github.com/advisories/GHSA-x23c-287f-qqv5): Spring Framework Denial of Service via Versioned Resources in Spring MVC and WebFlux

Severity: HIGH

Affected dependencies:
  - org.springframework:spring-webmvc (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 7.0.8 or later
  - org.springframework:spring-webflux
    Recommended: upgrade to 7.0.8 or later
  - org.springframework:spring-webmvc (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 6.2.19 or later
  - org.springframework:spring-webflux
    Recommended: upgrade to 6.2.19 or later
  - org.springframework:spring-webmvc (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
  - org.springframework:spring-webflux
  - org.springframework:spring-webmvc (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
  - org.springframework:spring-webflux

### CVE-2025-41249: Spring Framework annotation detection mechanism may result in improper authorization
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:55

[CVE-2025-41249](https://github.com/advisories/GHSA-jmp9-x22r-554x): Spring Framework annotation detection mechanism may result in improper authorization

Severity: HIGH

Affected dependencies:
  - org.springframework:spring-core (transitive, pulled by org.springframework.boot:spring-boot-starter-test at todo-web-api-use-oracle-db/pom.xml:55)
  - org.springframework:spring-core (transitive, pulled by org.springframework.boot:spring-boot-starter-test at todo-web-api-use-oracle-db/pom.xml:55)
  - org.springframework:spring-core (transitive, pulled by org.springframework.boot:spring-boot-starter-test at todo-web-api-use-oracle-db/pom.xml:55)
    Recommended: upgrade to 6.2.11 or later

### CVE-2025-22235: Spring Boot EndpointRequest.to() creates wrong matcher if actuator endpoint is not exposed
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:48

[CVE-2025-22235](https://github.com/advisories/GHSA-rc42-6c7j-7h5r): Spring Boot EndpointRequest.to() creates wrong matcher if actuator endpoint is not exposed

Severity: HIGH

Affected dependencies:
  - org.springframework.boot:spring-boot (transitive, pulled by org.springframework.boot:spring-boot-devtools at todo-web-api-use-oracle-db/pom.xml:48)
  - org.springframework.boot:spring-boot (transitive, pulled by org.springframework.boot:spring-boot-devtools at todo-web-api-use-oracle-db/pom.xml:48)
  - org.springframework.boot:spring-boot (transitive, pulled by org.springframework.boot:spring-boot-devtools at todo-web-api-use-oracle-db/pom.xml:48)
  - org.springframework.boot:spring-boot (transitive, pulled by org.springframework.boot:spring-boot-devtools at todo-web-api-use-oracle-db/pom.xml:48)
    Recommended: upgrade to 3.3.11 or later
  - org.springframework.boot:spring-boot (transitive, pulled by org.springframework.boot:spring-boot-devtools at todo-web-api-use-oracle-db/pom.xml:48)
    Recommended: upgrade to 3.4.5 or later

### CVE-2024-38819: Spring Framework Path Traversal vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:21

[CVE-2024-38819](https://github.com/advisories/GHSA-g5vr-rgqm-vf78): Spring Framework Path Traversal vulnerability

Severity: HIGH

Affected dependencies:
  - org.springframework:spring-webflux
    Recommended: upgrade to 6.1.14 or later
  - org.springframework:spring-webmvc (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 6.1.14 or later
  - org.springframework:spring-webflux
  - org.springframework:spring-webmvc (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
  - org.springframework:spring-webflux
  - org.springframework:spring-webmvc (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)

### CVE-2024-38816: Path traversal vulnerability in functional web frameworks
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:21

[CVE-2024-38816](https://github.com/advisories/GHSA-cx7f-g6mp-7hqm): Path traversal vulnerability in functional web frameworks

Severity: HIGH

Affected dependencies:
  - org.springframework:spring-webmvc (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 6.1.13 or later
  - org.springframework:spring-webflux
    Recommended: upgrade to 6.1.13 or later
  - org.springframework:spring-webmvc (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
  - org.springframework:spring-webflux
  - org.springframework:spring-webmvc (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
  - org.springframework:spring-webflux

### CVE-2024-22262: Spring Framework URL Parsing with Host Validation
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** todo-web-api-use-oracle-db/pom.xml:21

[CVE-2024-22262](https://github.com/advisories/GHSA-2wrp-6fg6-hmc5): Spring Framework URL Parsing with Host Validation

Severity: HIGH

Affected dependencies:
  - org.springframework:spring-web (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 5.3.34 or later
  - org.springframework:spring-web (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 6.0.19 or later
  - org.springframework:spring-web (transitive, pulled by org.springframework.boot:spring-boot-starter-web at todo-web-api-use-oracle-db/pom.xml:21)
    Recommended: upgrade to 6.1.6 or later

## CWE Findings (Code-Level Vulnerabilities)

### CWE-259: Use of Hard-coded Password
- **Category:** Credentials & Secrets
- **Severity:** optional
- **Story Points:** 5
- **Files:** src/main/resources/application.yaml:4

The Spring Boot datasource configuration hard-codes the Oracle database password: `spring.datasource.password: oracle` (application.yaml, line 4), alongside the hard-coded username `system` (line 3). Storing database credentials directly in a committed configuration file exposes them to anyone with source access and prevents per-environment credential rotation.

### CWE-798: Use of Hard-coded Credentials
- **Category:** Credentials & Secrets
- **Severity:** optional
- **Story Points:** 5
- **Files:** src/main/resources/application.yaml:3, src/main/resources/application.yaml:4

The Oracle datasource username (`system`) and password (`oracle`) are hard-coded directly in `spring.datasource.username`/`spring.datasource.password` in application.yaml rather than being externalized via environment variables, a secrets manager, or a Spring profile-specific/encrypted configuration source.
