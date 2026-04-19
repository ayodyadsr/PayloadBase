![PayloadBase](.github/PayloadBase.png)
 
### About PayloadBase

A focused payload collection for web application security testing.
Organized by vulnerability class load any file directly into Burp, ffuf, or nuclei and gobuster.

Maintained by [ayodyadsr](https://github.com/ayodyadsr)

- - -

### Repository Details

![Repo size](https://img.shields.io/github/repo-size/ayodyadsr/PayloadBase.svg)
[![Last commit](https://img.shields.io/github/last-commit/ayodyadsr/PayloadBase.svg)](https://github.com/ayodyadsr/PayloadBase/commits/main)
[![License](https://img.shields.io/github/license/ayodyadsr/PayloadBase.svg)](LICENSE)

- - -

### Install

**Zip**
```bash
wget -c https://github.com/ayodyadsr/PayloadBase/archive/main.zip -O PayloadBase.zip && unzip PayloadBase.zip && rm -f PayloadBase.zip
```

**Git (shallow)**
```bash
git clone --depth 1 https://github.com/ayodyadsr/PayloadBase.git
```

**Git (full)**
```bash
git clone https://github.com/ayodyadsr/PayloadBase.git
```

- - -

### Categories

**Injection**

| Category | Description |
|---|---|
| `Command Injection` | Unix/Windows — basic, chaining, OOB, time-based, filter bypass, context-specific |
| `CRLF` | Header injection, redirect injection, response splitting |
| `CSV Injection` | Formula injection (DDE) targeting Excel and Google Sheets |
| `CSS Injection` | Property injection, `@import` SSRF, attribute selector-based data exfiltration |
| `LDAP Injection` | Authentication bypass, blind character extraction, filter escape |
| `LaTeX Injection` | File read via `\input`, RCE via `\write18`, SSRF via `document()` |
| `Nosqli` | MongoDB operator injection, Redis/CouchDB/Elasticsearch payloads |
| `Prompt Injection` | Direct, indirect (document/email), jailbreaks, system prompt extraction |
| `SAML Injection` | XML signature wrapping (XSW), XXE in SAML response, attribute and condition tampering |
| `Server Side Include Injection` | `exec`, `include`, `printenv` — file read and RCE via SSI directives |
| `SQL Injection` | Boolean, time-based, error-based, OOB, WAF bypass; per-database: MySQL, MSSQL, PostgreSQL, Oracle, SQLite |
| `SSTI` | Jinja2, Twig, Freemarker, Velocity, Pebble, ERB, Smarty, Mako, Handlebars, EJS, Nunjucks |
| `XPATH Injection` | Authentication bypass, blind extraction via XPath string functions |
| `XSLT Injection` | SSRF via `document()`, RCE via Saxon, Xalan, MSXSL, PHP `registerPHPFunctions` |
| `XXE` | File read, SSRF, blind OOB, XInclude, SVG/SOAP vectors, PHP filter chains |

**Client-Side**

| Category | Description |
|---|---|
| `Clickjacking` | Transparent iframe PoC, sandbox bypass, reverse tabnabbing |
| `CORS Misconfiguration` | Origin reflection, bypass techniques, dangerous header combinations |
| `CSRF` | Token bypass, SameSite tricks, HTML/fetch/multipart PoC templates |
| `DOM Clobbering` | Global variable override, multi-level clobbering via `form+input`, CSP bypass |
| `Prototype Pollution` | Client-side and Node.js server-side gadgets |
| `Tabnabbing` | `window.opener` abuse, delayed redirect, opener document write |
| `XS-Leak` | Frame count oracle, history API, `onload/onerror` oracle, timing, postMessage |
| `XSS` | Reflected, stored, DOM, blind, polyglot, CSP bypass, Angular template, exfiltration |

**Access Control**

| Category | Description |
|---|---|
| `Account Takeover` | Password reset poisoning, token/session hijacking, OAuth-based ATO, 2FA bypass |
| `Brute Force Rate Limit` | IP spoofing headers, OTP bypass, password spray wordlist |
| `IDOR` | Numeric IDs, UUID variants, object-specific IDs, parameter pollution, GraphQL IDOR |
| `Mass Assignment` | Privilege escalation parameters, framework-specific payloads (Rails, Laravel, Django, Spring) |
| `ORM Leak` | Django filter traversal, Rails ActiveRecord ransack/scope injection |

**Authentication**

| Category | Description |
|---|---|
| `JWT` | Weak secrets, `alg:none`, RS256→HS256 confusion, framework defaults, breach lists |
| `OAuth` | Core endpoints, SAML, social login callbacks, `.well-known`, token management, PKCE bypass |

**File & Upload**

| Category | Description |
|---|---|
| `Directory Traversal` | Unix/Windows path traversal, encoding bypass (URL, double-URL, unicode, null byte) |
| `LFI` | Path traversal, null byte bypass, Windows LFI, RFI, log poisoning, LFI-to-RCE chains |
| `Upload Insecure Files` | Extension bypass, MIME type spoofing, magic bytes polyglot, web shells, path traversal via filename |
| `Zip Slip` | Malicious `.zip`/`.tar`/`.jar` — overwrites files outside extraction directory |

**Server-Side**

| Category | Description |
|---|---|
| `Insecure Deserialization` | Java ysoserial gadgets, PHP PHPGGC, Python pickle, .NET BinaryFormatter, Node.js node-serialize |
| `Race Condition` | HTTP/2 single-packet attack, Turbo Intruder patterns, TOCTOU scenarios |
| `Request Smuggling` | CL.TE, TE.CL, TE.TE obfuscation, HTTP/2 downgrade (H2.CL / H2.TE) |
| `SSRF` | Cloud metadata (AWS/GCP/Azure/DO/Oracle/Alibaba), bypass, internal services, Kubernetes, Redis |

**Infrastructure**

| Category | Description |
|---|---|
| `Bypass` | WAF bypass — Cloudflare, Akamai, ModSecurity, F5 ASM; method override, header tricks |
| `DNS Rebinding` | Attack flow, JS payload, Singularity framework reference, internal service targets |
| `Insecure Management Interface` | Admin panel paths, framework consoles (Actuator, phpMyAdmin), monitoring tools |
| `Insecure Source Code Management` | Git/SVN/Mercurial exposure paths, CI/CD config files, backup files |
| `Reverse Proxy Misconfigurations` | Nginx off-by-slash, path normalization, internal access via header abuse |
| `Virtual Hosts` | VHost discovery wordlist — internal, cloud, and environment-specific subdomains |

**API & Modern Web**

| Category | Description |
|---|---|
| `API` | Key testing, versioning bypass, content-type confusion, mass assignment, endpoint discovery |
| `API Key Leaks` | Regex patterns (AWS, GCP, GitHub, Stripe, OpenAI, Slack); common leak locations |
| `GraphQL` | Endpoint paths, introspection bypass, query/mutation names, sensitive fields, DoS |
| `HTTP Parameter Pollution` | Duplicate parameter behavior across servers, prototype pollution via HPP, WAF bypass |
| `Web Cache Deception` | Static extension path manipulation, cache poisoning via unkeyed headers |
| `Web Sockets` | CSWSH PoC, handshake header injection, SQLi/SSRF/XSS via WebSocket message |

**Business Logic**

| Category | Description |
|---|---|
| `Business Logic Errors` | Price manipulation, currency confusion, workflow bypass, replay attacks, 2FA skip |
| `Hidden Params` | Debug flags, admin escalation, role injection, framework-specific parameters |
| `Open Redirect` | Protocol bypass, @ tricks, domain confusion, encoding bypass, parameter name wordlist |

**Encoding & Format**

| Category | Description |
|---|---|
| `Encoding Transformations` | URL encoding, double encoding, unicode normalization, homoglyphs, HTML entities, Base64/Hex |
| `Mutation` | XSS (Cloudflare/ModSecurity), SQLi encoding, path traversal variants, HTTP smuggling |
| `Polyglot` | Multi-context payloads combining XSS/HTML/JS/SSTI/SQLi/LFI |
| `Type Juggling` | PHP loose comparison magic hashes, `strcmp()` bypass; JavaScript type coercion |

**Mobile**

| Category | Description |
|---|---|
| `Mobile` | Base paths, push endpoints, deep links, versioning, IAP, user agents, sync, device management |

**Miscellaneous**

| Category | Description |
|---|---|
| `Dependency Confusion` | Internal package name discovery, malicious postinstall strategy (npm/pip/gem) |
| `Denial of Service` | ReDoS patterns, XML billion laughs, GraphQL depth DoS, hash collision, zip bomb |
| `Insecure Randomness` | Weak PRNG patterns, UUID v1 analysis, PHP `mt_rand()` prediction, time-based token brute force |

- - -

### Contributing

Pull requests are welcome. Open an issue first for major additions or structural changes.

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

- - -

### Disclaimer

For authorized security testing and educational use only. Only test systems you own or have explicit written permission to assess. The maintainer takes no responsibility for misuse.

- - -

### License

[MIT](LICENSE)
