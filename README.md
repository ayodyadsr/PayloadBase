![Project logo](/.github/PayloadBase.png)

### About PayloadBase

PayloadBase is a structured collection of security testing payloads organized for practical use by researchers and bug hunters. Each category contains focused `.txt` files covering attack variants, bypass techniques, and exploitation patterns — ready to use with Burp Suite, ffuf, nuclei, or manual testing.

Maintained by [ayodyadsr](https://github.com/ayodyadsr)

---

### Repository Details

[![Repo size](https://img.shields.io/github/repo-size/ayodyadsr/PayloadBase.svg)](https://github.com/ayodyadsr/PayloadBase)
[![Last commit](https://img.shields.io/github/last-commit/ayodyadsr/PayloadBase.svg)](https://github.com/ayodyadsr/PayloadBase)
[![License](https://img.shields.io/github/license/ayodyadsr/PayloadBase.svg)](https://github.com/ayodyadsr/PayloadBase)

**329 payload files · 61 categories**

---

### Installation

**Zip**
```bash
wget -c https://github.com/ayodyadsr/PayloadBase/archive/main.zip -O PayloadBase.zip && unzip PayloadBase.zip && rm -f PayloadBase.zip
```

**Git (shallow clone)**
```bash
git clone --depth 1 https://github.com/ayodyadsr/PayloadBase.git
```

**Git (full history)**
```bash
git clone https://github.com/ayodyadsr/PayloadBase.git
```

---

### Categories

#### Injection

| Category | Files | Description |
|---|---|---|
| `Command Injection` | 20 | Unix/Windows command injection — basic, chaining, filter bypass, OOB, time-based, context-specific |
| `CRLF` | 3 | CRLF Injection — header injection, redirect injection, response splitting |
| `CSV Injection` | 1 | Formula injection (DDE) for Excel/Google Sheets |
| `CSS Injection` | 2 | Style injection, attribute selector exfiltration, CSS keylogger |
| `LDAP Injection` | 3 | Authentication bypass, blind extraction, filter escape and OID injection |
| `LaTeX Injection` | 2 | File read via `\input`, RCE via `\write18`, SSRF |
| `Nosqli` | 3 | MongoDB operator injection, Redis/CouchDB/Elasticsearch attacks |
| `Prompt Injection` | 4 | Direct injection, indirect via documents/emails, jailbreaks, system prompt extraction |
| `SAML Injection` | 2 | XML signature wrapping (XSW), XXE in SAML, attribute injection, condition bypass |
| `Server Side Include Injection` | 1 | SSI `exec`, `include`, `printenv` — file read and RCE |
| `SQL Injection` | 9 | Time-based, boolean, error-based, OOB, WAF bypass; per-database: MySQL, MSSQL, PostgreSQL, Oracle, SQLite |
| `SSTI` | 1 | Jinja2, Twig, Freemarker, Velocity, Pebble, ERB, Smarty, Mako, Handlebars, EJS, Nunjucks |
| `XPATH Injection` | 2 | Authentication bypass, blind data extraction via XPath functions |
| `XSLT Injection` | 2 | SSRF via `document()`, RCE via Saxon/Xalan/MSXSL/PHP |
| `XXE` | 1 | File read, SSRF, blind OOB, XInclude, SVG, SOAP, PHP filters |

#### Client-Side

| Category | Files | Description |
|---|---|---|
| `Clickjacking` | 1 | iframe PoC templates, sandbox bypass, reverse tabnabbing |
| `CORS Misconfiguration` | 3 | Origin reflection attack, bypass techniques, CORS headers for test/PoC |
| `CSRF` | 3 | Token bypass techniques, SameSite tricks, HTML/JS PoC templates |
| `DOM Clobbering` | 2 | Global variable override, multi-level clobbering, CSP bypass, anchor href abuse |
| `Prototype Pollution` | 1 | Client-side and Node.js server-side prototype pollution |
| `Tabnabbing` | 1 | `window.opener` abuse, delayed redirect, reverse tabnabbing |
| `XS-Leak` | 1 | Frame count oracle, history API, onload/onerror oracle, CSS `:visited`, timing oracle |
| `XSS` | 15 | Reflected, stored, DOM, blind, polyglot, CSP bypass, Angular template injection, event handlers, exfiltration |

#### Access Control & IDOR

| Category | Files | Description |
|---|---|---|
| `Account Takeover` | 3 | Password reset poisoning, token/session hijacking, OAuth-based ATO |
| `Brute Force Rate Limit` | 3 | IP spoofing headers, OTP bypass, password spray wordlist |
| `IDOR` | 20 | Numeric IDs, UUID variants, object-specific IDs, parameter pollution, GraphQL IDOR |
| `Mass Assignment` | 2 | Common privilege escalation parameters, framework-specific (Rails, Laravel, Django, Spring, Express) |
| `ORM Leak` | 2 | Django ORM filter traversal, Rails ActiveRecord ransack/scope injection |

#### Authentication

| Category | Files | Description |
|---|---|---|
| `JWT` | 9 | Weak secrets, `alg:none`, RS256→HS256 confusion, framework defaults |
| `OAuth` | 13 | Core endpoints, SAML, social login callbacks, `.well-known`, token management, PKCE bypass |

#### Injection via File / Upload

| Category | Files | Description |
|---|---|---|
| `LFI` | 8 | Path traversal, null byte bypass, Windows LFI, RFI, log poisoning, LFI-to-RCE |
| `Directory Traversal` | 3 | Unix/Windows path traversal, encoding bypass (URL, double, unicode, null byte) |
| `Upload Insecure Files` | 5 | Extension bypass, MIME type bypass, magic bytes polyglot, web shells, path traversal via filename |
| `Zip Slip` | 1 | Malicious archive path traversal — `.zip`, `.tar`, `.jar`; Python creation scripts |

#### Server-Side Attacks

| Category | Files | Description |
|---|---|---|
| `Insecure Deserialization` | 5 | Java ysoserial gadgets, PHP PHPGGC, Python pickle, .NET BinaryFormatter, Node.js node-serialize |
| `Race Condition` | 3 | Concurrent request patterns, HTTP/2 single-packet attack, TOCTOU patterns |
| `Request Smuggling` | 4 | CL.TE, TE.CL, TE.TE obfuscation, HTTP/2 downgrade (H2.CL/H2.TE) |
| `SSRF` | 23 | Cloud metadata (AWS/GCP/Azure/Alibaba/DO/Oracle), bypass, internal services, Kubernetes, Redis, DNS rebinding |

#### Infrastructure & Configuration

| Category | Files | Description |
|---|---|---|
| `Bypass` | 22 | WAF bypass — Cloudflare, Akamai, ModSecurity, F5 ASM; method override, header tricks |
| `DNS Rebinding` | 1 | Attack flow, rebinding JS payload, Singularity framework, internal service targets |
| `Insecure Management Interface` | 1 | Admin panel paths, framework-specific consoles, monitoring tools, DB admin interfaces |
| `Insecure Source Code Management` | 2 | Git directory exposure, SVN/Mercurial/CVS paths, CI/CD config files, backup files |
| `Reverse Proxy Misconfigurations` | 2 | Nginx off-by-slash, path normalization bypass, internal access via header abuse |
| `Virtual Hosts` | 1 | VHost discovery wordlist — internal, cloud, environment-specific subdomains |

#### API & Modern Web

| Category | Files | Description |
|---|---|---|
| `API` | 13 | API key testing, versioning bypass, content-type confusion, mass assignment, discovery |
| `API Key Leaks` | 2 | Regex patterns for AWS/GCP/GitHub/Stripe/OpenAI/Slack; common leak locations (git, configs, bundles) |
| `GraphQL` | 24 | Endpoint paths, introspection bypass, query/mutation names, sensitive fields, type names, DoS |
| `HTTP Parameter Pollution` | 2 | Duplicate parameter behavior per server, prototype pollution via HPP, WAF bypass |
| `Web Cache Deception` | 2 | Path manipulation (static extension append), cache poisoning via unkeyed headers |
| `Web Sockets` | 2 | CSWSH, header injection in handshake, message injection, SSRF/SQLi via WS |

#### Business Logic

| Category | Files | Description |
|---|---|---|
| `Business Logic Errors` | 3 | Price/payment manipulation, currency confusion, workflow bypass, 2FA skip, replay attacks |
| `Hidden Params` | 20 | Debug flags, admin escalation, role injection, price manipulation, framework-specific (Django, Express, Laravel, Rails, Spring, WordPress) |
| `Open Redirect` | 3 | Protocol bypass, @ tricks, domain confusion, URL encoding bypass, common parameter names |

#### Encoding & Format

| Category | Files | Description |
|---|---|---|
| `Encoding Transformations` | 2 | URL encoding, double encoding, unicode normalization, homoglyphs, HTML entities, Base64/Hex for WAF bypass |
| `Mutation` | 1 | Mutation payloads — XSS (Cloudflare/ModSecurity), SQLi encoding, path traversal variants |
| `Polyglot` | 14 | Multi-context payloads combining XSS/HTML/JS/SSTI/SQLi/LFI |
| `Type Juggling` | 2 | PHP loose comparison (`==`), magic hash values, `strcmp()` bypass; JavaScript type coercion |

#### Mobile

| Category | Files | Description |
|---|---|---|
| `Mobile` | 19 | Base paths, push endpoints, deep links, versioning, IAP, user agents, sync, device management |

#### Miscellaneous

| Category | Files | Description |
|---|---|---|
| `CORS Misconfiguration` | 3 | *(see Client-Side)* |
| `Dependency Confusion` | 1 | Internal package name discovery, malicious package upload strategy (npm/pip/gem) |
| `Denial of Service` | 2 | ReDoS patterns, XML billion laughs, GraphQL depth attack, hash collision, zip bomb, slowloris |
| `Insecure Randomness` | 1 | Weak PRNG patterns, UUID v1 analysis, PHP `mt_rand()` prediction, time-based token brute force |

---

### Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change or add.

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

### ⚠️ Disclaimer

This repository is intended for educational purposes and authorized security testing only. Only use these payloads against systems you own or have explicit written permission to test. Unauthorized use is strictly prohibited. The maintainer assumes no liability for misuse.

---

### License

This project is licensed under the [MIT License](LICENSE).

[![MIT License](https://img.shields.io/badge/license-MIT-blue)](https://opensource.org/licenses/MIT)
