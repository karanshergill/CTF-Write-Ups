# Enumeration
## Find target IP address
```
sudo netdiscover
```

## Full Port Scan
```
nmap -sC -sV -p- -v 192.168.1.33
```
IMG

## HTTP (Port 80)
IMG

## Directory Brute-Forcing
```
gobuster dir -u http://192.168.1.33 -w /usr/share/seclists/Discovery/Web-Content/directory-list-2.3-small.txt
```

## Recursive Directory Brute-Forcing
```
gobuster dir -u http://192.168.1.33/mailer -w /usr/share/seclists/Discovery/Web-Content/directory-list-2.3-small.txt
```

# Enumeration Results




## Python
```
python -c 'import pty;pty.spawn("/bin/bash")'
```
