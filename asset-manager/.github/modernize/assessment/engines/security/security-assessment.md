# Security Assessment Report

**Generated:** 2026-08-17T09:09:14.0000000Z

## Summary

| Metric | Count |
|--------|-------|
| Total Findings | 72 |
| CVE Vulnerabilities | 64 |
| CWE Vulnerabilities | 8 |
| Total Rules Assessed | 59 |
| Rules Passed | 51 |

### By Severity

| Severity | Count |
|----------|-------|
| mandatory | 65 |
| optional | 6 |
| potential | 1 |

## CVE Findings (Dependency Vulnerabilities)

### CVE-2026-56819: Netty: HTTP/2 decompression leaks ByteBuf reference count when the decompressor channel is already closed (Direct memory leak / OOM DoS)
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:35, worker/pom.xml:31

[CVE-2026-56819](https://github.com/advisories/GHSA-93wv-jw9v-4972): Netty: HTTP/2 decompression leaks ByteBuf reference count when the decompressor channel is already closed (Direct memory leak / OOM DoS)

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http2:4.1.101.Final (transitive, pulled by software.amazon.awssdk:s3 at worker/pom.xml:31)
  - io.netty:netty-codec-http2:4.1.101.Final (transitive, pulled by software.amazon.awssdk:s3 at web/pom.xml:35)

Recommended fix:
  - Upgrade io.netty:netty-codec-http2 to 4.1.136.Final or later

### CVE-2026-59901: Netty: [Bzip2Decoder] Infinite Loop in RLE State Machine Leads to Event-Loop Thread Hang
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:35, worker/pom.xml:31

[CVE-2026-59901](https://github.com/advisories/GHSA-558v-64gr-wgg4): Netty: [Bzip2Decoder] Infinite Loop in RLE State Machine Leads to Event-Loop Thread Hang

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec:4.1.101.Final (transitive, pulled by software.amazon.awssdk:s3 at worker/pom.xml:31)
  - io.netty:netty-codec:4.1.101.Final (transitive, pulled by software.amazon.awssdk:s3 at web/pom.xml:35)

Recommended fix:
  - Upgrade io.netty:netty-codec to 4.1.136.Final or later

### CVE-2026-56745: Netty: [SpdyHttpDecoder] ByteBuf Reference Leak on RST_STREAM Leads to Native Memory Exhaustion
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:35, worker/pom.xml:31

[CVE-2026-56745](https://github.com/advisories/GHSA-jppx-w49h-x2qq): Netty: [SpdyHttpDecoder] ByteBuf Reference Leak on RST_STREAM Leads to Native Memory Exhaustion

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http:4.1.101.Final (transitive, pulled by software.amazon.awssdk:s3 at worker/pom.xml:31)
  - io.netty:netty-codec-http:4.1.101.Final (transitive, pulled by software.amazon.awssdk:s3 at web/pom.xml:35)

Recommended fix:
  - Upgrade io.netty:netty-codec-http to 4.1.136.Final or later

### CVE-2026-55833: Netty SPDY zlib header block continues decoded expansion after maxHeaderSize truncation
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:35, worker/pom.xml:31

[CVE-2026-55833](https://github.com/advisories/GHSA-mvh2-crg5-v77c): Netty SPDY zlib header block continues decoded expansion after maxHeaderSize truncation

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http:4.1.101.Final (transitive, pulled by software.amazon.awssdk:s3 at worker/pom.xml:31)
  - io.netty:netty-codec-http:4.1.101.Final (transitive, pulled by software.amazon.awssdk:s3 at web/pom.xml:35)

Recommended fix:
  - Upgrade io.netty:netty-codec-http to 4.1.136.Final or later

### CVE-2026-55831: Netty SPDY SETTINGS frame count materializes unbounded settings map
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:35, worker/pom.xml:31

[CVE-2026-55831](https://github.com/advisories/GHSA-6jqx-86gh-f27w): Netty SPDY SETTINGS frame count materializes unbounded settings map

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http:4.1.101.Final (transitive, pulled by software.amazon.awssdk:s3 at worker/pom.xml:31)
  - io.netty:netty-codec-http:4.1.101.Final (transitive, pulled by software.amazon.awssdk:s3 at web/pom.xml:35)

Recommended fix:
  - Upgrade io.netty:netty-codec-http to 4.1.136.Final or later

### GHSA-r7wm-3cxj-wff9: jackson-core: Async parser maxNumberLength bypass via chunked digit accumulation (incomplete fix for GHSA-72hv-8253-57qq)
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27, worker/pom.xml:45

[GHSA-r7wm-3cxj-wff9](https://github.com/advisories/GHSA-r7wm-3cxj-wff9): jackson-core: Async parser maxNumberLength bypass via chunked digit accumulation (incomplete fix for GHSA-72hv-8253-57qq)

Severity: HIGH

Affected dependencies:
  - com.fasterxml.jackson.core:jackson-core:2.13.5 (transitive, pulled by com.fasterxml.jackson.core:jackson-databind at worker/pom.xml:45)
  - com.fasterxml.jackson.core:jackson-core:2.13.5 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)

Recommended fix:
  - Upgrade com.fasterxml.jackson.core:jackson-core to 2.18.8 or later

### CVE-2026-54513: jackson-databind has an array subtype allowlist bypass in BasicPolymorphicTypeValidator (allowIfSubTypeIsArray)
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27, worker/pom.xml:45

[CVE-2026-54513](https://github.com/advisories/GHSA-rmj7-2vxq-3g9f): jackson-databind has an array subtype allowlist bypass in BasicPolymorphicTypeValidator (allowIfSubTypeIsArray)

Severity: HIGH

Affected dependencies:
  - com.fasterxml.jackson.core:jackson-databind:2.13.5 (declared at worker/pom.xml:45)
  - com.fasterxml.jackson.core:jackson-databind:2.13.5 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)

Recommended fix:
  - Upgrade com.fasterxml.jackson.core:jackson-databind to 2.18.8 or later

### CVE-2026-54512: jackson-databind has a PolymorphicTypeValidator bypass via generic type parameters that allows arbitrary class instantiation
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27, worker/pom.xml:45

[CVE-2026-54512](https://github.com/advisories/GHSA-j3rv-43j4-c7qm): jackson-databind has a PolymorphicTypeValidator bypass via generic type parameters that allows arbitrary class instantiation

Severity: HIGH

Affected dependencies:
  - com.fasterxml.jackson.core:jackson-databind:2.13.5 (declared at worker/pom.xml:45)
  - com.fasterxml.jackson.core:jackson-databind:2.13.5 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)

Recommended fix:
  - Upgrade com.fasterxml.jackson.core:jackson-databind to 2.18.8 or later

### CVE-2026-50010: Netty: Wrapping plain trust manager silently disables hostname verification
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:35, worker/pom.xml:31

[CVE-2026-50010](https://github.com/advisories/GHSA-c653-97m9-rcg9): Netty: Wrapping plain trust manager silently disables hostname verification

Severity: HIGH

Affected dependencies:
  - io.netty:netty-handler:4.1.101.Final (transitive, pulled by software.amazon.awssdk:s3 at worker/pom.xml:31)
  - io.netty:netty-handler:4.1.101.Final (transitive, pulled by software.amazon.awssdk:s3 at web/pom.xml:35)

Recommended fix:
  - Upgrade io.netty:netty-handler to 4.1.135.Final or later

### CVE-2026-45416: Netty: SNI handler pre-allocates up to 16 MiB from nine attacker bytes
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:35, worker/pom.xml:31

[CVE-2026-45416](https://github.com/advisories/GHSA-x4gw-5cx5-pgmh): Netty: SNI handler pre-allocates up to 16 MiB from nine attacker bytes

Severity: HIGH

Affected dependencies:
  - io.netty:netty-handler:4.1.101.Final (transitive, pulled by software.amazon.awssdk:s3 at worker/pom.xml:31)
  - io.netty:netty-handler:4.1.101.Final (transitive, pulled by software.amazon.awssdk:s3 at web/pom.xml:35)

Recommended fix:
  - Upgrade io.netty:netty-handler to 4.1.135.Final or later

### CVE-2026-44249: Netty has an IPv6 Subnet Filter Bypass via Incorrect Comparator Masking
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:35, worker/pom.xml:31

[CVE-2026-44249](https://github.com/advisories/GHSA-3qp7-7mw8-wx86): Netty has an IPv6 Subnet Filter Bypass via Incorrect Comparator Masking

Severity: HIGH

Affected dependencies:
  - io.netty:netty-handler:4.1.101.Final (transitive, pulled by software.amazon.awssdk:s3 at worker/pom.xml:31)
  - io.netty:netty-handler:4.1.101.Final (transitive, pulled by software.amazon.awssdk:s3 at web/pom.xml:35)

Recommended fix:
  - Upgrade io.netty:netty-handler to 4.1.135.Final or later

### CVE-2026-42587: Netty: HttpContentDecompressor maxAllocation bypass when Content-Encoding set to br/zstd/snappy leads to decompression bomb DoS
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:35, worker/pom.xml:31

[CVE-2026-42587](https://github.com/advisories/GHSA-f6hv-jmp6-3vwv): Netty: HttpContentDecompressor maxAllocation bypass when Content-Encoding set to br/zstd/snappy leads to decompression bomb DoS

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http:4.1.101.Final (transitive, pulled by software.amazon.awssdk:s3 at worker/pom.xml:31)
  - io.netty:netty-codec-http:4.1.101.Final (transitive, pulled by software.amazon.awssdk:s3 at web/pom.xml:35)
  - io.netty:netty-codec-http2:4.1.101.Final (transitive, pulled by software.amazon.awssdk:s3 at worker/pom.xml:31)
  - io.netty:netty-codec-http2:4.1.101.Final (transitive, pulled by software.amazon.awssdk:s3 at web/pom.xml:35)

Recommended fix:
  - Upgrade io.netty:netty-codec-http to 4.1.133.Final or later
  - Upgrade io.netty:netty-codec-http2 to 4.1.133.Final or later

### CVE-2026-42584: Netty has HttpClientCodec response desynchronization
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:35, worker/pom.xml:31

[CVE-2026-42584](https://github.com/advisories/GHSA-57rv-r2g8-2cj3): Netty has HttpClientCodec response desynchronization

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http:4.1.101.Final (transitive, pulled by software.amazon.awssdk:s3 at worker/pom.xml:31)
  - io.netty:netty-codec-http:4.1.101.Final (transitive, pulled by software.amazon.awssdk:s3 at web/pom.xml:35)

Recommended fix:
  - Upgrade io.netty:netty-codec-http to 4.1.133.Final or later

### CVE-2026-42583: Netty Lz4FrameDecoder is vulnerable to resource exhaustion 
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:35, worker/pom.xml:31

[CVE-2026-42583](https://github.com/advisories/GHSA-mj4r-2hfc-f8p6): Netty Lz4FrameDecoder is vulnerable to resource exhaustion 

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec:4.1.101.Final (transitive, pulled by software.amazon.awssdk:s3 at worker/pom.xml:31)
  - io.netty:netty-codec:4.1.101.Final (transitive, pulled by software.amazon.awssdk:s3 at web/pom.xml:35)

Recommended fix:
  - Upgrade io.netty:netty-codec to 4.1.133.Final or later

### CVE-2026-33871: Netty HTTP/2 CONTINUATION Frame Flood DoS via Zero-Byte Frame Bypass
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:35, worker/pom.xml:31

[CVE-2026-33871](https://github.com/advisories/GHSA-w9fj-cfpg-grvv): Netty HTTP/2 CONTINUATION Frame Flood DoS via Zero-Byte Frame Bypass

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http2:4.1.101.Final (transitive, pulled by software.amazon.awssdk:s3 at worker/pom.xml:31)
  - io.netty:netty-codec-http2:4.1.101.Final (transitive, pulled by software.amazon.awssdk:s3 at web/pom.xml:35)

Recommended fix:
  - Upgrade io.netty:netty-codec-http2 to 4.1.132.Final or later

### CVE-2026-33870: Netty: HTTP Request Smuggling via Chunked Extension Quoted-String Parsing
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:35, worker/pom.xml:31

[CVE-2026-33870](https://github.com/advisories/GHSA-pwqr-wmgm-9rr8): Netty: HTTP Request Smuggling via Chunked Extension Quoted-String Parsing

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http:4.1.101.Final (transitive, pulled by software.amazon.awssdk:s3 at worker/pom.xml:31)
  - io.netty:netty-codec-http:4.1.101.Final (transitive, pulled by software.amazon.awssdk:s3 at web/pom.xml:35)

Recommended fix:
  - Upgrade io.netty:netty-codec-http to 4.1.132.Final or later

### CVE-2025-55163: Netty affected by MadeYouReset HTTP/2 DDoS vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:35, worker/pom.xml:31

[CVE-2025-55163](https://github.com/advisories/GHSA-prj3-ccx8-p6x4): Netty affected by MadeYouReset HTTP/2 DDoS vulnerability

Severity: HIGH

Affected dependencies:
  - io.netty:netty-codec-http2:4.1.101.Final (transitive, pulled by software.amazon.awssdk:s3 at worker/pom.xml:31)
  - io.netty:netty-codec-http2:4.1.101.Final (transitive, pulled by software.amazon.awssdk:s3 at web/pom.xml:35)

Recommended fix:
  - Upgrade io.netty:netty-codec-http2 to 4.1.124.Final or later

### CVE-2025-52999: jackson-core can throw a StackoverflowError when processing deeply nested data
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27, worker/pom.xml:45

[CVE-2025-52999](https://github.com/advisories/GHSA-h46c-h94j-95f3): jackson-core can throw a StackoverflowError when processing deeply nested data

Severity: HIGH

Affected dependencies:
  - com.fasterxml.jackson.core:jackson-core:2.13.5 (transitive, pulled by com.fasterxml.jackson.core:jackson-databind at worker/pom.xml:45)
  - com.fasterxml.jackson.core:jackson-core:2.13.5 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)

Recommended fix:
  - Upgrade com.fasterxml.jackson.core:jackson-core to 2.15.0 or later

### CVE-2025-24970: SslHandler doesn't correctly validate packets which can lead to native crash when using native SSLEngine
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:35, worker/pom.xml:31

[CVE-2025-24970](https://github.com/advisories/GHSA-4g8c-wm8x-jfhw): SslHandler doesn't correctly validate packets which can lead to native crash when using native SSLEngine

Severity: HIGH

Affected dependencies:
  - io.netty:netty-handler:4.1.101.Final (transitive, pulled by software.amazon.awssdk:s3 at worker/pom.xml:31)
  - io.netty:netty-handler:4.1.101.Final (transitive, pulled by software.amazon.awssdk:s3 at web/pom.xml:35)

Recommended fix:
  - Upgrade io.netty:netty-handler to 4.1.118.Final or later

### CVE-2023-6481: Logback is vulnerable to an attacker mounting a Denial-Of-Service attack by sending poisoned data
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:23, worker/pom.xml:23

[CVE-2023-6481](https://github.com/advisories/GHSA-gm62-rw4g-vrc4): Logback is vulnerable to an attacker mounting a Denial-Of-Service attack by sending poisoned data

Severity: HIGH

Affected dependencies:
  - ch.qos.logback:logback-core:1.2.12 (transitive, pulled by org.springframework.boot:spring-boot-starter-thymeleaf at web/pom.xml:23)
  - ch.qos.logback:logback-core:1.2.12 (transitive, pulled by org.springframework.boot:spring-boot-starter at worker/pom.xml:23)

Recommended fix:
  - Upgrade ch.qos.logback:logback-core to 1.2.13 or later

### CVE-2023-6378: logback serialization vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:23, worker/pom.xml:23

[CVE-2023-6378](https://github.com/advisories/GHSA-vmq6-5m68-f53m): logback serialization vulnerability

Severity: HIGH

Affected dependencies:
  - ch.qos.logback:logback-core:1.2.12 (transitive, pulled by org.springframework.boot:spring-boot-starter-thymeleaf at web/pom.xml:23)
  - ch.qos.logback:logback-core:1.2.12 (transitive, pulled by org.springframework.boot:spring-boot-starter at worker/pom.xml:23)
  - ch.qos.logback:logback-classic:1.2.12 (transitive, pulled by org.springframework.boot:spring-boot-starter-thymeleaf at web/pom.xml:23)
  - ch.qos.logback:logback-classic:1.2.12 (transitive, pulled by org.springframework.boot:spring-boot-starter at worker/pom.xml:23)

Recommended fix:
  - Upgrade ch.qos.logback:logback-classic to 1.2.13 or later
  - Upgrade ch.qos.logback:logback-core to 1.2.13 or later

### CVE-2026-41284: Apache Tomcat: Unbounded read in WebDAV LOCK and  PROPFIND handling
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27

[CVE-2026-41284](https://github.com/advisories/GHSA-gx5v-xp9w-j4cg): Apache Tomcat: Unbounded read in WebDAV LOCK and  PROPFIND handling

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:9.0.83 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)

Recommended fix:
  - Upgrade org.apache.tomcat.embed:tomcat-embed-core to 9.0.118 or later

### CVE-2026-43512: Apache Tomcat - Digest authenticator will authenticate any unknown user
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27

[CVE-2026-43512](https://github.com/advisories/GHSA-h6fc-48rj-7qqh): Apache Tomcat - Digest authenticator will authenticate any unknown user

Severity: CRITICAL

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:9.0.83 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)

Recommended fix:
  - Upgrade org.apache.tomcat.embed:tomcat-embed-core to 9.0.118 or later

### CVE-2026-43513: Apache Tomcat: LockOutRealm treats user names as case-sensitive
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27

[CVE-2026-43513](https://github.com/advisories/GHSA-5mp6-jrq3-r938): Apache Tomcat: LockOutRealm treats user names as case-sensitive

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:9.0.83 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)

Recommended fix:
  - Upgrade org.apache.tomcat.embed:tomcat-embed-core to 9.0.118 or later

### CVE-2026-43515: Apache Tomcat - Security constraints not correctly applied
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27

[CVE-2026-43515](https://github.com/advisories/GHSA-5m62-pw8w-7w9f): Apache Tomcat - Security constraints not correctly applied

Severity: CRITICAL

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:9.0.83 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)

Recommended fix:
  - Upgrade org.apache.tomcat.embed:tomcat-embed-core to 9.0.118 or later

### CVE-2026-41293: Apache Tomcat - HTTP/2 request headers not validated
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27

[CVE-2026-41293](https://github.com/advisories/GHSA-r29c-68gh-xp6x): Apache Tomcat - HTTP/2 request headers not validated

Severity: CRITICAL

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:9.0.83 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)

Recommended fix:
  - Upgrade org.apache.tomcat.embed:tomcat-embed-core to 9.0.118 or later

### CVE-2026-42498: Apache Tomcat - WebSocket authentication header exposure
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27

[CVE-2026-42498](https://github.com/advisories/GHSA-fv25-8xcx-gqjc): Apache Tomcat - WebSocket authentication header exposure

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:9.0.83 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)

Recommended fix:
  - Upgrade org.apache.tomcat.embed:tomcat-embed-core to 9.0.118 or later

### CVE-2026-34483: Apache Tomcat has an Improper Encoding or Escaping of Output vulnerability in the JsonAccessLogValve
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27

[CVE-2026-34483](https://github.com/advisories/GHSA-rv64-5gf8-9qq8): Apache Tomcat has an Improper Encoding or Escaping of Output vulnerability in the JsonAccessLogValve

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:9.0.83 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)

Recommended fix:
  - Upgrade org.apache.tomcat.embed:tomcat-embed-core to 9.0.116 or later

### CVE-2026-34487: Apache Tomcat vulnerable to Insertion of Sensitive Information into Log File
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27

[CVE-2026-34487](https://github.com/advisories/GHSA-x4m4-345f-5h5g): Apache Tomcat vulnerable to Insertion of Sensitive Information into Log File

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:9.0.83 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)

Recommended fix:
  - Upgrade org.apache.tomcat.embed:tomcat-embed-core to 9.0.117 or later

### CVE-2026-24880: Apache Tomcat has an HTTP Request/Response Smuggling vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27

[CVE-2026-24880](https://github.com/advisories/GHSA-563x-q5rq-57qp): Apache Tomcat has an HTTP Request/Response Smuggling vulnerability

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:9.0.83 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)

Recommended fix:
  - Upgrade org.apache.tomcat.embed:tomcat-embed-core to 9.0.116 or later

### CVE-2026-24734: Apache Tomcat has an Improper Input Validation vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27

[CVE-2026-24734](https://github.com/advisories/GHSA-mgp5-rv84-w37q): Apache Tomcat has an Improper Input Validation vulnerability

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:9.0.83 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)

Recommended fix:
  - Upgrade org.apache.tomcat.embed:tomcat-embed-core to 9.0.115 or later

### CVE-2026-24400: AssertJ has XML External Entity (XXE) vulnerability when parsing untrusted XML via isXmlEqualTo assertion
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:55, worker/pom.xml:40

[CVE-2026-24400](https://github.com/advisories/GHSA-rqfh-9r24-8c9r): AssertJ has XML External Entity (XXE) vulnerability when parsing untrusted XML via isXmlEqualTo assertion

Severity: HIGH

Affected dependencies:
  - org.assertj:assertj-core:3.22.0 (transitive, pulled by org.springframework.boot:spring-boot-starter-test at web/pom.xml:55)
  - org.assertj:assertj-core:3.22.0 (transitive, pulled by org.springframework.boot:spring-boot-starter-test at worker/pom.xml:40)

Recommended fix:
  - Upgrade org.assertj:assertj-core to 3.27.7 or later

### CVE-2025-55752: Apache Tomcat Vulnerable to Relative Path Traversal
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27

[CVE-2025-55752](https://github.com/advisories/GHSA-wmwf-9ccg-fff5): Apache Tomcat Vulnerable to Relative Path Traversal

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:9.0.83 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)

Recommended fix:
  - Upgrade org.apache.tomcat.embed:tomcat-embed-core to 9.0.109 or later

### CVE-2025-48989: Apache Tomcat Improper Resource Shutdown or Release vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27

[CVE-2025-48989](https://github.com/advisories/GHSA-gqp3-2cvr-x8m3): Apache Tomcat Improper Resource Shutdown or Release vulnerability

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:9.0.83 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)

Recommended fix:
  - Upgrade org.apache.tomcat.embed:tomcat-embed-core to 9.0.108 or later

### CVE-2025-53506: Apache Tomcat Coyote vulnerable to Denial of Service via excessive HTTP/2 streams
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27

[CVE-2025-53506](https://github.com/advisories/GHSA-25xr-qj8w-c4vf): Apache Tomcat Coyote vulnerable to Denial of Service via excessive HTTP/2 streams

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:9.0.83 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)

Recommended fix:
  - Upgrade org.apache.tomcat.embed:tomcat-embed-core to 9.0.107 or later

### CVE-2025-52520: Apache Tomcat Catalina is vulnerable to DoS attack through bypassing of size limits
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27

[CVE-2025-52520](https://github.com/advisories/GHSA-wr62-c79q-cv37): Apache Tomcat Catalina is vulnerable to DoS attack through bypassing of size limits

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:9.0.83 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)

Recommended fix:
  - Upgrade org.apache.tomcat.embed:tomcat-embed-core to 9.0.107 or later

### CVE-2025-48988: Apache Tomcat - DoS in multipart upload
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27

[CVE-2025-48988](https://github.com/advisories/GHSA-h3gc-qfqq-6h8f): Apache Tomcat - DoS in multipart upload

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:9.0.83 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)

Recommended fix:
  - Upgrade org.apache.tomcat.embed:tomcat-embed-core to 9.0.106 or later

### CVE-2025-24813: Apache Tomcat: Potential RCE and/or information disclosure and/or information corruption with partial PUT
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27

[CVE-2025-24813](https://github.com/advisories/GHSA-83qj-6fr2-vhqg): Apache Tomcat: Potential RCE and/or information disclosure and/or information corruption with partial PUT

Severity: CRITICAL

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:9.0.83 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)

Recommended fix:
  - Upgrade org.apache.tomcat.embed:tomcat-embed-core to 9.0.99 or later

### CVE-2024-56337: Apache Tomcat Time-of-check Time-of-use (TOCTOU) Race Condition vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27

[CVE-2024-56337](https://github.com/advisories/GHSA-27hp-xhwr-wr2m): Apache Tomcat Time-of-check Time-of-use (TOCTOU) Race Condition vulnerability

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:9.0.83 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)

Recommended fix:
  - Upgrade org.apache.tomcat.embed:tomcat-embed-core to 9.0.98 or later

### CVE-2024-50379: Apache Tomcat Time-of-check Time-of-use (TOCTOU) Race Condition vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27

[CVE-2024-50379](https://github.com/advisories/GHSA-5j33-cvvr-w245): Apache Tomcat Time-of-check Time-of-use (TOCTOU) Race Condition vulnerability

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:9.0.83 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)

Recommended fix:
  - Upgrade org.apache.tomcat.embed:tomcat-embed-core to 9.0.98 or later

### CVE-2024-38286: Apache Tomcat Allocation of Resources Without Limits or Throttling vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27

[CVE-2024-38286](https://github.com/advisories/GHSA-7jqf-v358-p8g7): Apache Tomcat Allocation of Resources Without Limits or Throttling vulnerability

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:9.0.83 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)

Recommended fix:
  - Upgrade org.apache.tomcat.embed:tomcat-embed-core to 9.0.90 or later

### CVE-2024-34750: Apache Tomcat - Denial of Service
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27

[CVE-2024-34750](https://github.com/advisories/GHSA-wm9w-rjj3-j356): Apache Tomcat - Denial of Service

Severity: HIGH

Affected dependencies:
  - org.apache.tomcat.embed:tomcat-embed-core:9.0.83 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)

Recommended fix:
  - Upgrade org.apache.tomcat.embed:tomcat-embed-core to 9.0.90 or later

### CVE-2026-41850: Spring Framework Algorithmic Denial of Service via SpEL Expressions
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27, worker/pom.xml:23

[CVE-2026-41850](https://github.com/advisories/GHSA-r5w3-xv2f-j59q): Spring Framework Algorithmic Denial of Service via SpEL Expressions

Severity: HIGH

Affected dependencies:
  - org.springframework:spring-expression:5.3.31 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)
  - org.springframework:spring-expression:5.3.31 (transitive, pulled by org.springframework.boot:spring-boot-starter at worker/pom.xml:23)

### CVE-2026-41849: Spring Framework Denial of Service via Integer Overflow in SpEL Expressions
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27, worker/pom.xml:23

[CVE-2026-41849](https://github.com/advisories/GHSA-775g-4xr8-78h8): Spring Framework Denial of Service via Integer Overflow in SpEL Expressions

Severity: HIGH

Affected dependencies:
  - org.springframework:spring-expression:5.3.31 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)
  - org.springframework:spring-expression:5.3.31 (transitive, pulled by org.springframework.boot:spring-boot-starter at worker/pom.xml:23)

### CVE-2026-41845: Spring Framework Cross-site Scripting via JavaScriptUtils
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27

[CVE-2026-41845](https://github.com/advisories/GHSA-3chg-m5w7-qfv5): Spring Framework Cross-site Scripting via JavaScriptUtils

Severity: HIGH

Affected dependencies:
  - org.springframework:spring-webmvc:5.3.31 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)

### CVE-2026-41842: Spring Framework Denial of Service via Versioned Resources in Spring MVC and WebFlux
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27

[CVE-2026-41842](https://github.com/advisories/GHSA-x23c-287f-qqv5): Spring Framework Denial of Service via Versioned Resources in Spring MVC and WebFlux

Severity: HIGH

Affected dependencies:
  - org.springframework:spring-webmvc:5.3.31 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)

### CVE-2026-42198: pgjdbc: Unbounded PBKDF2 iterations in SCRAM authentication allows CPU exhaustion DoS
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:64, worker/pom.xml:53

[CVE-2026-42198](https://github.com/advisories/GHSA-98qh-xjc8-98pq): pgjdbc: Unbounded PBKDF2 iterations in SCRAM authentication allows CPU exhaustion DoS

Severity: HIGH

Affected dependencies:
  - org.postgresql:postgresql:42.3.8 (declared at web/pom.xml:64)
  - org.postgresql:postgresql:42.3.8 (declared at worker/pom.xml:53)

Recommended fix:
  - Upgrade org.postgresql:postgresql to 42.7.11 or later

### CVE-2026-40973: Spring Boot accepts predictable temp directory without ownership verification
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:39, worker/pom.xml:23

[CVE-2026-40973](https://github.com/advisories/GHSA-wwpq-f5c3-7hvx): Spring Boot accepts predictable temp directory without ownership verification

Severity: HIGH

Affected dependencies:
  - org.springframework.boot:spring-boot:2.7.18 (transitive, pulled by org.springframework.boot:spring-boot-starter at worker/pom.xml:23)
  - org.springframework.boot:spring-boot:2.7.18 (transitive, pulled by org.springframework.boot:spring-boot-devtools at web/pom.xml:39)

### CVE-2025-41249: Spring Framework annotation detection mechanism may result in improper authorization
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:55, worker/pom.xml:23

[CVE-2025-41249](https://github.com/advisories/GHSA-jmp9-x22r-554x): Spring Framework annotation detection mechanism may result in improper authorization

Severity: HIGH

Affected dependencies:
  - org.springframework:spring-core:5.3.31 (transitive, pulled by org.springframework.boot:spring-boot-starter-test at web/pom.xml:55)
  - org.springframework:spring-core:5.3.31 (transitive, pulled by org.springframework.boot:spring-boot-starter at worker/pom.xml:23)

### CVE-2025-22235: Spring Boot EndpointRequest.to() creates wrong matcher if actuator endpoint is not exposed
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:39, worker/pom.xml:23

[CVE-2025-22235](https://github.com/advisories/GHSA-rc42-6c7j-7h5r): Spring Boot EndpointRequest.to() creates wrong matcher if actuator endpoint is not exposed

Severity: HIGH

Affected dependencies:
  - org.springframework.boot:spring-boot:2.7.18 (transitive, pulled by org.springframework.boot:spring-boot-starter at worker/pom.xml:23)
  - org.springframework.boot:spring-boot:2.7.18 (transitive, pulled by org.springframework.boot:spring-boot-devtools at web/pom.xml:39)

### CVE-2024-38819: Spring Framework Path Traversal vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27

[CVE-2024-38819](https://github.com/advisories/GHSA-g5vr-rgqm-vf78): Spring Framework Path Traversal vulnerability

Severity: HIGH

Affected dependencies:
  - org.springframework:spring-webmvc:5.3.31 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)

### CVE-2024-38816: Path traversal vulnerability in functional web frameworks
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27

[CVE-2024-38816](https://github.com/advisories/GHSA-cx7f-g6mp-7hqm): Path traversal vulnerability in functional web frameworks

Severity: HIGH

Affected dependencies:
  - org.springframework:spring-webmvc:5.3.31 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)

### CVE-2024-22262: Spring Framework URL Parsing with Host Validation
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27

[CVE-2024-22262](https://github.com/advisories/GHSA-2wrp-6fg6-hmc5): Spring Framework URL Parsing with Host Validation

Severity: HIGH

Affected dependencies:
  - org.springframework:spring-web:5.3.31 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)

Recommended fix:
  - Upgrade org.springframework:spring-web to 5.3.34 or later

### CVE-2024-22259: Spring Framework URL Parsing with Host Validation Vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27

[CVE-2024-22259](https://github.com/advisories/GHSA-hgjh-9rj2-g67j): Spring Framework URL Parsing with Host Validation Vulnerability

Severity: HIGH

Affected dependencies:
  - org.springframework:spring-web:5.3.31 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)

Recommended fix:
  - Upgrade org.springframework:spring-web to 5.3.33 or later

### CVE-2024-22243: Spring Web vulnerable to Open Redirect or Server Side Request Forgery
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27

[CVE-2024-22243](https://github.com/advisories/GHSA-ccgv-vj62-xf9h): Spring Web vulnerable to Open Redirect or Server Side Request Forgery

Severity: HIGH

Affected dependencies:
  - org.springframework:spring-web:5.3.31 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)

Recommended fix:
  - Upgrade org.springframework:spring-web to 5.3.32 or later

### CVE-2024-1597: org.postgresql:postgresql vulnerable to SQL Injection via line comment generation
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:64, worker/pom.xml:53

[CVE-2024-1597](https://github.com/advisories/GHSA-24rp-q3w6-vc56): org.postgresql:postgresql vulnerable to SQL Injection via line comment generation

Severity: CRITICAL

Affected dependencies:
  - org.postgresql:postgresql:42.3.8 (declared at web/pom.xml:64)
  - org.postgresql:postgresql:42.3.8 (declared at worker/pom.xml:53)

Recommended fix:
  - Upgrade org.postgresql:postgresql to 42.3.9 or later

### CVE-2016-1000027: Pivotal Spring Framework contains unsafe Java deserialization methods
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:27

[CVE-2016-1000027](https://github.com/advisories/GHSA-4wrc-f8pq-fpqp): Pivotal Spring Framework contains unsafe Java deserialization methods

Severity: CRITICAL

Affected dependencies:
  - org.springframework:spring-web:5.3.31 (transitive, pulled by org.springframework.boot:spring-boot-starter-web at web/pom.xml:27)

Recommended fix:
  - Upgrade org.springframework:spring-web to 6.0.0 or later

### CVE-2026-41716: Spring Data Commons: Heap exhaustion from unbounded property-lookup cache retaining crafted string keys
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:60, worker/pom.xml:49

[CVE-2026-41716](https://github.com/advisories/GHSA-9fw2-h3hf-293r): Spring Data Commons: Heap exhaustion from unbounded property-lookup cache retaining crafted string keys

Severity: HIGH

Affected dependencies:
  - org.springframework.data:spring-data-commons:2.7.18 (transitive, pulled by org.springframework.boot:spring-boot-starter-data-jpa at web/pom.xml:60)
  - org.springframework.data:spring-data-commons:2.7.18 (transitive, pulled by org.springframework.boot:spring-boot-starter-data-jpa at worker/pom.xml:49)

### CVE-2026-41901: Sandboxed Thymeleaf expressions vulnerable to improper recognition of unauthorized syntax patterns
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:23

[CVE-2026-41901](https://github.com/advisories/GHSA-c9ph-gxww-7744): Sandboxed Thymeleaf expressions vulnerable to improper recognition of unauthorized syntax patterns

Severity: CRITICAL

Affected dependencies:
  - org.thymeleaf:thymeleaf:3.0.15.RELEASE (transitive, pulled by org.springframework.boot:spring-boot-starter-thymeleaf at web/pom.xml:23)
  - org.thymeleaf:thymeleaf-spring5:3.0.15.RELEASE (transitive, pulled by org.springframework.boot:spring-boot-starter-thymeleaf at web/pom.xml:23)

Recommended fix:
  - Upgrade org.thymeleaf:thymeleaf to 3.1.5.RELEASE or later
  - Upgrade org.thymeleaf:thymeleaf-spring5 to 3.1.5.RELEASE or later

### CVE-2026-40972: Spring Boot DevTools remote secret comparison is vulnerable to timing attacks
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:39

[CVE-2026-40972](https://github.com/advisories/GHSA-56v8-86gj-66jp): Spring Boot DevTools remote secret comparison is vulnerable to timing attacks

Severity: HIGH

Affected dependencies:
  - org.springframework.boot:spring-boot-devtools:2.7.18 (declared at web/pom.xml:39)

### CVE-2026-40478: Improper neutralization of specific syntax patterns for unauthorized expressions in Thymeleaf
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:23

[CVE-2026-40478](https://github.com/advisories/GHSA-xjw8-8c5c-9r79): Improper neutralization of specific syntax patterns for unauthorized expressions in Thymeleaf

Severity: CRITICAL

Affected dependencies:
  - org.thymeleaf:thymeleaf:3.0.15.RELEASE (transitive, pulled by org.springframework.boot:spring-boot-starter-thymeleaf at web/pom.xml:23)
  - org.thymeleaf:thymeleaf-spring5:3.0.15.RELEASE (transitive, pulled by org.springframework.boot:spring-boot-starter-thymeleaf at web/pom.xml:23)

Recommended fix:
  - Upgrade org.thymeleaf:thymeleaf to 3.1.4.RELEASE or later
  - Upgrade org.thymeleaf:thymeleaf-spring5 to 3.1.4.RELEASE or later

### CVE-2026-40477: Improper restriction of the scope of accessible objects in Thymeleaf expressions
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:23

[CVE-2026-40477](https://github.com/advisories/GHSA-r4v4-5mwr-2fwr): Improper restriction of the scope of accessible objects in Thymeleaf expressions

Severity: CRITICAL

Affected dependencies:
  - org.thymeleaf:thymeleaf:3.0.15.RELEASE (transitive, pulled by org.springframework.boot:spring-boot-starter-thymeleaf at web/pom.xml:23)
  - org.thymeleaf:thymeleaf-spring5:3.0.15.RELEASE (transitive, pulled by org.springframework.boot:spring-boot-starter-thymeleaf at web/pom.xml:23)

Recommended fix:
  - Upgrade org.thymeleaf:thymeleaf to 3.1.4.RELEASE or later
  - Upgrade org.thymeleaf:thymeleaf-spring5 to 3.1.4.RELEASE or later

### CVE-2022-1471: SnakeYaml Constructor Deserialization Remote Code Execution
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:23, worker/pom.xml:23

[CVE-2022-1471](https://github.com/advisories/GHSA-mjmj-j48q-9wg2): SnakeYaml Constructor Deserialization Remote Code Execution

Severity: HIGH

Affected dependencies:
  - org.yaml:snakeyaml:1.30 (transitive, pulled by org.springframework.boot:spring-boot-starter-thymeleaf at web/pom.xml:23)
  - org.yaml:snakeyaml:1.30 (transitive, pulled by org.springframework.boot:spring-boot-starter at worker/pom.xml:23)

Recommended fix:
  - Upgrade org.yaml:snakeyaml to 2.0 or later

### CVE-2022-25857: Uncontrolled Resource Consumption in snakeyaml
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** web/pom.xml:23, worker/pom.xml:23

[CVE-2022-25857](https://github.com/advisories/GHSA-3mc7-4q67-w48m): Uncontrolled Resource Consumption in snakeyaml

Severity: HIGH

Affected dependencies:
  - org.yaml:snakeyaml:1.30 (transitive, pulled by org.springframework.boot:spring-boot-starter-thymeleaf at web/pom.xml:23)
  - org.yaml:snakeyaml:1.30 (transitive, pulled by org.springframework.boot:spring-boot-starter at worker/pom.xml:23)

Recommended fix:
  - Upgrade org.yaml:snakeyaml to 1.31 or later

## CWE Findings (Code-Level Vulnerabilities)

### CWE-477: Use of Obsolete Function
- **Category:** Code Quality
- **Severity:** optional
- **Story Points:** 1
- **Files:** asset-manager/web/src/main/java/com/microsoft/migration/assets/config/WebMvcConfig.java

WebMvcConfig extends deprecated Spring MVC base class WebMvcConfigurerAdapter at line 16 and its nested FileOperationLoggingInterceptor extends deprecated HandlerInterceptorAdapter at line 48; the file even suppresses the deprecation warning at line 15, confirming continued use of obsolete framework APIs.

### CWE-259: Use of Hard-coded Password
- **Category:** Credentials & Secrets
- **Severity:** optional
- **Story Points:** 5
- **Files:** asset-manager/web/src/main/resources/application.properties, asset-manager/worker/src/main/resources/application.properties

Both application.properties files embed outbound service passwords directly in configuration source: web/src/main/resources/application.properties defines spring.rabbitmq.password and spring.datasource.password at lines 17 and 22, and worker/src/main/resources/application.properties defines the same password properties at lines 14 and 19. These are hard-coded passwords shipped with the application source.

### CWE-798: Use of Hard-coded Credentials
- **Category:** Credentials & Secrets
- **Severity:** optional
- **Story Points:** 5
- **Files:** asset-manager/web/src/main/resources/application.properties, asset-manager/worker/src/main/resources/application.properties, asset-manager/web/src/main/java/com/microsoft/migration/assets/config/AwsS3Config.java, asset-manager/worker/src/main/java/com/microsoft/migration/assets/worker/config/AwsS3Config.java

The application source includes embedded service credentials in both application.properties files: AWS access key and secret key entries at web lines 4-5 and worker lines 2-3, plus RabbitMQ/database username-password settings. AwsS3Config in web lines 17-29 and worker lines 17-29 then load these hard-coded credential properties and construct AwsBasicCredentials for outbound authentication.

### CWE-22: Improper Limitation of a Pathname to a Restricted Directory ('Path Traversal')
- **Category:** File & Path Security
- **Severity:** optional
- **Story Points:** 8
- **Files:** asset-manager/web/src/main/java/com/microsoft/migration/assets/controller/S3Controller.java, asset-manager/web/src/main/java/com/microsoft/migration/assets/service/LocalFileStorageService.java

S3Controller.viewObject() and deleteObject() accept user-controlled @PathVariable key at lines 79-81 and 96-99, then LocalFileStorageService.getObject()/deleteObject() resolve that key directly against rootLocation at lines 109-124 without canonical containment checks, allowing path traversal outside the intended storage directory when crafted path elements are supplied.

### CWE-23: Relative Path Traversal
- **Category:** File & Path Security
- **Severity:** optional
- **Story Points:** 5
- **Files:** asset-manager/web/src/main/java/com/microsoft/migration/assets/controller/S3Controller.java, asset-manager/web/src/main/java/com/microsoft/migration/assets/service/LocalFileStorageService.java, asset-manager/worker/src/main/java/com/microsoft/migration/assets/worker/service/LocalFileProcessingService.java

S3Controller forwards user-controlled key values from viewObject()/deleteObject() (lines 79-81 and 96-99) to LocalFileStorageService, which calls rootLocation.resolve(key) in getObject()/deleteObject() at lines 109-124 with no '..' validation. LocalFileProcessingService.downloadOriginal() and uploadThumbnail() likewise resolve message-supplied keys at lines 37-49, so relative traversal sequences can escape the storage root.

### CWE-36: Absolute Path Traversal
- **Category:** File & Path Security
- **Severity:** optional
- **Story Points:** 5
- **Files:** asset-manager/web/src/main/java/com/microsoft/migration/assets/service/LocalFileStorageService.java, asset-manager/worker/src/main/java/com/microsoft/migration/assets/worker/service/LocalFileProcessingService.java

LocalFileStorageService.uploadObject() only rejects '..' after cleanPath() at lines 89-95, then passes filename into rootLocation.resolve(filename); an absolute filename causes Path.resolve() to ignore rootLocation and target that absolute path. The same missing absolute-path validation appears in LocalFileProcessingService.downloadOriginal()/uploadThumbnail() at lines 37-49 when resolving message keys.

### CWE-434: Unrestricted Upload of File with Dangerous Type
- **Category:** File & Path Security
- **Severity:** mandatory
- **Story Points:** 8
- **Files:** asset-manager/web/src/main/java/com/microsoft/migration/assets/controller/S3Controller.java, asset-manager/web/src/main/java/com/microsoft/migration/assets/service/LocalFileStorageService.java, asset-manager/web/src/main/java/com/microsoft/migration/assets/service/AwsS3Service.java, asset-manager/worker/src/main/java/com/microsoft/migration/assets/worker/service/AbstractFileProcessingService.java

S3Controller.uploadObject() accepts any MultipartFile at lines 40-49 and delegates without extension or MIME allowlisting. LocalFileStorageService.uploadObject() stores the file and enqueues processing at lines 84-105, AwsS3Service.uploadObject() uploads any file/contentType to S3 at lines 68-85, and AbstractFileProcessingService.processImage() automatically downloads and processes queued uploads at lines 24-50.

### CWE-99: Improper Control of Resource Identifiers ('Resource Injection')
- **Category:** Injection Attacks
- **Severity:** potential
- **Story Points:** 3
- **Files:** asset-manager/web/src/main/java/com/microsoft/migration/assets/controller/S3Controller.java, asset-manager/web/src/main/java/com/microsoft/migration/assets/service/LocalFileStorageService.java, asset-manager/worker/src/main/java/com/microsoft/migration/assets/worker/service/LocalFileProcessingService.java

S3Controller.viewObject() and deleteObject() accept user-controlled @PathVariable key values at lines 79-81 and 96-99, then LocalFileStorageService.getObject()/deleteObject() use rootLocation.resolve(key) at lines 109-124 and LocalFileProcessingService.downloadOriginal()/uploadThumbnail() use rootLocation.resolve(key) at lines 37-49, treating upstream input directly as a filesystem resource identifier without restricting it to intended objects.

