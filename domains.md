Finding subdomain certificates and issuers of example.com:
https://crt.sh/?q=%.example.com&dir=ASC

### robots.txt
- Tells crawlers which paths they should avoid (Disallow)
- Optionally tells them which paths are allowed even inside blocked areas (Allow)
- Applies rules per crawler via User-agent
- Does not hide content from users or prevent direct access

## 🧭 DIG — Quick CTF Notes

**Basic lookup**  
`dig domain.com` — full DNS response  
`dig domain.com +short` — clean output (IPs only)

**Record types**  
`dig domain.com A` — IPv4  
`dig domain.com AAAA` — IPv6  
`dig domain.com TXT` — hidden hints often here  
`dig domain.com MX` — mail servers  
`dig domain.com NS` — name servers  
`dig domain.com ANY` — grab everything (if allowed)

**Reverse lookup**  
`dig -x <IP>`

**Query specific DNS server**  
`dig @server domain.com`

**Trace DNS path**  
`dig domain.com +trace` — useful for custom TLDs or staged puzzles

**Zone transfer attempt (AXFR)**  
`dig AXFR domain.com @ns1.domain.com`  
(CTF classic — reveals all subdomains if misconfigured)

**Bruteforce subdomains**  
Use a wordlist:  
`for s in $(cat list.txt); do dig +short $s.domain.com; done`

**Check TTLs / weird behavior**  
`dig domain.com +ttlunits`

## 🚀 GoBuster / Fierce
**GoBuster (DNS mode)**  
`gobuster dns -h` — help menu  
`gobuster dns -d dns.ctf -w wordlist.txt` — brute‑force subdomains  
`gobuster dns -d dns.ctf -w wordlist.txt -t 50` — faster (threads)

**Fierce (alternative to GoBuster)**  
`fierce --domain dns.ctf --subdomain-file subdomains-top1million-5000.txt`  
Useful for recursive DNS enumeration and finding deep subdomain chains.

**After finding subdomains**  
Scan common web ports:  
`nmap -p 80,443 <target>`  
Check for web services, redirects, hidden directories, or next‑stage clues.
