# 📚 Kali Linux Wordlists — Quick Reference

Kali comes with several high‑value wordlist collections preinstalled. These are the most useful paths and recommended lists for CTFs.

---

## 📁 Default Wordlist Locations

### **SecLists (largest and most useful)**
Path:
/usr/share/seclists/

Recommended lists:
- **DNS brute‑forcing**  
  `/usr/share/seclists/Discovery/DNS/subdomains-top1million-5000.txt`
- **Directory brute‑forcing**  
  `/usr/share/seclists/Discovery/Web-Content/common.txt`  
  `/usr/share/seclists/Discovery/Web-Content/directory-list-2.3-medium.txt`
- **Passwords**  
  `/usr/share/seclists/Passwords/rockyou-75.txt`  
  `/usr/share/seclists/Passwords/Common-Credentials/10-million-password-list-top-1000000.txt`
- **Usernames**  
  `/usr/share/seclists/Usernames/top-usernames-shortlist.txt`

---

## 🔐 RockYou (classic password list)
Path (compressed by default):
/usr/share/wordlists/rockyou.txt.gz

Unzip:
gunzip /usr/share/wordlists/rockyou.txt.gz

Recommended use:
- Password cracking  
- Login brute‑forcing  
- Wi‑Fi cracking  
- Web login forms

---

## 🌐 Dirb Wordlists
Path:
/usr/share/dirb/wordlists/


Recommended lists:
- `common.txt`
- `big.txt`

Good for:
- Directory enumeration  
- Lightweight scans

---

## 🗂️ DirBuster Wordlists
Path:
/usr/share/dirbuster/wordlists/

Recommended lists:
- `directory-list-2.3-small.txt`
- `directory-list-2.3-medium.txt`

Good for:
- Web directory brute‑forcing  
- Larger scans with more coverage

---

## 🧭 Quick Usage Examples

**DNS brute‑force:**
`gobuster dns -d target.ctf -w /usr/share/seclists/Discovery/DNS/subdomains-top1million-5000.txt`

**Directory brute‑force:**
`gobuster dir -u http://target.ctf -w /usr/share/seclists/Discovery/Web-Content/common.txt`

**Password cracking:**
`hydra -l admin -P /usr/share/wordlists/rockyou.txt <service>`

---

## ✅ Summary
Kali includes:
- **SecLists** → best all‑rounder for DNS, directories, passwords  
- **RockYou** → essential password list  
- **Dirb/DirBuster lists** → strong for web enumeration

