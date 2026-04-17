![Project logo](/.github/PayloadBase.png)

### About PayloadBase

PayloadBase is a modern payload arsenal for security researchers and bug bounty hunters, focused on real-world exploitation and modern attack surfaces (APIs, GraphQL, mobile, and cloud). Unlike traditional wordlists, PayloadBase emphasizes structured payloads, mutation-driven variations, and context-aware fuzzing sets designed for practical testing scenarios. The repository includes categorized payloads for SQL injection, XSS, SSRF, LFI, command injection, GraphQL security testing, IDOR, JWT weaknesses, OAuth flows, hidden parameters, mobile-specific vectors, and WAF bypass techniques.

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
| `cmdi/` | Command Injection — Unix, Windows, blind OOB |
| `crlf/` | CRLF Injection — header injection, response splitting |
| `csrf/` | CSRF — token bypass, SameSite tricks |
| `graphql/` | GraphQL Endpoint paths, query/mutation names, field names sensitif, type names, introspection bypass |
| `hidden_params/` | Debug flags, admin escalation, role injection, price manipulation, validation bypass, framework-specific |
| `idor/` | IDOR Numeric IDs, UUID variants, object-specific IDs, parameter pollution patterns, indirect ref fields |
| `jwt/` | JWT Weak secrets, framework defaults, language-specific, year-based patterns |
| `lfi/` | Local/Remote File Inclusion — path traversal, null byte, Windows |
| `mobile/` | Mobile base paths, push notification endpoints, deep links, version check, IAP, sync |
| `mutation/` | WAF bypass mutation payloads XSS (Cloudflare/ModSec), SQLi encoding, path traversal variants, CMDi, HTTP smuggling headers |
| `nosqli/` | NoSQL Injection — MongoDB, CouchDB, operator injection |
| `oauth/` | OAuth2/OIDC core endpoints, SAML, social login callbacks, .well-known, token management |
| `open_redirect/` | Open Redirect — protocol bypass, @-based, header injection |
| `polyglot/` | Multi-context polyglot payloads |
| `prototype_pollution/` | Prototype Pollution — client-side, server-side (Node.js) |
| `sqli/` | SQL Injection — time-based, boolean, error-based, OOB, WAF bypass |
| `ssrf/` | Server-Side Request Forgery — cloud metadata, bypass, internal ports |
| `ssti/` | Server-Side Template Injection — Jinja2, Twig, Freemarker, ERB, Pebble |
| `xss/` | Cross-Site Scripting — reflected, stored, DOM, blind, polyglot |
| `xxe/` | XML External Entity — file read, SSRF, blind OOB, bypass |
- - -

### Usage

**ffuf**
```bash
ffuf -u https://target.com/FUZZ -w sqli/time-based.txt
ffuf -u "https://target.com/page?id=FUZZ" -w sqli/boolean.txt
```
 
**Burp Suite Intruder**
```
Load any .txt file directly as Intruder payload list.
```
 
**SQLMap**
```bash
# GET
sqlmap -u "https://target.com/page?id=1" --technique=T --time-sec=10 --level=3 --risk=1
 
# POST (from saved request)
sqlmap -r /tmp/target.txt --technique=T --time-sec=10 --level=3 --risk=1
 
# Header injection
sqlmap -u "https://target.com/" --technique=T --time-sec=10 --level=5 --risk=3 -p "User-Agent" --random-agent
 
# WAF bypass
sqlmap -u "https://target.com/page?id=1" --tamper=space2comment,between,randomcase
```
 
**Dalfox (XSS)**
```bash
dalfox file xss/reflected.txt --silence
echo "https://target.com/?q=FUZZ" | dalfox pipe
```
 
**JWT crack**
```bash
hashcat -m 16500 <jwt_token> jwt/secrets.txt
python3 jwt_tool.py <token> -C -d jwt/secrets.txt
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
