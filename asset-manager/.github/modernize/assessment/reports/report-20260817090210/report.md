# assets-manager-parent

## Summary

| Metric | Value |
|--------|-------|
| Total Issues | 86 |
| Mandatory Blockers | 71 |
| Potential Issues | 5 |

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
| CRA: Hard-coded credentials in configuration files | Mandatory | 5 | [2](#CRA_Hard-coded_credentials_in_configuration_files) |
| CRA: Default or well-known password detected | Mandatory | 3 | [2](#CRA_Default_or_well-known_password_detected) |
| Local JDBC Calls | Mandatory | 5 | [2](#Local_JDBC_Calls) |
| No Dockerfile found | Mandatory | 3 | 1 |
| Password found in configuration file | Potential | 3 | [4](#Password_found_in_configuration_file) |
| PostgreSQL database found | Potential | 5 | [3](#PostgreSQL_database_found) |
| Restricted configurations found | Potential | 2 | [2](#Restricted_configurations_found) |
| Detects usage of Jakarta Persistence (JPA) APIs | Potential | 5 | [2](#Detects_usage_of_Jakarta_Persistence_JPA_APIs) |
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

<details id="Local_JDBC_Calls">
<summary><b>Local JDBC Calls</b> — affected files</summary>

- `web/src/main/resources/application.properties (line 20)`
- `worker/src/main/resources/application.properties (line 17)`

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

- `worker/src/main/resources/application.properties (line 17)`
- `web/src/main/resources/application.properties (line 20)`

</details>

<details id="Restricted_configurations_found">
<summary><b>Restricted configurations found</b> — affected files</summary>

- `worker/src/main/resources/application.properties (line 8)`
- `web/src/main/resources/application.properties (line 1)`

</details>

<details id="Detects_usage_of_Jakarta_Persistence_JPA_APIs">
<summary><b>Detects usage of Jakarta Persistence (JPA) APIs</b> — affected files</summary>

- `worker/pom.xml (line 49)`
- `web/pom.xml (line 60)`

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

- `worker/src/main/resources/application.properties (line 11)`
- `web/src/main/resources/application.properties (line 14)`

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

## Security Issues

> **Note:** These issues were generated by AI and may contain inaccuracies or incomplete information. Please review carefully.

| Issue Name | Criticality | Story Points | Files |
|------------|-------------|--------------|-------|
| CWE-434: Unrestricted Upload of File with Dangerous Type | Mandatory | 8 | [4](#CWE-434_Unrestricted_Upload_of_File_with_Dangerous_Type) |
| CVE-2026-56819: Netty: HTTP/2 decompression leaks ByteBuf reference count when the decompressor channel is already closed (Direct memory leak / OOM DoS) | Mandatory | 1 | [2](#CVE-2026-56819_Netty_HTTP_2_decompression_leaks_ByteBuf_reference_count_when_the_decompressor_channel_is_already_closed_Direct_memory_leak_OOM_DoS) |
| CVE-2026-59901: Netty: [Bzip2Decoder] Infinite Loop in RLE State Machine Leads to Event-Loop Thread Hang | Mandatory | 1 | [2](#CVE-2026-59901_Netty_Bzip2Decoder_Infinite_Loop_in_RLE_State_Machine_Leads_to_Event-Loop_Thread_Hang) |
| CVE-2026-56745: Netty: [SpdyHttpDecoder] ByteBuf Reference Leak on RST_STREAM Leads to Native Memory Exhaustion | Mandatory | 1 | [2](#CVE-2026-56745_Netty_SpdyHttpDecoder_ByteBuf_Reference_Leak_on_RST_STREAM_Leads_to_Native_Memory_Exhaustion) |
| CVE-2026-55833: Netty SPDY zlib header block continues decoded expansion after maxHeaderSize truncation | Mandatory | 1 | [2](#CVE-2026-55833_Netty_SPDY_zlib_header_block_continues_decoded_expansion_after_maxHeaderSize_truncation) |
| CVE-2026-55831: Netty SPDY SETTINGS frame count materializes unbounded settings map | Mandatory | 1 | [2](#CVE-2026-55831_Netty_SPDY_SETTINGS_frame_count_materializes_unbounded_settings_map) |
| GHSA-r7wm-3cxj-wff9: jackson-core: Async parser maxNumberLength bypass via chunked digit accumulation (incomplete fix for GHSA-72hv-8253-57qq) | Mandatory | 1 | [2](#GHSA-r7wm-3cxj-wff9_jackson-core_Async_parser_maxNumberLength_bypass_via_chunked_digit_accumulation_incomplete_fix_for_GHSA-72hv-8253-57qq) |
| CVE-2026-54513: jackson-databind has an array subtype allowlist bypass in BasicPolymorphicTypeValidator (allowIfSubTypeIsArray) | Mandatory | 1 | [2](#CVE-2026-54513_jackson-databind_has_an_array_subtype_allowlist_bypass_in_BasicPolymorphicTypeValidator_allowIfSubTypeIsArray) |
| CVE-2026-54512: jackson-databind has a PolymorphicTypeValidator bypass via generic type parameters that allows arbitrary class instantiation | Mandatory | 1 | [2](#CVE-2026-54512_jackson-databind_has_a_PolymorphicTypeValidator_bypass_via_generic_type_parameters_that_allows_arbitrary_class_instantiation) |
| CVE-2026-50010: Netty: Wrapping plain trust manager silently disables hostname verification | Mandatory | 1 | [2](#CVE-2026-50010_Netty_Wrapping_plain_trust_manager_silently_disables_hostname_verification) |
| CVE-2026-45416: Netty: SNI handler pre-allocates up to 16 MiB from nine attacker bytes | Mandatory | 1 | [2](#CVE-2026-45416_Netty_SNI_handler_pre-allocates_up_to_16_MiB_from_nine_attacker_bytes) |
| CVE-2026-44249: Netty has an IPv6 Subnet Filter Bypass via Incorrect Comparator Masking | Mandatory | 1 | [2](#CVE-2026-44249_Netty_has_an_IPv6_Subnet_Filter_Bypass_via_Incorrect_Comparator_Masking) |
| CVE-2026-42587: Netty: HttpContentDecompressor maxAllocation bypass when Content-Encoding set to br/zstd/snappy leads to decompression bomb DoS | Mandatory | 1 | [2](#CVE-2026-42587_Netty_HttpContentDecompressor_maxAllocation_bypass_when_Content-Encoding_set_to_br_zstd_snappy_leads_to_decompression_bomb_DoS) |
| CVE-2026-42584: Netty has HttpClientCodec response desynchronization | Mandatory | 1 | [2](#CVE-2026-42584_Netty_has_HttpClientCodec_response_desynchronization) |
| CVE-2026-42583: Netty Lz4FrameDecoder is vulnerable to resource exhaustion  | Mandatory | 1 | [2](#CVE-2026-42583_Netty_Lz4FrameDecoder_is_vulnerable_to_resource_exhaustion) |
| CVE-2026-33871: Netty HTTP/2 CONTINUATION Frame Flood DoS via Zero-Byte Frame Bypass | Mandatory | 1 | [2](#CVE-2026-33871_Netty_HTTP_2_CONTINUATION_Frame_Flood_DoS_via_Zero-Byte_Frame_Bypass) |
| CVE-2026-33870: Netty: HTTP Request Smuggling via Chunked Extension Quoted-String Parsing | Mandatory | 1 | [2](#CVE-2026-33870_Netty_HTTP_Request_Smuggling_via_Chunked_Extension_Quoted-String_Parsing) |
| CVE-2025-55163: Netty affected by MadeYouReset HTTP/2 DDoS vulnerability | Mandatory | 1 | [2](#CVE-2025-55163_Netty_affected_by_MadeYouReset_HTTP_2_DDoS_vulnerability) |
| CVE-2025-52999: jackson-core can throw a StackoverflowError when processing deeply nested data | Mandatory | 1 | [2](#CVE-2025-52999_jackson-core_can_throw_a_StackoverflowError_when_processing_deeply_nested_data) |
| CVE-2025-24970: SslHandler doesn't correctly validate packets which can lead to native crash when using native SSLEngine | Mandatory | 1 | [2](#CVE-2025-24970_SslHandler_doesn_t_correctly_validate_packets_which_can_lead_to_native_crash_when_using_native_SSLEngine) |
| CVE-2023-6481: Logback is vulnerable to an attacker mounting a Denial-Of-Service attack by sending poisoned data | Mandatory | 1 | [2](#CVE-2023-6481_Logback_is_vulnerable_to_an_attacker_mounting_a_Denial-Of-Service_attack_by_sending_poisoned_data) |
| CVE-2023-6378: logback serialization vulnerability | Mandatory | 1 | [2](#CVE-2023-6378_logback_serialization_vulnerability) |
| CVE-2026-41284: Apache Tomcat: Unbounded read in WebDAV LOCK and  PROPFIND handling | Mandatory | 1 | [1](#CVE-2026-41284_Apache_Tomcat_Unbounded_read_in_WebDAV_LOCK_and_PROPFIND_handling) |
| CVE-2026-43512: Apache Tomcat - Digest authenticator will authenticate any unknown user | Mandatory | 1 | [1](#CVE-2026-43512_Apache_Tomcat_-_Digest_authenticator_will_authenticate_any_unknown_user) |
| CVE-2026-43513: Apache Tomcat: LockOutRealm treats user names as case-sensitive | Mandatory | 1 | [1](#CVE-2026-43513_Apache_Tomcat_LockOutRealm_treats_user_names_as_case-sensitive) |
| CVE-2026-43515: Apache Tomcat - Security constraints not correctly applied | Mandatory | 1 | [1](#CVE-2026-43515_Apache_Tomcat_-_Security_constraints_not_correctly_applied) |
| CVE-2026-41293: Apache Tomcat - HTTP/2 request headers not validated | Mandatory | 1 | [1](#CVE-2026-41293_Apache_Tomcat_-_HTTP_2_request_headers_not_validated) |
| CVE-2026-42498: Apache Tomcat - WebSocket authentication header exposure | Mandatory | 1 | [1](#CVE-2026-42498_Apache_Tomcat_-_WebSocket_authentication_header_exposure) |
| CVE-2026-34483: Apache Tomcat has an Improper Encoding or Escaping of Output vulnerability in the JsonAccessLogValve | Mandatory | 1 | [1](#CVE-2026-34483_Apache_Tomcat_has_an_Improper_Encoding_or_Escaping_of_Output_vulnerability_in_the_JsonAccessLogValve) |
| CVE-2026-34487: Apache Tomcat vulnerable to Insertion of Sensitive Information into Log File | Mandatory | 1 | [1](#CVE-2026-34487_Apache_Tomcat_vulnerable_to_Insertion_of_Sensitive_Information_into_Log_File) |
| CVE-2026-24880: Apache Tomcat has an HTTP Request/Response Smuggling vulnerability | Mandatory | 1 | [1](#CVE-2026-24880_Apache_Tomcat_has_an_HTTP_Request_Response_Smuggling_vulnerability) |
| CVE-2026-24734: Apache Tomcat has an Improper Input Validation vulnerability | Mandatory | 1 | [1](#CVE-2026-24734_Apache_Tomcat_has_an_Improper_Input_Validation_vulnerability) |
| CVE-2026-24400: AssertJ has XML External Entity (XXE) vulnerability when parsing untrusted XML via isXmlEqualTo assertion | Mandatory | 1 | [2](#CVE-2026-24400_AssertJ_has_XML_External_Entity_XXE_vulnerability_when_parsing_untrusted_XML_via_isXmlEqualTo_assertion) |
| CVE-2025-55752: Apache Tomcat Vulnerable to Relative Path Traversal | Mandatory | 1 | [1](#CVE-2025-55752_Apache_Tomcat_Vulnerable_to_Relative_Path_Traversal) |
| CVE-2025-48989: Apache Tomcat Improper Resource Shutdown or Release vulnerability | Mandatory | 1 | [1](#CVE-2025-48989_Apache_Tomcat_Improper_Resource_Shutdown_or_Release_vulnerability) |
| CVE-2025-53506: Apache Tomcat Coyote vulnerable to Denial of Service via excessive HTTP/2 streams | Mandatory | 1 | [1](#CVE-2025-53506_Apache_Tomcat_Coyote_vulnerable_to_Denial_of_Service_via_excessive_HTTP_2_streams) |
| CVE-2025-52520: Apache Tomcat Catalina is vulnerable to DoS attack through bypassing of size limits | Mandatory | 1 | [1](#CVE-2025-52520_Apache_Tomcat_Catalina_is_vulnerable_to_DoS_attack_through_bypassing_of_size_limits) |
| CVE-2025-48988: Apache Tomcat - DoS in multipart upload | Mandatory | 1 | [1](#CVE-2025-48988_Apache_Tomcat_-_DoS_in_multipart_upload) |
| CVE-2025-24813: Apache Tomcat: Potential RCE and/or information disclosure and/or information corruption with partial PUT | Mandatory | 1 | [1](#CVE-2025-24813_Apache_Tomcat_Potential_RCE_and_or_information_disclosure_and_or_information_corruption_with_partial_PUT) |
| CVE-2024-56337: Apache Tomcat Time-of-check Time-of-use (TOCTOU) Race Condition vulnerability | Mandatory | 1 | [1](#CVE-2024-56337_Apache_Tomcat_Time-of-check_Time-of-use_TOCTOU_Race_Condition_vulnerability) |
| CVE-2024-50379: Apache Tomcat Time-of-check Time-of-use (TOCTOU) Race Condition vulnerability | Mandatory | 1 | [1](#CVE-2024-50379_Apache_Tomcat_Time-of-check_Time-of-use_TOCTOU_Race_Condition_vulnerability) |
| CVE-2024-38286: Apache Tomcat Allocation of Resources Without Limits or Throttling vulnerability | Mandatory | 1 | [1](#CVE-2024-38286_Apache_Tomcat_Allocation_of_Resources_Without_Limits_or_Throttling_vulnerability) |
| CVE-2024-34750: Apache Tomcat - Denial of Service | Mandatory | 1 | [1](#CVE-2024-34750_Apache_Tomcat_-_Denial_of_Service) |
| CVE-2026-41850: Spring Framework Algorithmic Denial of Service via SpEL Expressions | Mandatory | 1 | [2](#CVE-2026-41850_Spring_Framework_Algorithmic_Denial_of_Service_via_SpEL_Expressions) |
| CVE-2026-41849: Spring Framework Denial of Service via Integer Overflow in SpEL Expressions | Mandatory | 1 | [2](#CVE-2026-41849_Spring_Framework_Denial_of_Service_via_Integer_Overflow_in_SpEL_Expressions) |
| CVE-2026-41845: Spring Framework Cross-site Scripting via JavaScriptUtils | Mandatory | 1 | [1](#CVE-2026-41845_Spring_Framework_Cross-site_Scripting_via_JavaScriptUtils) |
| CVE-2026-41842: Spring Framework Denial of Service via Versioned Resources in Spring MVC and WebFlux | Mandatory | 1 | [1](#CVE-2026-41842_Spring_Framework_Denial_of_Service_via_Versioned_Resources_in_Spring_MVC_and_WebFlux) |
| CVE-2026-42198: pgjdbc: Unbounded PBKDF2 iterations in SCRAM authentication allows CPU exhaustion DoS | Mandatory | 1 | [2](#CVE-2026-42198_pgjdbc_Unbounded_PBKDF2_iterations_in_SCRAM_authentication_allows_CPU_exhaustion_DoS) |
| CVE-2026-40973: Spring Boot accepts predictable temp directory without ownership verification | Mandatory | 1 | [2](#CVE-2026-40973_Spring_Boot_accepts_predictable_temp_directory_without_ownership_verification) |
| CVE-2025-41249: Spring Framework annotation detection mechanism may result in improper authorization | Mandatory | 1 | [2](#CVE-2025-41249_Spring_Framework_annotation_detection_mechanism_may_result_in_improper_authorization) |
| CVE-2025-22235: Spring Boot EndpointRequest.to() creates wrong matcher if actuator endpoint is not exposed | Mandatory | 1 | [2](#CVE-2025-22235_Spring_Boot_EndpointRequest_to_creates_wrong_matcher_if_actuator_endpoint_is_not_exposed) |
| CVE-2024-38819: Spring Framework Path Traversal vulnerability | Mandatory | 1 | [1](#CVE-2024-38819_Spring_Framework_Path_Traversal_vulnerability) |
| CVE-2024-38816: Path traversal vulnerability in functional web frameworks | Mandatory | 1 | [1](#CVE-2024-38816_Path_traversal_vulnerability_in_functional_web_frameworks) |
| CVE-2024-22262: Spring Framework URL Parsing with Host Validation | Mandatory | 1 | [1](#CVE-2024-22262_Spring_Framework_URL_Parsing_with_Host_Validation) |
| CVE-2024-22259: Spring Framework URL Parsing with Host Validation Vulnerability | Mandatory | 1 | [1](#CVE-2024-22259_Spring_Framework_URL_Parsing_with_Host_Validation_Vulnerability) |
| CVE-2024-22243: Spring Web vulnerable to Open Redirect or Server Side Request Forgery | Mandatory | 1 | [1](#CVE-2024-22243_Spring_Web_vulnerable_to_Open_Redirect_or_Server_Side_Request_Forgery) |
| CVE-2024-1597: org.postgresql:postgresql vulnerable to SQL Injection via line comment generation | Mandatory | 1 | [2](#CVE-2024-1597_org_postgresql_postgresql_vulnerable_to_SQL_Injection_via_line_comment_generation) |
| CVE-2016-1000027: Pivotal Spring Framework contains unsafe Java deserialization methods | Mandatory | 1 | [1](#CVE-2016-1000027_Pivotal_Spring_Framework_contains_unsafe_Java_deserialization_methods) |
| CVE-2026-41716: Spring Data Commons: Heap exhaustion from unbounded property-lookup cache retaining crafted string keys | Mandatory | 1 | [2](#CVE-2026-41716_Spring_Data_Commons_Heap_exhaustion_from_unbounded_property-lookup_cache_retaining_crafted_string_keys) |
| CVE-2026-41901: Sandboxed Thymeleaf expressions vulnerable to improper recognition of unauthorized syntax patterns | Mandatory | 1 | [1](#CVE-2026-41901_Sandboxed_Thymeleaf_expressions_vulnerable_to_improper_recognition_of_unauthorized_syntax_patterns) |
| CVE-2026-40972: Spring Boot DevTools remote secret comparison is vulnerable to timing attacks | Mandatory | 1 | [1](#CVE-2026-40972_Spring_Boot_DevTools_remote_secret_comparison_is_vulnerable_to_timing_attacks) |
| CVE-2026-40478: Improper neutralization of specific syntax patterns for unauthorized expressions in Thymeleaf | Mandatory | 1 | [1](#CVE-2026-40478_Improper_neutralization_of_specific_syntax_patterns_for_unauthorized_expressions_in_Thymeleaf) |
| CVE-2026-40477: Improper restriction of the scope of accessible objects in Thymeleaf expressions | Mandatory | 1 | [1](#CVE-2026-40477_Improper_restriction_of_the_scope_of_accessible_objects_in_Thymeleaf_expressions) |
| CVE-2022-1471: SnakeYaml Constructor Deserialization Remote Code Execution | Mandatory | 1 | [2](#CVE-2022-1471_SnakeYaml_Constructor_Deserialization_Remote_Code_Execution) |
| CVE-2022-25857: Uncontrolled Resource Consumption in snakeyaml | Mandatory | 1 | [2](#CVE-2022-25857_Uncontrolled_Resource_Consumption_in_snakeyaml) |
| CWE-99: Improper Control of Resource Identifiers ('Resource Injection') | Potential | 3 | [3](#CWE-99_Improper_Control_of_Resource_Identifiers_Resource_Injection) |
| CWE-22: Improper Limitation of a Pathname to a Restricted Directory ('Path Traversal') | Optional | 8 | [2](#CWE-22_Improper_Limitation_of_a_Pathname_to_a_Restricted_Directory_Path_Traversal) |
| CWE-259: Use of Hard-coded Password | Optional | 5 | [2](#CWE-259_Use_of_Hard-coded_Password) |
| CWE-798: Use of Hard-coded Credentials | Optional | 5 | [4](#CWE-798_Use_of_Hard-coded_Credentials) |
| CWE-23: Relative Path Traversal | Optional | 5 | [3](#CWE-23_Relative_Path_Traversal) |
| CWE-36: Absolute Path Traversal | Optional | 5 | [2](#CWE-36_Absolute_Path_Traversal) |
| CWE-477: Use of Obsolete Function | Optional | 1 | [1](#CWE-477_Use_of_Obsolete_Function) |

### Security Issue Details

<details id="CWE-434_Unrestricted_Upload_of_File_with_Dangerous_Type">
<summary><b>CWE-434: Unrestricted Upload of File with Dangerous Type</b> — affected files</summary>

- `asset-manager/web/src/main/java/com/microsoft/migration/assets/controller/S3Controller.java`
- `asset-manager/web/src/main/java/com/microsoft/migration/assets/service/LocalFileStorageService.java`
- `asset-manager/web/src/main/java/com/microsoft/migration/assets/service/AwsS3Service.java`
- `asset-manager/worker/src/main/java/com/microsoft/migration/assets/worker/service/AbstractFileProcessingService.java`

</details>

<details id="CVE-2026-56819_Netty_HTTP_2_decompression_leaks_ByteBuf_reference_count_when_the_decompressor_channel_is_already_closed_Direct_memory_leak_OOM_DoS">
<summary><b>CVE-2026-56819: Netty: HTTP/2 decompression leaks ByteBuf reference count when the decompressor channel is already closed (Direct memory leak / OOM DoS)</b> — affected files</summary>

- `web/pom.xml:35`
- `worker/pom.xml:31`

</details>

<details id="CVE-2026-59901_Netty_Bzip2Decoder_Infinite_Loop_in_RLE_State_Machine_Leads_to_Event-Loop_Thread_Hang">
<summary><b>CVE-2026-59901: Netty: [Bzip2Decoder] Infinite Loop in RLE State Machine Leads to Event-Loop Thread Hang</b> — affected files</summary>

- `web/pom.xml:35`
- `worker/pom.xml:31`

</details>

<details id="CVE-2026-56745_Netty_SpdyHttpDecoder_ByteBuf_Reference_Leak_on_RST_STREAM_Leads_to_Native_Memory_Exhaustion">
<summary><b>CVE-2026-56745: Netty: [SpdyHttpDecoder] ByteBuf Reference Leak on RST_STREAM Leads to Native Memory Exhaustion</b> — affected files</summary>

- `web/pom.xml:35`
- `worker/pom.xml:31`

</details>

<details id="CVE-2026-55833_Netty_SPDY_zlib_header_block_continues_decoded_expansion_after_maxHeaderSize_truncation">
<summary><b>CVE-2026-55833: Netty SPDY zlib header block continues decoded expansion after maxHeaderSize truncation</b> — affected files</summary>

- `web/pom.xml:35`
- `worker/pom.xml:31`

</details>

<details id="CVE-2026-55831_Netty_SPDY_SETTINGS_frame_count_materializes_unbounded_settings_map">
<summary><b>CVE-2026-55831: Netty SPDY SETTINGS frame count materializes unbounded settings map</b> — affected files</summary>

- `web/pom.xml:35`
- `worker/pom.xml:31`

</details>

<details id="GHSA-r7wm-3cxj-wff9_jackson-core_Async_parser_maxNumberLength_bypass_via_chunked_digit_accumulation_incomplete_fix_for_GHSA-72hv-8253-57qq">
<summary><b>GHSA-r7wm-3cxj-wff9: jackson-core: Async parser maxNumberLength bypass via chunked digit accumulation (incomplete fix for GHSA-72hv-8253-57qq)</b> — affected files</summary>

- `web/pom.xml:27`
- `worker/pom.xml:45`

</details>

<details id="CVE-2026-54513_jackson-databind_has_an_array_subtype_allowlist_bypass_in_BasicPolymorphicTypeValidator_allowIfSubTypeIsArray">
<summary><b>CVE-2026-54513: jackson-databind has an array subtype allowlist bypass in BasicPolymorphicTypeValidator (allowIfSubTypeIsArray)</b> — affected files</summary>

- `web/pom.xml:27`
- `worker/pom.xml:45`

</details>

<details id="CVE-2026-54512_jackson-databind_has_a_PolymorphicTypeValidator_bypass_via_generic_type_parameters_that_allows_arbitrary_class_instantiation">
<summary><b>CVE-2026-54512: jackson-databind has a PolymorphicTypeValidator bypass via generic type parameters that allows arbitrary class instantiation</b> — affected files</summary>

- `web/pom.xml:27`
- `worker/pom.xml:45`

</details>

<details id="CVE-2026-50010_Netty_Wrapping_plain_trust_manager_silently_disables_hostname_verification">
<summary><b>CVE-2026-50010: Netty: Wrapping plain trust manager silently disables hostname verification</b> — affected files</summary>

- `web/pom.xml:35`
- `worker/pom.xml:31`

</details>

<details id="CVE-2026-45416_Netty_SNI_handler_pre-allocates_up_to_16_MiB_from_nine_attacker_bytes">
<summary><b>CVE-2026-45416: Netty: SNI handler pre-allocates up to 16 MiB from nine attacker bytes</b> — affected files</summary>

- `web/pom.xml:35`
- `worker/pom.xml:31`

</details>

<details id="CVE-2026-44249_Netty_has_an_IPv6_Subnet_Filter_Bypass_via_Incorrect_Comparator_Masking">
<summary><b>CVE-2026-44249: Netty has an IPv6 Subnet Filter Bypass via Incorrect Comparator Masking</b> — affected files</summary>

- `web/pom.xml:35`
- `worker/pom.xml:31`

</details>

<details id="CVE-2026-42587_Netty_HttpContentDecompressor_maxAllocation_bypass_when_Content-Encoding_set_to_br_zstd_snappy_leads_to_decompression_bomb_DoS">
<summary><b>CVE-2026-42587: Netty: HttpContentDecompressor maxAllocation bypass when Content-Encoding set to br/zstd/snappy leads to decompression bomb DoS</b> — affected files</summary>

- `web/pom.xml:35`
- `worker/pom.xml:31`

</details>

<details id="CVE-2026-42584_Netty_has_HttpClientCodec_response_desynchronization">
<summary><b>CVE-2026-42584: Netty has HttpClientCodec response desynchronization</b> — affected files</summary>

- `web/pom.xml:35`
- `worker/pom.xml:31`

</details>

<details id="CVE-2026-42583_Netty_Lz4FrameDecoder_is_vulnerable_to_resource_exhaustion">
<summary><b>CVE-2026-42583: Netty Lz4FrameDecoder is vulnerable to resource exhaustion </b> — affected files</summary>

- `web/pom.xml:35`
- `worker/pom.xml:31`

</details>

<details id="CVE-2026-33871_Netty_HTTP_2_CONTINUATION_Frame_Flood_DoS_via_Zero-Byte_Frame_Bypass">
<summary><b>CVE-2026-33871: Netty HTTP/2 CONTINUATION Frame Flood DoS via Zero-Byte Frame Bypass</b> — affected files</summary>

- `web/pom.xml:35`
- `worker/pom.xml:31`

</details>

<details id="CVE-2026-33870_Netty_HTTP_Request_Smuggling_via_Chunked_Extension_Quoted-String_Parsing">
<summary><b>CVE-2026-33870: Netty: HTTP Request Smuggling via Chunked Extension Quoted-String Parsing</b> — affected files</summary>

- `web/pom.xml:35`
- `worker/pom.xml:31`

</details>

<details id="CVE-2025-55163_Netty_affected_by_MadeYouReset_HTTP_2_DDoS_vulnerability">
<summary><b>CVE-2025-55163: Netty affected by MadeYouReset HTTP/2 DDoS vulnerability</b> — affected files</summary>

- `web/pom.xml:35`
- `worker/pom.xml:31`

</details>

<details id="CVE-2025-52999_jackson-core_can_throw_a_StackoverflowError_when_processing_deeply_nested_data">
<summary><b>CVE-2025-52999: jackson-core can throw a StackoverflowError when processing deeply nested data</b> — affected files</summary>

- `web/pom.xml:27`
- `worker/pom.xml:45`

</details>

<details id="CVE-2025-24970_SslHandler_doesn_t_correctly_validate_packets_which_can_lead_to_native_crash_when_using_native_SSLEngine">
<summary><b>CVE-2025-24970: SslHandler doesn't correctly validate packets which can lead to native crash when using native SSLEngine</b> — affected files</summary>

- `web/pom.xml:35`
- `worker/pom.xml:31`

</details>

<details id="CVE-2023-6481_Logback_is_vulnerable_to_an_attacker_mounting_a_Denial-Of-Service_attack_by_sending_poisoned_data">
<summary><b>CVE-2023-6481: Logback is vulnerable to an attacker mounting a Denial-Of-Service attack by sending poisoned data</b> — affected files</summary>

- `web/pom.xml:23`
- `worker/pom.xml:23`

</details>

<details id="CVE-2023-6378_logback_serialization_vulnerability">
<summary><b>CVE-2023-6378: logback serialization vulnerability</b> — affected files</summary>

- `web/pom.xml:23`
- `worker/pom.xml:23`

</details>

<details id="CVE-2026-41284_Apache_Tomcat_Unbounded_read_in_WebDAV_LOCK_and_PROPFIND_handling">
<summary><b>CVE-2026-41284: Apache Tomcat: Unbounded read in WebDAV LOCK and  PROPFIND handling</b> — affected files</summary>

- `web/pom.xml:27`

</details>

<details id="CVE-2026-43512_Apache_Tomcat_-_Digest_authenticator_will_authenticate_any_unknown_user">
<summary><b>CVE-2026-43512: Apache Tomcat - Digest authenticator will authenticate any unknown user</b> — affected files</summary>

- `web/pom.xml:27`

</details>

<details id="CVE-2026-43513_Apache_Tomcat_LockOutRealm_treats_user_names_as_case-sensitive">
<summary><b>CVE-2026-43513: Apache Tomcat: LockOutRealm treats user names as case-sensitive</b> — affected files</summary>

- `web/pom.xml:27`

</details>

<details id="CVE-2026-43515_Apache_Tomcat_-_Security_constraints_not_correctly_applied">
<summary><b>CVE-2026-43515: Apache Tomcat - Security constraints not correctly applied</b> — affected files</summary>

- `web/pom.xml:27`

</details>

<details id="CVE-2026-41293_Apache_Tomcat_-_HTTP_2_request_headers_not_validated">
<summary><b>CVE-2026-41293: Apache Tomcat - HTTP/2 request headers not validated</b> — affected files</summary>

- `web/pom.xml:27`

</details>

<details id="CVE-2026-42498_Apache_Tomcat_-_WebSocket_authentication_header_exposure">
<summary><b>CVE-2026-42498: Apache Tomcat - WebSocket authentication header exposure</b> — affected files</summary>

- `web/pom.xml:27`

</details>

<details id="CVE-2026-34483_Apache_Tomcat_has_an_Improper_Encoding_or_Escaping_of_Output_vulnerability_in_the_JsonAccessLogValve">
<summary><b>CVE-2026-34483: Apache Tomcat has an Improper Encoding or Escaping of Output vulnerability in the JsonAccessLogValve</b> — affected files</summary>

- `web/pom.xml:27`

</details>

<details id="CVE-2026-34487_Apache_Tomcat_vulnerable_to_Insertion_of_Sensitive_Information_into_Log_File">
<summary><b>CVE-2026-34487: Apache Tomcat vulnerable to Insertion of Sensitive Information into Log File</b> — affected files</summary>

- `web/pom.xml:27`

</details>

<details id="CVE-2026-24880_Apache_Tomcat_has_an_HTTP_Request_Response_Smuggling_vulnerability">
<summary><b>CVE-2026-24880: Apache Tomcat has an HTTP Request/Response Smuggling vulnerability</b> — affected files</summary>

- `web/pom.xml:27`

</details>

<details id="CVE-2026-24734_Apache_Tomcat_has_an_Improper_Input_Validation_vulnerability">
<summary><b>CVE-2026-24734: Apache Tomcat has an Improper Input Validation vulnerability</b> — affected files</summary>

- `web/pom.xml:27`

</details>

<details id="CVE-2026-24400_AssertJ_has_XML_External_Entity_XXE_vulnerability_when_parsing_untrusted_XML_via_isXmlEqualTo_assertion">
<summary><b>CVE-2026-24400: AssertJ has XML External Entity (XXE) vulnerability when parsing untrusted XML via isXmlEqualTo assertion</b> — affected files</summary>

- `web/pom.xml:55`
- `worker/pom.xml:40`

</details>

<details id="CVE-2025-55752_Apache_Tomcat_Vulnerable_to_Relative_Path_Traversal">
<summary><b>CVE-2025-55752: Apache Tomcat Vulnerable to Relative Path Traversal</b> — affected files</summary>

- `web/pom.xml:27`

</details>

<details id="CVE-2025-48989_Apache_Tomcat_Improper_Resource_Shutdown_or_Release_vulnerability">
<summary><b>CVE-2025-48989: Apache Tomcat Improper Resource Shutdown or Release vulnerability</b> — affected files</summary>

- `web/pom.xml:27`

</details>

<details id="CVE-2025-53506_Apache_Tomcat_Coyote_vulnerable_to_Denial_of_Service_via_excessive_HTTP_2_streams">
<summary><b>CVE-2025-53506: Apache Tomcat Coyote vulnerable to Denial of Service via excessive HTTP/2 streams</b> — affected files</summary>

- `web/pom.xml:27`

</details>

<details id="CVE-2025-52520_Apache_Tomcat_Catalina_is_vulnerable_to_DoS_attack_through_bypassing_of_size_limits">
<summary><b>CVE-2025-52520: Apache Tomcat Catalina is vulnerable to DoS attack through bypassing of size limits</b> — affected files</summary>

- `web/pom.xml:27`

</details>

<details id="CVE-2025-48988_Apache_Tomcat_-_DoS_in_multipart_upload">
<summary><b>CVE-2025-48988: Apache Tomcat - DoS in multipart upload</b> — affected files</summary>

- `web/pom.xml:27`

</details>

<details id="CVE-2025-24813_Apache_Tomcat_Potential_RCE_and_or_information_disclosure_and_or_information_corruption_with_partial_PUT">
<summary><b>CVE-2025-24813: Apache Tomcat: Potential RCE and/or information disclosure and/or information corruption with partial PUT</b> — affected files</summary>

- `web/pom.xml:27`

</details>

<details id="CVE-2024-56337_Apache_Tomcat_Time-of-check_Time-of-use_TOCTOU_Race_Condition_vulnerability">
<summary><b>CVE-2024-56337: Apache Tomcat Time-of-check Time-of-use (TOCTOU) Race Condition vulnerability</b> — affected files</summary>

- `web/pom.xml:27`

</details>

<details id="CVE-2024-50379_Apache_Tomcat_Time-of-check_Time-of-use_TOCTOU_Race_Condition_vulnerability">
<summary><b>CVE-2024-50379: Apache Tomcat Time-of-check Time-of-use (TOCTOU) Race Condition vulnerability</b> — affected files</summary>

- `web/pom.xml:27`

</details>

<details id="CVE-2024-38286_Apache_Tomcat_Allocation_of_Resources_Without_Limits_or_Throttling_vulnerability">
<summary><b>CVE-2024-38286: Apache Tomcat Allocation of Resources Without Limits or Throttling vulnerability</b> — affected files</summary>

- `web/pom.xml:27`

</details>

<details id="CVE-2024-34750_Apache_Tomcat_-_Denial_of_Service">
<summary><b>CVE-2024-34750: Apache Tomcat - Denial of Service</b> — affected files</summary>

- `web/pom.xml:27`

</details>

<details id="CVE-2026-41850_Spring_Framework_Algorithmic_Denial_of_Service_via_SpEL_Expressions">
<summary><b>CVE-2026-41850: Spring Framework Algorithmic Denial of Service via SpEL Expressions</b> — affected files</summary>

- `web/pom.xml:27`
- `worker/pom.xml:23`

</details>

<details id="CVE-2026-41849_Spring_Framework_Denial_of_Service_via_Integer_Overflow_in_SpEL_Expressions">
<summary><b>CVE-2026-41849: Spring Framework Denial of Service via Integer Overflow in SpEL Expressions</b> — affected files</summary>

- `web/pom.xml:27`
- `worker/pom.xml:23`

</details>

<details id="CVE-2026-41845_Spring_Framework_Cross-site_Scripting_via_JavaScriptUtils">
<summary><b>CVE-2026-41845: Spring Framework Cross-site Scripting via JavaScriptUtils</b> — affected files</summary>

- `web/pom.xml:27`

</details>

<details id="CVE-2026-41842_Spring_Framework_Denial_of_Service_via_Versioned_Resources_in_Spring_MVC_and_WebFlux">
<summary><b>CVE-2026-41842: Spring Framework Denial of Service via Versioned Resources in Spring MVC and WebFlux</b> — affected files</summary>

- `web/pom.xml:27`

</details>

<details id="CVE-2026-42198_pgjdbc_Unbounded_PBKDF2_iterations_in_SCRAM_authentication_allows_CPU_exhaustion_DoS">
<summary><b>CVE-2026-42198: pgjdbc: Unbounded PBKDF2 iterations in SCRAM authentication allows CPU exhaustion DoS</b> — affected files</summary>

- `web/pom.xml:64`
- `worker/pom.xml:53`

</details>

<details id="CVE-2026-40973_Spring_Boot_accepts_predictable_temp_directory_without_ownership_verification">
<summary><b>CVE-2026-40973: Spring Boot accepts predictable temp directory without ownership verification</b> — affected files</summary>

- `web/pom.xml:39`
- `worker/pom.xml:23`

</details>

<details id="CVE-2025-41249_Spring_Framework_annotation_detection_mechanism_may_result_in_improper_authorization">
<summary><b>CVE-2025-41249: Spring Framework annotation detection mechanism may result in improper authorization</b> — affected files</summary>

- `web/pom.xml:55`
- `worker/pom.xml:23`

</details>

<details id="CVE-2025-22235_Spring_Boot_EndpointRequest_to_creates_wrong_matcher_if_actuator_endpoint_is_not_exposed">
<summary><b>CVE-2025-22235: Spring Boot EndpointRequest.to() creates wrong matcher if actuator endpoint is not exposed</b> — affected files</summary>

- `web/pom.xml:39`
- `worker/pom.xml:23`

</details>

<details id="CVE-2024-38819_Spring_Framework_Path_Traversal_vulnerability">
<summary><b>CVE-2024-38819: Spring Framework Path Traversal vulnerability</b> — affected files</summary>

- `web/pom.xml:27`

</details>

<details id="CVE-2024-38816_Path_traversal_vulnerability_in_functional_web_frameworks">
<summary><b>CVE-2024-38816: Path traversal vulnerability in functional web frameworks</b> — affected files</summary>

- `web/pom.xml:27`

</details>

<details id="CVE-2024-22262_Spring_Framework_URL_Parsing_with_Host_Validation">
<summary><b>CVE-2024-22262: Spring Framework URL Parsing with Host Validation</b> — affected files</summary>

- `web/pom.xml:27`

</details>

<details id="CVE-2024-22259_Spring_Framework_URL_Parsing_with_Host_Validation_Vulnerability">
<summary><b>CVE-2024-22259: Spring Framework URL Parsing with Host Validation Vulnerability</b> — affected files</summary>

- `web/pom.xml:27`

</details>

<details id="CVE-2024-22243_Spring_Web_vulnerable_to_Open_Redirect_or_Server_Side_Request_Forgery">
<summary><b>CVE-2024-22243: Spring Web vulnerable to Open Redirect or Server Side Request Forgery</b> — affected files</summary>

- `web/pom.xml:27`

</details>

<details id="CVE-2024-1597_org_postgresql_postgresql_vulnerable_to_SQL_Injection_via_line_comment_generation">
<summary><b>CVE-2024-1597: org.postgresql:postgresql vulnerable to SQL Injection via line comment generation</b> — affected files</summary>

- `web/pom.xml:64`
- `worker/pom.xml:53`

</details>

<details id="CVE-2016-1000027_Pivotal_Spring_Framework_contains_unsafe_Java_deserialization_methods">
<summary><b>CVE-2016-1000027: Pivotal Spring Framework contains unsafe Java deserialization methods</b> — affected files</summary>

- `web/pom.xml:27`

</details>

<details id="CVE-2026-41716_Spring_Data_Commons_Heap_exhaustion_from_unbounded_property-lookup_cache_retaining_crafted_string_keys">
<summary><b>CVE-2026-41716: Spring Data Commons: Heap exhaustion from unbounded property-lookup cache retaining crafted string keys</b> — affected files</summary>

- `web/pom.xml:60`
- `worker/pom.xml:49`

</details>

<details id="CVE-2026-41901_Sandboxed_Thymeleaf_expressions_vulnerable_to_improper_recognition_of_unauthorized_syntax_patterns">
<summary><b>CVE-2026-41901: Sandboxed Thymeleaf expressions vulnerable to improper recognition of unauthorized syntax patterns</b> — affected files</summary>

- `web/pom.xml:23`

</details>

<details id="CVE-2026-40972_Spring_Boot_DevTools_remote_secret_comparison_is_vulnerable_to_timing_attacks">
<summary><b>CVE-2026-40972: Spring Boot DevTools remote secret comparison is vulnerable to timing attacks</b> — affected files</summary>

- `web/pom.xml:39`

</details>

<details id="CVE-2026-40478_Improper_neutralization_of_specific_syntax_patterns_for_unauthorized_expressions_in_Thymeleaf">
<summary><b>CVE-2026-40478: Improper neutralization of specific syntax patterns for unauthorized expressions in Thymeleaf</b> — affected files</summary>

- `web/pom.xml:23`

</details>

<details id="CVE-2026-40477_Improper_restriction_of_the_scope_of_accessible_objects_in_Thymeleaf_expressions">
<summary><b>CVE-2026-40477: Improper restriction of the scope of accessible objects in Thymeleaf expressions</b> — affected files</summary>

- `web/pom.xml:23`

</details>

<details id="CVE-2022-1471_SnakeYaml_Constructor_Deserialization_Remote_Code_Execution">
<summary><b>CVE-2022-1471: SnakeYaml Constructor Deserialization Remote Code Execution</b> — affected files</summary>

- `web/pom.xml:23`
- `worker/pom.xml:23`

</details>

<details id="CVE-2022-25857_Uncontrolled_Resource_Consumption_in_snakeyaml">
<summary><b>CVE-2022-25857: Uncontrolled Resource Consumption in snakeyaml</b> — affected files</summary>

- `web/pom.xml:23`
- `worker/pom.xml:23`

</details>

<details id="CWE-99_Improper_Control_of_Resource_Identifiers_Resource_Injection">
<summary><b>CWE-99: Improper Control of Resource Identifiers ('Resource Injection')</b> — affected files</summary>

- `asset-manager/web/src/main/java/com/microsoft/migration/assets/controller/S3Controller.java`
- `asset-manager/web/src/main/java/com/microsoft/migration/assets/service/LocalFileStorageService.java`
- `asset-manager/worker/src/main/java/com/microsoft/migration/assets/worker/service/LocalFileProcessingService.java`

</details>

<details id="CWE-22_Improper_Limitation_of_a_Pathname_to_a_Restricted_Directory_Path_Traversal">
<summary><b>CWE-22: Improper Limitation of a Pathname to a Restricted Directory ('Path Traversal')</b> — affected files</summary>

- `asset-manager/web/src/main/java/com/microsoft/migration/assets/controller/S3Controller.java`
- `asset-manager/web/src/main/java/com/microsoft/migration/assets/service/LocalFileStorageService.java`

</details>

<details id="CWE-259_Use_of_Hard-coded_Password">
<summary><b>CWE-259: Use of Hard-coded Password</b> — affected files</summary>

- `asset-manager/web/src/main/resources/application.properties`
- `asset-manager/worker/src/main/resources/application.properties`

</details>

<details id="CWE-798_Use_of_Hard-coded_Credentials">
<summary><b>CWE-798: Use of Hard-coded Credentials</b> — affected files</summary>

- `asset-manager/web/src/main/resources/application.properties`
- `asset-manager/worker/src/main/resources/application.properties`
- `asset-manager/web/src/main/java/com/microsoft/migration/assets/config/AwsS3Config.java`
- `asset-manager/worker/src/main/java/com/microsoft/migration/assets/worker/config/AwsS3Config.java`

</details>

<details id="CWE-23_Relative_Path_Traversal">
<summary><b>CWE-23: Relative Path Traversal</b> — affected files</summary>

- `asset-manager/web/src/main/java/com/microsoft/migration/assets/controller/S3Controller.java`
- `asset-manager/web/src/main/java/com/microsoft/migration/assets/service/LocalFileStorageService.java`
- `asset-manager/worker/src/main/java/com/microsoft/migration/assets/worker/service/LocalFileProcessingService.java`

</details>

<details id="CWE-36_Absolute_Path_Traversal">
<summary><b>CWE-36: Absolute Path Traversal</b> — affected files</summary>

- `asset-manager/web/src/main/java/com/microsoft/migration/assets/service/LocalFileStorageService.java`
- `asset-manager/worker/src/main/java/com/microsoft/migration/assets/worker/service/LocalFileProcessingService.java`

</details>

<details id="CWE-477_Use_of_Obsolete_Function">
<summary><b>CWE-477: Use of Obsolete Function</b> — affected files</summary>

- `asset-manager/web/src/main/java/com/microsoft/migration/assets/config/WebMvcConfig.java`

</details>

---

## Codebase Insights

> **Note:** These documents are generated by AI and may contain inaccuracies or incomplete information. Please review carefully.

> **Codebase Insights aren't available yet.**
>
> These documents are generated when assessment runs with **Full analysis** coverage. Re-run the assessment and set `analysisCoverage: full` to enable them.

[Share feedback](https://aka.ms/ghcp-appmod/feedback)
