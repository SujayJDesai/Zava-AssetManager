# Security Assessment Report

**Generated:** 2026-08-17T09:10:34.0000000Z

## Summary

| Metric | Count |
|--------|-------|
| Total Findings | 3 |
| CVE Vulnerabilities | 1 |
| CWE Vulnerabilities | 2 |
| Total Rules Assessed | 59 |
| Rules Passed | 57 |

### By Severity

| Severity | Count |
|----------|-------|
| mandatory | 1 |
| optional | 1 |
| potential | 1 |

## CVE Findings (Dependency Vulnerabilities)

### CVE-2024-0056: Microsoft.Data.SqlClient and System.Data.SqlClient vulnerable to SQL Data Provider Security Feature Bypass
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** packages.config:14

[CVE-2024-0056](https://github.com/advisories/GHSA-98g6-xh36-x2p7): Microsoft.Data.SqlClient and System.Data.SqlClient vulnerable to SQL Data Provider Security Feature Bypass

Severity: HIGH

Affected dependencies:
  - Microsoft.Data.SqlClient:2.1.4 (declared at packages.config:14), vulnerable range: < 2.1.7

Recommended fix:
  - Upgrade Microsoft.Data.SqlClient to 2.1.7 or later (or to a version >= 5.1.3 for the latest major line)

## CWE Findings (Code-Level Vulnerabilities)

### CWE-732: Incorrect Permission Assignment for Critical Resource
- **Category:** Credentials & Secrets
- **Severity:** optional
- **Story Points:** 5
- **Files:** Services/NotificationService.cs:23

In `NotificationService` constructor, when the MSMQ notification queue is created, `_queue.SetPermissions("Everyone", MessageQueueAccessRights.FullControl)` grants the built-in 'Everyone' group full control (read, write, and manage) over the message queue. This allows any local user or process to read, send, or delete notification messages, which is an overly permissive assignment for a security-critical resource.

### CWE-778: Insufficient Logging
- **Category:** Credentials & Secrets
- **Severity:** potential
- **Story Points:** 3
- **Files:** Controllers/NotificationsController.cs:32, Controllers/NotificationsController.cs:54, Controllers/BaseController.cs:34, Controllers/CoursesController.cs:240, Services/NotificationService.cs:66, Services/NotificationService.cs:85

Exceptions in notification handling and file operations (e.g. `NotificationsController.GetNotifications`, `NotificationService.SendNotification`/`ReceiveNotification`, and `CoursesController.DeleteConfirmed`) are caught and only written via `System.Diagnostics.Debug.WriteLine`, which is compiled out / not captured in Release builds and is not persisted to any durable log store. Failures of these operations (including file deletion and message queue send/receive failures) are therefore effectively unlogged in production, providing no audit trail for these events.
