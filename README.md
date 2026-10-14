# Week 6: Web Security & Vulnerability Testing (VAPT Basics)

**Cyber Security Internship Program | DG Cyber Security Internship**
**Submitted by:** Diksha Uma Shankar Rao

This repository contains my Week 6 work on web application security. I studied common OWASP Top 10 vulnerabilities, set up a safe lab with DVWA, tested SQL Injection and XSS manually with Burp Suite, and ran an automated scan with OWASP ZAP.

> All testing was done only on my own local DVWA lab (Kali Linux, security level Low). Nothing here was tested on systems I do not own or have permission to test.

## Tools Used

- Kali Linux (attacker machine)
- DVWA (Damn Vulnerable Web Application) as the target
- Burp Suite Community Edition
- OWASP ZAP

## Repository Contents

- `Report/` - Final project report (PDF)
- `PPT/` - Presentation (10 slides)
- `Screenshots/` - All lab screenshots (payloads, results, Burp requests and responses, ZAP scan)
- `Notes/` - Short study notes on SQL Injection, XSS, Broken Authentication and Security Misconfiguration

## Summary of Work

- **SQL Injection:** payload `1' OR '1'='1` returned the full users table. Risk: High.
- **Reflected XSS:** script executed from user input. Risk: Medium.
- **Stored XSS:** script was saved in the database and executed again on page refresh. Risk: High.
- **Burp Suite:** captured and inspected the requests and responses for the SQL Injection test.
- **OWASP ZAP:** automated scan found 9 distinct alerts (10 instances): 2 Medium, 5 Low, 3 Informational. Examples include Missing Anti-Clickjacking Header and CSP Header Not Set.

## Mitigation Highlights

- Use parameterised queries to prevent SQL Injection
- Encode output and set a Content-Security-Policy header to prevent XSS
- Set security headers such as X-Frame-Options on every response
- Keep training and debug configurations out of production

## Disclaimer

This project is for educational purposes only. DVWA is intentionally vulnerable and must never be exposed to the internet or used in production.
