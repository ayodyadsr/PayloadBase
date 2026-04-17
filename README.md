![Project logo](/.github/PayloadBase.png)

### About PayloadBase

PayloadBase is a modern payload arsenal for bug hunters — focused on APIs, GraphQL, business logic, and WAF bypass. The repository covers a wide range of vulnerabilities including API and JSON fuzzing, WAF bypass techniques, injection classes (SQLi, NoSQLi, SSTI, CMDi), client-side attacks (XSS, prototype pollution), access control issues, and modern application attack vectors across web, mobile, and distributed systems.

This project is maintained by [ayodyadsr](https://github.com/ayodyadsr).

- - -

### Repository details

[![Repo size](https://img.shields.io/github/repo-size/ayodyadsr/PayloadBase.svg)](https://github.com/ayodyadsr/PayloadBase)
[![Last commit](https://img.shields.io/github/last-commit/ayodyadsr/PayloadBase.svg)](https://github.com/ayodyadsr/PayloadBase)
[![License](https://img.shields.io/github/license/ayodyadsr/PayloadBase.svg)](https://github.com/ayodyadsr/PayloadBase)

- - -

### Install

**Zip**
```bash
wget -c https://github.com/ayodyadsr/PayloadBase/archive/main.zip -O PayloadBase.zip && unzip PayloadBase.zip && rm -f PayloadBase.zip
```
 
**Git — No commit history (faster)**
```bash
git clone --depth 1 https://github.com/ayodyadsr/PayloadBase.git
```
 
**Git — Complete**
```bash
git clone https://github.com/ayodyadsr/PayloadBase.git
```

- - -

### Categories

| Category | Description |
|---|---|
| `api/` | API and JSON fuzzing payloads |
| `business_logic/` | Business logic abuse — workflow bypass, price manipulation, state tampering |
| `bypass/` | WAF and filter bypass techniques — method override, header tricks |
| `cmdi/` | Command Injection — Unix, Windows, blind OOB |
| `crlf/` | CRLF Injection — header injection, response splitting |
| `csrf/` | CSRF — token bypass, SameSite tricks |
| `graphql/` | GraphQL endpoint paths, query/mutation names, sensitive field names, type names, introspection bypass |
| `hidden_params/` | Debug flags, admin escalation, role injection, price manipulation, validation bypass, framework-specific |
| `idor/` | IDOR — numeric IDs, UUID variants, object-specific IDs, parameter pollution patterns, indirect reference fields |
| `jwt/` | JWT — weak secrets, framework defaults, language-specific, year-based patterns |
| `lfi/` | Local/Remote File Inclusion — path traversal, null byte bypass, Windows |
| `mobile/` | Mobile attack surface — base paths, push endpoints, deep links, versioning, IAP, sync |
| `mutation/` | Mutation payloads — XSS (Cloudflare/ModSecurity), SQLi encoding, path traversal variants, CMDi, HTTP smuggling |
| `nosqli/` | NoSQL Injection — MongoDB, CouchDB, operator injection |
| `oauth/` | OAuth2/OIDC — core endpoints, SAML, social login callbacks, .well-known, token management |
| `open_redirect/` | Open Redirect — protocol bypass, @ tricks, header injection |
| `polyglot/` | Polyglot payloads — multi-context execution (XSS, HTML, JS) |
| `prototype_pollution/` | Prototype Pollution — client-side and Node.js server-side |
| `race_condition/` | Race condition — concurrent requests, state desynchronization, double-spend |
| `sqli/` | SQL Injection — time-based, boolean, error-based, OOB, WAF bypass |
| `ssrf/` | Server-Side Request Forgery — cloud metadata, bypass, internal services |
| `ssti/` | Server-Side Template Injection — Jinja2, Twig, Freemarker, ERB, Pebble |
| `xss/` | Cross-Site Scripting — reflected, stored, DOM, blind, polyglot |
| `xxe/` | XML External Entity — file read, SSRF, blind OOB, bypass |

- - -

### Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change or add.

- - -

### ⚠️ Disclaimer

This repository is intended for **educational purposes and authorized security testing only**. Use of these payloads against systems you do not own or have explicit written permission to test is illegal and unethical. The maintainer assumes no liability for misuse.

- - -

### Licensing

This project is licensed under the [MIT License](LICENSE).

[![MIT License](https://img.shields.io/badge/license-MIT-blue)](https://opensource.org/licenses/MIT)
