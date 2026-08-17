# assets-manager-parent

## Summary

| Metric | Value |
|--------|-------|
| Total Issues | 13 |
| Mandatory Blockers | 6 |
| Potential Issues | 3 |

## Component Information

| Property | Value |
|----------|-------|
| Language | Java |
| Frameworks | Spring Boot, Spring |
| Build tools | Maven |
| JDK version | 8 |

## Cloud Readiness Issues

| Issue Name | Criticality | Story Points | Occurrences |
|------------|-------------|--------------|-------------|
| AWS region configuration | Mandatory | 2 | [4](#AWS_region_configuration) |
| AWS S3 usage found | Mandatory | 8 | [2](#AWS_S3_usage_found) |
| Local JDBC Calls | Mandatory | 5 | [2](#Local_JDBC_Calls) |
| CRA: Hard-coded credentials in configuration files | Mandatory | 5 | [2](#CRA_Hard-coded_credentials_in_configuration_files) |
| CRA: Default or well-known password detected | Mandatory | 3 | [2](#CRA_Default_or_well-known_password_detected) |
| No Dockerfile found | Mandatory | 3 | 1 |
| Password found in configuration file | Potential | 3 | [4](#Password_found_in_configuration_file) |
| PostgreSQL database found | Potential | 5 | [3](#PostgreSQL_database_found) |
| Restricted configurations found | Potential | 2 | [2](#Restricted_configurations_found) |
| RabbitMQ connection string, username or password found in configuration file | Optional | 5 | [6](#RabbitMQ_connection_string_username_or_password_found_in_configuration_file) |
| Spring AMQP dependency found | Optional | 5 | [3](#Spring_AMQP_dependency_found) |
| Localhost Usage | Optional | 3 | [2](#Localhost_Usage) |

### Issue Details

<details id="AWS_region_configuration">
<summary><b>AWS region configuration</b> — affected files</summary>

- `web/src/main/java/com/microsoft/migration/assets/config/AwsS3Config.java (line 20)`
- `web/src/main/resources/application.properties (line 6)`
- `worker/src/main/java/com/microsoft/migration/assets/worker/config/AwsS3Config.java (line 19)`
- `worker/src/main/resources/application.properties (line 4)`

</details>

<details id="AWS_S3_usage_found">
<summary><b>AWS S3 usage found</b> — affected files</summary>

- `worker/src/main/resources/application.properties (line 5)`
- `web/src/main/resources/application.properties (line 7)`

</details>

<details id="Local_JDBC_Calls">
<summary><b>Local JDBC Calls</b> — affected files</summary>

- `web/src/main/resources/application.properties (line 20)`
- `worker/src/main/resources/application.properties (line 17)`

</details>

<details id="CRA_Hard-coded_credentials_in_configuration_files">
<summary><b>CRA: Hard-coded credentials in configuration files</b> — affected files</summary>

- `worker/src/main/resources/application.properties (line 3)`
- `web/src/main/resources/application.properties (line 5)`

</details>

<details id="CRA_Default_or_well-known_password_detected">
<summary><b>CRA: Default or well-known password detected</b> — affected files</summary>

- `web/src/main/resources/application.properties (line 17)`
- `worker/src/main/resources/application.properties (line 14)`

</details>

<details id="Password_found_in_configuration_file">
<summary><b>Password found in configuration file</b> — affected files</summary>

- `worker/src/main/resources/application.properties (line 14)`
- `worker/src/main/resources/application.properties (line 19)`
- `web/src/main/resources/application.properties (line 17)`
- `web/src/main/resources/application.properties (line 22)`

</details>

<details id="PostgreSQL_database_found">
<summary><b>PostgreSQL database found</b> — affected files</summary>

- `web/src/main/resources/application.properties (line 20)`
- `worker/src/main/resources/application.properties (line 17)`

</details>

<details id="Restricted_configurations_found">
<summary><b>Restricted configurations found</b> — affected files</summary>

- `worker/src/main/resources/application.properties (line 8)`
- `web/src/main/resources/application.properties (line 1)`

</details>

<details id="RabbitMQ_connection_string_username_or_password_found_in_configuration_file">
<summary><b>RabbitMQ connection string, username or password found in configuration file</b> — affected files</summary>

- `worker/src/main/resources/application.properties (line 11)`
- `worker/src/main/resources/application.properties (line 13)`
- `worker/src/main/resources/application.properties (line 14)`
- `web/src/main/resources/application.properties (line 14)`
- `web/src/main/resources/application.properties (line 16)`
- `web/src/main/resources/application.properties (line 17)`

</details>

<details id="Spring_AMQP_dependency_found">
<summary><b>Spring AMQP dependency found</b> — affected files</summary>

- `worker/pom.xml (line 27)`
- `web/pom.xml (line 31)`

</details>

<details id="Localhost_Usage">
<summary><b>Localhost Usage</b> — affected files</summary>

- `web/src/main/resources/application.properties (line 14)`
- `worker/src/main/resources/application.properties (line 11)`

</details>

## Upgrade Issues

| Issue Name | Criticality | Story Points | Occurrences |
|------------|-------------|--------------|-------------|
| Java Version is not the latest LTS | Optional | 8 | [1](#Java_Version_is_not_the_latest_LTS) |

### Issue Details

<details id="Java_Version_is_not_the_latest_LTS">
<summary><b>Java Version is not the latest LTS</b> — affected files</summary>

- `pom.xml (line 19)`

</details>

---

## Codebase Insights

> **Note:** These documents are generated by AI and may contain inaccuracies or incomplete information. Please review carefully.

> **Codebase Insights aren't available yet.**
>
> These documents are generated when assessment runs with **Full analysis** coverage. Re-run the assessment and set `analysisCoverage: full` to enable them.

[Share feedback](https://aka.ms/ghcp-appmod/feedback)
