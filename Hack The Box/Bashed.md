# Reconnaissance
### NMAP Initial Scan
```
▶ nmap -Pn -sS -T4 -p- 10.10.10.68

PORT   STATE SERVICE
80/tcp open  http
```

### NMAP Complete Scan
```
▶ nmap -sC -sV -O 10.10.10.68 -p 80

PORT   STATE SERVICE VERSION
80/tcp open  http    Apache httpd 2.4.18 ((Ubuntu))
|_http-server-header: Apache/2.4.18 (Ubuntu)
|_http-title: Arrexel's Development Site
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
Aggressive OS guesses: Linux 3.2 - 4.9 (95%), Linux 3.16 (95%), ASUS RT-N56U WAP (Linux 3.4) (95%), Linux 3.18 (94%), Linux 4.2 (94%), Linux 3.12 (93%), Linux 3.13 (93%), Linux 3.8 - 3.11 (93%), Linux 4.8 (93%), Linux 4.4 (93%)
No exact OS matches for host (test conditions non-ideal).
Network Distance: 2 hops

OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 18.25 seconds
```

---

# Content Discovery
## Gobuster Directory Brute-Force
```
▶ gobuster dir --url http://10.10.10.68/ --wordlist /usr/share/seclists/Discovery/Web-Content/directory-list-2.3-small.txt

===============================================================
Starting gobuster in directory enumeration mode
===============================================================
/images               (Status: 301) [Size: 311] [--> http://10.10.10.68/images/]
/uploads              (Status: 301) [Size: 312] [--> http://10.10.10.68/uploads/]
/php                  (Status: 301) [Size: 308] [--> http://10.10.10.68/php/]
/css                  (Status: 301) [Size: 308] [--> http://10.10.10.68/css/]
/dev                  (Status: 301) [Size: 308] [--> http://10.10.10.68/dev/]
/js                   (Status: 301) [Size: 307] [--> http://10.10.10.68/js/]
/fonts                (Status: 301) [Size: 310] [--> http://10.10.10.68/fonts/]
===============================================================
Finished
===============================================================

```
