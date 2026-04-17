![Project logo](/.github/PayloadBase.png)

### About PayloadBase

PayloadBase is a structured payload arsenal designed for security researchers and bug hunters, built around real-world attack surfaces and organized by vulnerability classes. The repository includes categorized payloads for API testing, GraphQL, SQL injection, XSS, SSRF, LFI, command injection, IDOR, JWT weaknesses, OAuth, hidden parameters, mobile-specific vectors, and WAF bypass techniques.

This project is maintained by [ayodyadsr](https://github.com/ayodyadsr).

- - -

### Repository details

![Repo size](https://img.shields.io/github/repo-size/ayodyadsr/PayloadBase.svg)
![Last commit](https://img.shields.io/github/last-commit/ayodyadsr/PayloadBase.svg)
![License](https://img.shields.io/github/license/ayodyadsr/PayloadBase.svg)

- - -

### Install

**Zip**

```
wget -c https://github.com/ayodyadsr/PayloadBase/archive/main.zip -O PayloadBase.zip && unzip PayloadBase.zip && rm -f PayloadBase.zip
```

**Git: No commit history (faster)**

```
git clone --depth 1 https://github.com/ayodyadsr/PayloadBase.git
```

**Git: Complete**

```
git clone https://github.com/ayodyadsr/PayloadBase.git
```

- - -

### Categories

| Category | Description |
|---|---|
| `sqli/` | SQL Injection — time-based, boolean, error-based, OOB, WAF bypass |
| `xss/` | Cross-Site Scripting — reflected, stored, DOM, blind, polyglot |
| `ssrf/` | Server-Side Request Forgery — cloud metadata, bypass, internal ports |
| `lfi/` | Local/Remote File Inclusion — path traversal, null byte, Windows |
| `cmdi/` | Command Injection — Unix, Windows, blind OOB |
| `xxe/` | XML External Entity — file read, SSRF, blind OOB, bypass |
| `ssti/` | Server-Side Template Injection — Jinja2, Twig, Freemarker, ERB, Pebble |
| `open_redirect/` | Open Redirect — protocol bypass, @-based, header injection |
| `nosqli/` | NoSQL Injection — MongoDB, CouchDB, operator injection |
| `crlf/` | CRLF Injection — header injection, response splitting |
| `csrf/` | CSRF — token bypass, SameSite tricks |
| `prototype_pollution/` | Prototype Pollution — client-side, server-side (Node.js) |
| `api/` | API and JSON fuzzing payloads |
| `polyglot/` | Multi-context polyglot payloads |
| `mutation/` | WAF bypass mutation payloads XSS (Cloudflare/ModSec), SQLi encoding, path traversal variants, CMDi, HTTP smuggling headers |
| `graphql/` | GraphQL Endpoint paths, query/mutation names, field names sensitif, type names, introspection bypass |
| `jwt/` | JWT Weak secrets, framework defaults, language-specific, year-based patterns |
| `idor/` | IDOR Numeric IDs, UUID variants, object-specific IDs, parameter pollution patterns, indirect ref fields |
| `oauth/` | OAuth2/OIDC core endpoints, SAML, social login callbacks, .well-known, token management |
| `hidden_params/` | Debug flags, admin escalation, role injection, price manipulation, validation bypass, framework-specific |
| `mobile/` | Mobile base paths, push notification endpoints, deep links, version check, IAP, sync |

- - -

### Usage

**ffuf**

```bash
ffuf -u https://target.com/FUZZ -w xss/basic.txt
```

**Burp Suite Intruder**

```
Load any .txt file directly as Intruder payload list.
```

**SQLMap — HTTP GET**

```bash
sqlmap -u "https://target.com/page?id=1" --technique=T --time-sec=10 --level=3 --risk=1
```

**SQLMap — HTTP POST**

```bash
sqlmap -r /tmp/target.txt --technique=T --time-sec=10 --level=3 --risk=1
```

**SQLMap — HTTP Header injection**

```bash
sqlmap -u "https://target.com/page" --technique=T --time-sec=10 --level=5 --risk=3 -p "User-Agent" --random-agent
```

**SQLMap — WAF Bypass**

```bash
sqlmap -u "https://target.com/page?id=1" --technique=T --time-sec=10 --tamper=space2comment,between,randomcase
```

- - -

### Similar Projects

- [SecLists](https://github.com/danielmiessler/SecLists): The security tester's companion — usernames, passwords, URLs, fuzzing payloads, web shells, and more.
- [PayloadsAllTheThings](https://github.com/swisskyrepo/PayloadsAllTheThings): A list of useful payloads and bypasses for web application security and pentest/CTF.
- [FuzzDB](https://github.com/fuzzdb-project/fuzzdb): Dictionary of attack patterns and primitives for black-box application fault injection.
- [IntruderPayloads](https://github.com/1N3/IntruderPayloads): A collection of Burp Suite Intruder payloads and fuzz lists.

- - -

### Payload Tools

- [sqlmap](https://github.com/sqlmapproject/sqlmap): Automatic SQL injection and database takeover tool.
- [ffuf](https://github.com/ffuf/ffuf): Fast web fuzzer written in Go.
- [Burp Suite](https://portswigger.net/burp): Web security testing platform.

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
