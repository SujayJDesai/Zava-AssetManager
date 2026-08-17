# Security Assessment Report

**Generated:** 2026-08-17T09:07:07.0000000Z

## Summary

| Metric | Count |
|--------|-------|
| Total Findings | 27 |
| CVE Vulnerabilities | 27 |
| CWE Vulnerabilities | 0 |
| Total Rules Assessed | 59 |
| Rules Passed | 59 |

### By Severity

| Severity | Count |
|----------|-------|
| mandatory | 27 |
| optional | 0 |
| potential | 0 |

## CVE Findings (Dependency Vulnerabilities)

### GHSA-r7wm-3cxj-wff9: jackson-core: Async parser maxNumberLength bypass via chunked digit accumulation (incomplete fix for GHSA-72hv-8253-57qq)
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:67

[GHSA-r7wm-3cxj-wff9](https://github.com/advisories/GHSA-r7wm-3cxj-wff9): jackson-core: Async parser maxNumberLength bypass via chunked digit accumulation (incomplete fix for GHSA-72hv-8253-57qq)

Severity: HIGH

Affected dependencies:
  - com.fasterxml.jackson.core:jackson-core:2.17.1 (transitive, pulled by com.fasterxml.jackson.core:jackson-databind at pom.xml:67), patch: upgrade to 2.18.8

Recommended fix:
  - Upgrade com.fasterxml.jackson.core:jackson-core to 2.18.8 or later

### CVE-2026-54513: jackson-databind has an array subtype allowlist bypass in BasicPolymorphicTypeValidator (allowIfSubTypeIsArray)
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:67

[CVE-2026-54513](https://github.com/advisories/GHSA-rmj7-2vxq-3g9f): jackson-databind has an array subtype allowlist bypass in BasicPolymorphicTypeValidator (allowIfSubTypeIsArray)

Severity: HIGH

Affected dependencies:
  - com.fasterxml.jackson.core:jackson-databind:2.17.1 (declared at pom.xml:67), patch: upgrade to 2.18.8

Recommended fix:
  - Upgrade com.fasterxml.jackson.core:jackson-databind to 2.18.8 or later

### CVE-2026-54512: jackson-databind has a PolymorphicTypeValidator bypass via generic type parameters that allows arbitrary class instantiation
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:67

[CVE-2026-54512](https://github.com/advisories/GHSA-j3rv-43j4-c7qm): jackson-databind has a PolymorphicTypeValidator bypass via generic type parameters that allows arbitrary class instantiation

Severity: HIGH

Affected dependencies:
  - com.fasterxml.jackson.core:jackson-databind:2.17.1 (declared at pom.xml:67), patch: upgrade to 2.18.8

Recommended fix:
  - Upgrade com.fasterxml.jackson.core:jackson-databind to 2.18.8 or later

### CVE-2026-56819: Netty: HTTP/2 decompression leaks ByteBuf reference count when the decompressor channel is already closed (Direct memory leak / OOM DoS)
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-56819](https://github.com/advisories/GHSA-93wv-jw9v-4972): Netty: HTTP/2 decompression leaks ByteBuf reference count when the decompressor channel is already closed (Direct memory leak / OOM DoS)

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http2:4.1.110.Final (transitive, pulled by com.azure:azure-core-http-netty at pom.xml), patch: upgrade to 4.1.136.Final

Recommended fix:
  - Upgrade io.netty:netty-codec-http2 to 4.1.136.Final or later

### CVE-2026-59901: Netty: [Bzip2Decoder] Infinite Loop in RLE State Machine Leads to Event-Loop Thread Hang
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-59901](https://github.com/advisories/GHSA-558v-64gr-wgg4): Netty: [Bzip2Decoder] Infinite Loop in RLE State Machine Leads to Event-Loop Thread Hang

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec:4.1.110.Final (transitive, pulled by com.azure:azure-core-http-netty at pom.xml), patch: upgrade to 4.1.136.Final

Recommended fix:
  - Upgrade io.netty:netty-codec to 4.1.136.Final or later

### CVE-2026-56745: Netty: [SpdyHttpDecoder] ByteBuf Reference Leak on RST_STREAM Leads to Native Memory Exhaustion
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-56745](https://github.com/advisories/GHSA-jppx-w49h-x2qq): Netty: [SpdyHttpDecoder] ByteBuf Reference Leak on RST_STREAM Leads to Native Memory Exhaustion

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http:4.1.110.Final (transitive, pulled by com.azure:azure-core-http-netty at pom.xml), patch: upgrade to 4.1.136.Final

Recommended fix:
  - Upgrade io.netty:netty-codec-http to 4.1.136.Final or later

### CVE-2026-55833: Netty SPDY zlib header block continues decoded expansion after maxHeaderSize truncation
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-55833](https://github.com/advisories/GHSA-mvh2-crg5-v77c): Netty SPDY zlib header block continues decoded expansion after maxHeaderSize truncation

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http:4.1.110.Final (transitive, pulled by com.azure:azure-core-http-netty at pom.xml), patch: upgrade to 4.1.136.Final

Recommended fix:
  - Upgrade io.netty:netty-codec-http to 4.1.136.Final or later

### CVE-2026-55831: Netty SPDY SETTINGS frame count materializes unbounded settings map
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-55831](https://github.com/advisories/GHSA-6jqx-86gh-f27w): Netty SPDY SETTINGS frame count materializes unbounded settings map

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http:4.1.110.Final (transitive, pulled by com.azure:azure-core-http-netty at pom.xml), patch: upgrade to 4.1.136.Final

Recommended fix:
  - Upgrade io.netty:netty-codec-http to 4.1.136.Final or later

### CVE-2026-50010: Netty: Wrapping plain trust manager silently disables hostname verification
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-50010](https://github.com/advisories/GHSA-c653-97m9-rcg9): Netty: Wrapping plain trust manager silently disables hostname verification

Severity: HIGH

Affected dependencies:
  - io.netty:netty-handler:4.1.110.Final (transitive, pulled by com.azure:azure-core-http-netty at pom.xml), patch: upgrade to 4.1.135.Final

Recommended fix:
  - Upgrade io.netty:netty-handler to 4.1.135.Final or later

### CVE-2026-47691: Netty has Insufficient Bailiwick Validation for NS Records
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-47691](https://github.com/advisories/GHSA-5pvg-856g-cp85): Netty has Insufficient Bailiwick Validation for NS Records

Severity: HIGH

Affected dependencies:
  - io.netty:netty-resolver-dns:4.1.110.Final (transitive, pulled by io.projectreactor.netty:reactor-netty-http at pom.xml), patch: upgrade to 4.1.135.Final

Recommended fix:
  - Upgrade io.netty:netty-resolver-dns to 4.1.135.Final or later

### CVE-2026-45674: Netty Vulnerable to DNS Cache Poisoning via Missing Bailiwick Checks in CNAME Records
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-45674](https://github.com/advisories/GHSA-676x-f7gg-47vc): Netty Vulnerable to DNS Cache Poisoning via Missing Bailiwick Checks in CNAME Records

Severity: HIGH

Affected dependencies:
  - io.netty:netty-resolver-dns:4.1.110.Final (transitive, pulled by io.projectreactor.netty:reactor-netty-http at pom.xml), patch: upgrade to 4.1.135.Final

Recommended fix:
  - Upgrade io.netty:netty-resolver-dns to 4.1.135.Final or later

### CVE-2026-45416: Netty: SNI handler pre-allocates up to 16 MiB from nine attacker bytes
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-45416](https://github.com/advisories/GHSA-x4gw-5cx5-pgmh): Netty: SNI handler pre-allocates up to 16 MiB from nine attacker bytes

Severity: HIGH

Affected dependencies:
  - io.netty:netty-handler:4.1.110.Final (transitive, pulled by com.azure:azure-core-http-netty at pom.xml), patch: upgrade to 4.1.135.Final

Recommended fix:
  - Upgrade io.netty:netty-handler to 4.1.135.Final or later

### CVE-2026-44249: Netty has an IPv6 Subnet Filter Bypass via Incorrect Comparator Masking
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-44249](https://github.com/advisories/GHSA-3qp7-7mw8-wx86): Netty has an IPv6 Subnet Filter Bypass via Incorrect Comparator Masking

Severity: HIGH

Affected dependencies:
  - io.netty:netty-handler:4.1.110.Final (transitive, pulled by com.azure:azure-core-http-netty at pom.xml), patch: upgrade to 4.1.135.Final

Recommended fix:
  - Upgrade io.netty:netty-handler to 4.1.135.Final or later

### CVE-2026-42587: Netty: HttpContentDecompressor maxAllocation bypass when Content-Encoding set to br/zstd/snappy leads to decompression bomb DoS
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-42587](https://github.com/advisories/GHSA-f6hv-jmp6-3vwv): Netty: HttpContentDecompressor maxAllocation bypass when Content-Encoding set to br/zstd/snappy leads to decompression bomb DoS

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http:4.1.110.Final (transitive, pulled by com.azure:azure-core-http-netty at pom.xml), patch: upgrade to 4.1.133.Final
  - io.netty:netty-codec-http2:4.1.110.Final (transitive, pulled by com.azure:azure-core-http-netty at pom.xml), patch: upgrade to 4.1.133.Final

Recommended fix:
  - Upgrade io.netty:netty-codec-http to 4.1.133.Final or later
  - Upgrade io.netty:netty-codec-http2 to 4.1.133.Final or later

### CVE-2026-42584: Netty has HttpClientCodec response desynchronization
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-42584](https://github.com/advisories/GHSA-57rv-r2g8-2cj3): Netty has HttpClientCodec response desynchronization

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http:4.1.110.Final (transitive, pulled by com.azure:azure-core-http-netty at pom.xml), patch: upgrade to 4.1.133.Final

Recommended fix:
  - Upgrade io.netty:netty-codec-http to 4.1.133.Final or later

### CVE-2026-42583: Netty Lz4FrameDecoder is vulnerable to resource exhaustion 
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-42583](https://github.com/advisories/GHSA-mj4r-2hfc-f8p6): Netty Lz4FrameDecoder is vulnerable to resource exhaustion 

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec:4.1.110.Final (transitive, pulled by com.azure:azure-core-http-netty at pom.xml), patch: upgrade to 4.1.133.Final

Recommended fix:
  - Upgrade io.netty:netty-codec to 4.1.133.Final or later

### CVE-2026-42579: Netty has a DNS Codec Input Validation Bypass (Encoder + Decoder)
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-42579](https://github.com/advisories/GHSA-cm33-6792-r9fm): Netty has a DNS Codec Input Validation Bypass (Encoder + Decoder)

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-dns:4.1.110.Final (transitive, pulled by io.netty:netty-resolver-dns at pom.xml), patch: upgrade to 4.1.133.Final

Recommended fix:
  - Upgrade io.netty:netty-codec-dns to 4.1.133.Final or later

### CVE-2026-33871: Netty HTTP/2 CONTINUATION Frame Flood DoS via Zero-Byte Frame Bypass
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-33871](https://github.com/advisories/GHSA-w9fj-cfpg-grvv): Netty HTTP/2 CONTINUATION Frame Flood DoS via Zero-Byte Frame Bypass

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http2:4.1.110.Final (transitive, pulled by com.azure:azure-core-http-netty at pom.xml), patch: upgrade to 4.1.132.Final

Recommended fix:
  - Upgrade io.netty:netty-codec-http2 to 4.1.132.Final or later

### CVE-2026-33870: Netty: HTTP Request Smuggling via Chunked Extension Quoted-String Parsing
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-33870](https://github.com/advisories/GHSA-pwqr-wmgm-9rr8): Netty: HTTP Request Smuggling via Chunked Extension Quoted-String Parsing

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http:4.1.110.Final (transitive, pulled by com.azure:azure-core-http-netty at pom.xml), patch: upgrade to 4.1.132.Final

Recommended fix:
  - Upgrade io.netty:netty-codec-http to 4.1.132.Final or later

### CVE-2025-55163: Netty affected by MadeYouReset HTTP/2 DDoS vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2025-55163](https://github.com/advisories/GHSA-prj3-ccx8-p6x4): Netty affected by MadeYouReset HTTP/2 DDoS vulnerability

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http2:4.1.110.Final (transitive, pulled by com.azure:azure-core-http-netty at pom.xml), patch: upgrade to 4.1.124.Final

Recommended fix:
  - Upgrade io.netty:netty-codec-http2 to 4.1.124.Final or later

### CVE-2025-24970: SslHandler doesn't correctly validate packets which can lead to native crash when using native SSLEngine
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2025-24970](https://github.com/advisories/GHSA-4g8c-wm8x-jfhw): SslHandler doesn't correctly validate packets which can lead to native crash when using native SSLEngine

Severity: HIGH

Affected dependencies:
  - io.netty:netty-handler:4.1.110.Final (transitive, pulled by com.azure:azure-core-http-netty at pom.xml), patch: upgrade to 4.1.118.Final

Recommended fix:
  - Upgrade io.netty:netty-handler to 4.1.118.Final or later

### CVE-2026-24400: AssertJ has XML External Entity (XXE) vulnerability when parsing untrusted XML via isXmlEqualTo assertion
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:50

[CVE-2026-24400](https://github.com/advisories/GHSA-rqfh-9r24-8c9r): AssertJ has XML External Entity (XXE) vulnerability when parsing untrusted XML via isXmlEqualTo assertion

Severity: HIGH

Affected dependencies:
  - org.assertj:assertj-core:3.25.3 (transitive, pulled by org.springframework.boot:spring-boot-starter-test at pom.xml:50), patch: upgrade to 3.27.7

Recommended fix:
  - Upgrade org.assertj:assertj-core to 3.27.7 or later

### CVE-2024-57699: Netplex Json-smart Uncontrolled Recursion vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:50

[CVE-2024-57699](https://github.com/advisories/GHSA-pq2g-wx69-c263): Netplex Json-smart Uncontrolled Recursion vulnerability

Severity: HIGH

Affected dependencies:
  - net.minidev:json-smart:2.5.1 (transitive, pulled by org.springframework.boot:spring-boot-starter-test at pom.xml:50), patch: upgrade to 2.5.2

Recommended fix:
  - Upgrade net.minidev:json-smart to 2.5.2 or later

### CVE-2026-41850: Spring Framework Algorithmic Denial of Service via SpEL Expressions
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-41850](https://github.com/advisories/GHSA-r5w3-xv2f-j59q): Spring Framework Algorithmic Denial of Service via SpEL Expressions

Severity: HIGH

Affected dependencies:
  - org.springframework:spring-expression:6.1.8 (transitive, pulled by org.springframework:spring-context at pom.xml)

Recommended fix:


### CVE-2026-40973: Spring Boot accepts predictable temp directory without ownership verification
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2026-40973](https://github.com/advisories/GHSA-wwpq-f5c3-7hvx): Spring Boot accepts predictable temp directory without ownership verification

Severity: HIGH

Affected dependencies:
  - org.springframework.boot:spring-boot:3.3.0 (transitive, pulled by org.springframework.boot:spring-boot-starter at pom.xml)

Recommended fix:


### CVE-2025-41249: Spring Framework annotation detection mechanism may result in improper authorization
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml:50

[CVE-2025-41249](https://github.com/advisories/GHSA-jmp9-x22r-554x): Spring Framework annotation detection mechanism may result in improper authorization

Severity: HIGH

Affected dependencies:
  - org.springframework:spring-core:6.1.8 (transitive, pulled by org.springframework.boot:spring-boot-starter-test at pom.xml:50)

Recommended fix:


### CVE-2025-22235: Spring Boot EndpointRequest.to() creates wrong matcher if actuator endpoint is not exposed
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** pom.xml

[CVE-2025-22235](https://github.com/advisories/GHSA-rc42-6c7j-7h5r): Spring Boot EndpointRequest.to() creates wrong matcher if actuator endpoint is not exposed

Severity: HIGH

Affected dependencies:
  - org.springframework.boot:spring-boot:3.3.0 (transitive, pulled by org.springframework.boot:spring-boot-starter at pom.xml), patch: upgrade to 3.3.11

Recommended fix:
  - Upgrade org.springframework.boot:spring-boot to 3.3.11 or later

