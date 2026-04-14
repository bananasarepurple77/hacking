## Shodan
```https://www.shodan.io/```
Search for specific versions and applications such as apache.
Shodan continuously scans the internet, searching for networking equipment, industrial control systems, traffic cameras, and virtually anything else with a public network connection to see what's running and where.
Also, has many filters using "Advanced search".

## Virus Total
```virustotal.com/gui/```
VirusTotal collates results from over 70 antivirus engines and website scanners into a single interface. Submit a file, a URL, a domain, or a file hash. VirusTotal will tell you whether any of those engines have flagged it as malicious or not.
Whilst not foolproof, VirusTotal is a popular resource in the blue teaming community for obtaining a general consensus on suspicious files and links, as well as for gathering intelligence on new threats on the move.

## Common Vulnerabilities and Exposures (CVE)
Closest thing the industry has to a universal dictionary of known vulnerabilities.
These vulnerabilities are given a score (CVSS) based on a variety of factors, such as:
Impact - What damage can this vulnerability lead to?
Complexity - Is the vulnerability easy to exploit or not? 
Availability - How likely is it that someone can exploit this?

## Linux Manual pages
```man {program-name}
man nc
```

## Github
GitHub can be a great resource for staying updated on the latest threats and vulnerabilities. Researchers often publish proof-of-concept (PoC) code, exploitation tools, and detailed technical reports there, which are usually faster than official channels. 
Searching for a CVE identifier (e.g., CVE-2026-13337) directly on GitHub often reveals repositories containing PoC code, scanner scripts, or detailed analyses of the vulnerability.
That said, not all PoCs are equally reliable. Some are incomplete, some are intentionally flawed, and occasionally a "PoC" repository is malicious itself. Always verify what you're about to execute.

