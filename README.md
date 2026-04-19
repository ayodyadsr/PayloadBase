![Project logo](/.github/PayloadBase.png)

### About PayloadBase

PayloadBase is a collection of payloads. It is organized and easy to use, making it a practical resource for researchers and bug hunters. Everything is arranged in a simple and clear way, so it is easy to browse, find, and use. It is designed to be straightforward and useful for anyone who needs it.

Maintained by [ayodyadsr](https://github.com/ayodyadsr)

---

### Repository Details

[![Repo size](https://img.shields.io/github/repo-size/ayodyadsr/PayloadBase.svg)](https://github.com/ayodyadsr/PayloadBase)
[![Last commit](https://img.shields.io/github/last-commit/ayodyadsr/PayloadBase.svg)](https://github.com/ayodyadsr/PayloadBase)
[![License](https://img.shields.io/github/license/ayodyadsr/PayloadBase.svg)](https://github.com/ayodyadsr/PayloadBase)

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

| Category | Description |
|---|---|
| `API` | API and JSON fuzzing payloads |
| `Business Logic` | Business logic abuse — workflow bypass, price manipulation, state tampering |
| `Bypass` | WAF and filter bypass techniques — method override, header tricks |
| `Command Injection` | Command Injection — Unix, Windows, blind OOB |
| `CRLF` | CRLF Injection — header injection, response splitting |
| `CSRF` | CSRF — token bypass, SameSite tricks |
| `GraphQL` | GraphQL endpoint paths, query/mutation names, sensitive field names, type names, introspection bypass |
| `Hidden Params` | Debug flags, admin escalation, role injection, price manipulation, validation bypass, framework-specific |
| `IDOR` | IDOR — numeric IDs, UUID variants, object-specific IDs, parameter pollution patterns, indirect reference fields |
| `JWT` | JWT — weak secrets, framework defaults, language-specific, year-based patterns |
| `LFI` | Local/Remote File Inclusion — path traversal, null byte bypass, Windows |
| `Mobile` | Mobile attack surface — base paths, push endpoints, deep links, versioning, IAP, sync |
| `Mutation` | Mutation payloads — XSS (Cloudflare/ModSecurity), SQLi encoding, path traversal variants, CMDi, HTTP smuggling |
| `Nosqli` | NoSQL Injection — MongoDB, CouchDB, operator injection |
| `OAuth` | OAuth2/OIDC — core endpoints, SAML, social login callbacks, .well-known, token management |
| `Open Redirect` | Open Redirect — protocol bypass, @ tricks, header injection |
| `Polyglot` | Polyglot payloads — multi-context execution (XSS, HTML, JS) |
| `Prototype Pollution` | Prototype Pollution — client-side and Node.js server-side |
| `Race Condition` | Race condition — concurrent requests, state desynchronization, double-spend |
| `SQL Injection` | SQL Injection — time-based, boolean, error-based, OOB, WAF bypass |
| `SSRF` | Server-Side Request Forgery — cloud metadata, bypass, internal services |
| `SSTI` | Server-Side Template Injection — Jinja2, Twig, Freemarker, ERB, Pebble |
| `XSS` | Cross-Site Scripting — reflected, stored, DOM, blind, polyglot |
| `XXE` | XML External Entity — file read, SSRF, blind OOB, bypass |

---

### Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change or add.

---

### ⚠️ Disclaimer

This repository is intended for educational purposes and authorized security testing only. Unauthorized use is strictly prohibited. The maintainer assumes no liability for misuse.

---

### License

This project is licensed under the [MIT License](LICENSE).

[![MIT License](https://img.shields.io/badge/license-MIT-blue)](https://opensource.org/licenses/MIT)
