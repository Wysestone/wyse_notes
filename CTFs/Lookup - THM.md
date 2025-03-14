###Room Description

**Lookup** offers a treasure trove of learning opportunities for aspiring hackers. This intriguing machine showcases various real-world vulnerabilities, ranging from web application weaknesses to privilege escalation techniques. By exploring and exploiting these vulnerabilities, hackers can sharpen their skills and gain invaluable experience in ethical hacking. Through "Lookup," hackers can master the art of reconnaissance, scanning, and enumeration to uncover hidden services and subdomains. They will learn how to exploit web application vulnerabilities, such as command injection, and understand the significance of secure coding practices. The machine also challenges hackers to automate tasks, demonstrating the power of scripting in penetration testing.

###Nmap Scan

nmap -sCV -p- -Pn -T4 10.10.226.222 -vvv
Starting Nmap 7.80 ( https://nmap.org ) at 2025-03-14 00:28 GMT
NSE: Loaded 151 scripts for scanning.
NSE: Script Pre-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 00:28
Completed NSE at 00:28, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 00:28
Completed NSE at 00:28, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 00:28
Completed NSE at 00:28, 0.00s elapsed
Initiating ARP Ping Scan at 00:28
Scanning 10.10.226.222 [1 port]
Completed ARP Ping Scan at 00:28, 0.03s elapsed (1 total hosts)
Initiating Parallel DNS resolution of 1 host. at 00:28
Completed Parallel DNS resolution of 1 host. at 00:28, 0.00s elapsed
DNS resolution of 1 IPs took 0.00s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating SYN Stealth Scan at 00:28
Scanning 10.10.226.222 [65535 ports]
Discovered open port 22/tcp on 10.10.226.222
Discovered open port 80/tcp on 10.10.226.222
Completed SYN Stealth Scan at 00:28, 1.94s elapsed (65535 total ports)
Initiating Service scan at 00:28
Scanning 2 services on 10.10.226.222
Completed Service scan at 00:28, 6.01s elapsed (2 services on 1 host)
NSE: Script scanning 10.10.226.222.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 00:28
Completed NSE at 00:28, 0.22s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 00:28
Completed NSE at 00:28, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 00:28
Completed NSE at 00:28, 0.00s elapsed
Nmap scan report for 10.10.226.222
Host is up, received arp-response (0.000084s latency).
Scanned at 2025-03-14 00:28:34 GMT for 9s
Not shown: 65533 closed ports
Reason: 65533 resets
PORT   STATE SERVICE REASON         VERSION
22/tcp open  ssh     syn-ack ttl 64 OpenSSH 8.2p1 Ubuntu 4ubuntu0.9 (Ubuntu Linux; protocol 2.0)
80/tcp open  http    syn-ack ttl 64 Apache httpd 2.4.41 ((Ubuntu))
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-server-header: Apache/2.4.41 (Ubuntu)
|_http-title: Did not follow redirect to http://lookup.thm
MAC Address: 02:F4:E0:7F:3C:A9 (Unknown)
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

NSE: Script Post-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 00:28
Completed NSE at 00:28, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 00:28
Completed NSE at 00:28, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 00:28
Completed NSE at 00:28, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 9.95 seconds
           Raw packets sent: 65536 (2.884MB) | Rcvd: 65536 (2.621MB)


Ports 80 and 22 are open which means we will likely use something in the web interface to look for access to ssh.

10.10.226.222 redirects to http://lookup.thm/ 
10.10.226.222   lookup.thm  added to /etc/hosts using nano

This brings up  a login screen

![[Pasted image 20250313203740.png]]

No comments in the page source

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Login Page</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="container">
    <form action="login.php" method="post">
      <h2>Login</h2>
      <div class="input-group">
        <label for="username">Username</label>
        <input type="text" id="username" name="username" required>
      </div>
      <div class="input-group">
        <label for="password">Password</label>
        <input type="password" id="password" name="password" required>
      </div>
      <button type="submit">Login</button>
    </form>
  </div>
</body>
</html>

POST /login.php HTTP/1.1
Host: lookup.thm
Content-Length: 29
Cache-Control: max-age=0
Accept-Language: en-GB,en;q=0.9
Origin: http://lookup.thm
Content-Type: application/x-www-form-urlencoded
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/130.0.6723.70 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7
Referer: http://lookup.thm/
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

###Enumeration

root@ip-10-10-87-205:~# gobuster dir -u http://lookup.thm -w /usr/share/dirb/wordlists/common.txt 
===============================================================
Gobuster v3.6
by OJ Reeves (@TheColonial) & Christian Mehlmauer (@firefart)
===============================================================
[+] Url:                     http://lookup.thm
[+] Method:                  GET
[+] Threads:                 10
[+] Wordlist:                /usr/share/dirb/wordlists/common.txt
[+] Negative Status codes:   404
[+] User Agent:              gobuster/3.6
[+] Timeout:                 10s
===============================================================
Starting gobuster in directory enumeration mode
===============================================================
/.htaccess            (Status: 403) [Size: 275]
/.hta                 (Status: 403) [Size: 275]
/.htpasswd            (Status: 403) [Size: 275]
/index.php            (Status: 200) [Size: 719]
/server-status        (Status: 403) [Size: 275]
Progress: 4614 / 4615 (99.98%)
===============================================================
Finished
===============================================================
root@ip-10-10-87-205:~# gobuster dir -u http://lookup.thm -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt 
===============================================================
Gobuster v3.6
by OJ Reeves (@TheColonial) & Christian Mehlmauer (@firefart)
===============================================================
[+] Url:                     http://lookup.thm
[+] Method:                  GET
[+] Threads:                 10
[+] Wordlist:                /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt
[+] Negative Status codes:   404
[+] User Agent:              gobuster/3.6
[+] Timeout:                 10s
===============================================================
Starting gobuster in directory enumeration mode
===============================================================
/server-status        (Status: 403) [Size: 275]
Progress: 218275 / 218276 (100.00%)
===============================================================
Finished
===============================================================
root@ip-10-10-87-205:~# gobuster dns -d lookup.thm -w /usr/share/wordlists/SecLists/Discovery/DNS/subdomains-top1million-20000.txt 
===============================================================
Gobuster v3.6
by OJ Reeves (@TheColonial) & Christian Mehlmauer (@firefart)
===============================================================
[+] Domain:     lookup.thm
[+] Threads:    10
[+] Timeout:    1s
[+] Wordlist:   /usr/share/wordlists/SecLists/Discovery/DNS/subdomains-top1million-20000.txt
===============================================================
Starting gobuster in DNS enumeration mode
===============================================================
Progress: 19983 / 19984 (99.99%)
===============================================================
Finished
===============================================================
root@ip-10-10-87-205:~# gobuster vhost -u http://lookup.thm -w /usr/share/wordlists/SecLists/Discovery/DNS/subdomains-top1million-20000.txt ===============================================================
Gobuster v3.6
by OJ Reeves (@TheColonial) & Christian Mehlmauer (@firefart)
===============================================================
[+] Url:             http://lookup.thm
[+] Method:          GET
[+] Threads:         10
[+] Wordlist:        /usr/share/wordlists/SecLists/Discovery/DNS/subdomains-top1million-20000.txt
[+] User Agent:      gobuster/3.6
[+] Timeout:         10s
[+] Append Domain:   false
===============================================================
Starting gobuster in VHOST enumeration mode
===============================================================
Found: 1 Status: 400 [Size: 301]
Found: 11192521404255 Status: 400 [Size: 301]
Found: 11192521403954 Status: 400 [Size: 301]
Found: gc._msdcs Status: 400 [Size: 301]
Found: 2 Status: 400 [Size: 301]
Found: 11285521401250 Status: 400 [Size: 301]
Found: 2012 Status: 400 [Size: 301]
Found: 11290521402560 Status: 400 [Size: 301]
Found: 123 Status: 400 [Size: 301]
Found: 2011 Status: 400 [Size: 301]
Found: 3 Status: 400 [Size: 301]
Found: 4 Status: 400 [Size: 301]
Found: 2013 Status: 400 [Size: 301]
Found: 2010 Status: 400 [Size: 301]
Found: 911 Status: 400 [Size: 301]
Found: 11 Status: 400 [Size: 301]
Found: 24 Status: 400 [Size: 301]
Found: 10 Status: 400 [Size: 301]
Found: 7 Status: 400 [Size: 301]
Found: 99 Status: 400 [Size: 301]
Found: 2009 Status: 400 [Size: 301]
Found: www.1 Status: 400 [Size: 301]
Found: 50 Status: 400 [Size: 301]
Found: 12 Status: 400 [Size: 301]
Found: 20 Status: 400 [Size: 301]
Found: 2008 Status: 400 [Size: 301]
Found: 25 Status: 400 [Size: 301]
Found: 5 Status: 400 [Size: 301]
Found: 15 Status: 400 [Size: 301]
Found: www.2 Status: 400 [Size: 301]
Found: 13 Status: 400 [Size: 301]
Found: 100 Status: 400 [Size: 301]
Found: 44 Status: 400 [Size: 301]
Found: 54 Status: 400 [Size: 301]
Found: 9 Status: 400 [Size: 301]
Found: 70 Status: 400 [Size: 301]
Found: 01 Status: 400 [Size: 301]
Found: 16 Status: 400 [Size: 301]
Found: 39 Status: 400 [Size: 301]
Found: 6 Status: 400 [Size: 301]
Found: www.123 Status: 400 [Size: 301]
Found: 88 Status: 400 [Size: 301]
Found: 21 Status: 400 [Size: 301]
Found: 17 Status: 400 [Size: 301]
Found: 14 Status: 400 [Size: 301]
Found: 18 Status: 400 [Size: 301]
Found: 37 Status: 400 [Size: 301]
Found: 1234 Status: 400 [Size: 301]
Found: 79 Status: 400 [Size: 301]
Found: 35 Status: 400 [Size: 301]
Found: 49 Status: 400 [Size: 301]
Found: 114 Status: 400 [Size: 301]
Found: 29 Status: 400 [Size: 301]
Found: 8 Status: 400 [Size: 301]
Found: 0 Status: 400 [Size: 301]
Found: 1000 Status: 400 [Size: 301]
Found: 19 Status: 400 [Size: 301]
Found: 48 Status: 400 [Size: 301]
Found: 34 Status: 400 [Size: 301]
Found: 46 Status: 400 [Size: 301]
Found: 51 Status: 400 [Size: 301]
Found: 27 Status: 400 [Size: 301]
Found: 60 Status: 400 [Size: 301]
Found: 26 Status: 400 [Size: 301]
Found: 90 Status: 400 [Size: 301]
Found: 22 Status: 400 [Size: 301]
Found: 80 Status: 400 [Size: 301]
Found: 23 Status: 400 [Size: 301]
Found: 31 Status: 400 [Size: 301]
Found: 66 Status: 400 [Size: 301]
Found: 67 Status: 400 [Size: 301]
Found: 40 Status: 400 [Size: 301]
Found: 53 Status: 400 [Size: 301]
Found: 52 Status: 400 [Size: 301]
Found: mail.99 Status: 400 [Size: 301]
Found: www.2012 Status: 400 [Size: 301]
Found: 112 Status: 400 [Size: 301]
Found: 42 Status: 400 [Size: 301]
Found: 45 Status: 400 [Size: 301]
Found: 47 Status: 400 [Size: 301]
Found: 61 Status: 400 [Size: 301]
Found: 69 Status: 400 [Size: 301]
Found: 77 Status: 400 [Size: 301]
Found: 32 Status: 400 [Size: 301]
Found: 360 Status: 400 [Size: 301]
Found: 57 Status: 400 [Size: 301]
Found: 63 Status: 400 [Size: 301]
Found: 30 Status: 400 [Size: 301]
Found: 76 Status: 400 [Size: 301]
Found: www.24 Status: 400 [Size: 301]
Found: 94 Status: 400 [Size: 301]
Found: 64 Status: 400 [Size: 301]
Found: 111 Status: 400 [Size: 301]
Found: 28 Status: 400 [Size: 301]
Found: 33 Status: 400 [Size: 301]
Found: 41 Status: 400 [Size: 301]
Found: 101 Status: 400 [Size: 301]
Found: 203 Status: 400 [Size: 301]
Found: 163 Status: 400 [Size: 301]
Found: 666 Status: 400 [Size: 301]
Found: 365 Status: 400 [Size: 301]
Found: www.2011 Status: 400 [Size: 301]
Found: www.11 Status: 400 [Size: 301]
Found: 777 Status: 400 [Size: 301]
Found: 12345 Status: 400 [Size: 301]
Found: 132 Status: 400 [Size: 301]
Found: mail.85st Status: 400 [Size: 301]
Found: 43 Status: 400 [Size: 301]
Found: 120 Status: 400 [Size: 301]
Found: www.3 Status: 400 [Size: 301]
Found: 65 Status: 400 [Size: 301]
Found: www.4 Status: 400 [Size: 301]
Found: 87 Status: 400 [Size: 301]
Found: 91 Status: 400 [Size: 301]
Found: 89 Status: 400 [Size: 301]
Found: 71 Status: 400 [Size: 301]
Found: 58 Status: 400 [Size: 301]
Found: 56 Status: 400 [Size: 301]
Found: 55 Status: 400 [Size: 301]
Found: www.16 Status: 400 [Size: 301]
Found: 204 Status: 400 [Size: 301]
Found: 103 Status: 400 [Size: 301]
Found: www.10 Status: 400 [Size: 301]
Found: www.2013 Status: 400 [Size: 301]
Found: 110 Status: 400 [Size: 301]
Found: 404 Status: 400 [Size: 301]
Found: www.15 Status: 400 [Size: 301]
Found: 125 Status: 400 [Size: 301]
Found: 123456 Status: 400 [Size: 301]
Found: 86 Status: 400 [Size: 301]
Found: 81 Status: 400 [Size: 301]
Found: 75 Status: 400 [Size: 301]
Found: 74 Status: 400 [Size: 301]
Found: 68 Status: 400 [Size: 301]
Found: 62 Status: 400 [Size: 301]
Found: www.12 Status: 400 [Size: 301]
Found: 96 Status: 400 [Size: 301]
Found: www.13 Status: 400 [Size: 301]
Found: www.20 Status: 400 [Size: 301]
Found: 02 Status: 400 [Size: 301]
Found: www.9 Status: 400 [Size: 301]
Found: 222 Status: 400 [Size: 301]
Found: 8591 Status: 400 [Size: 301]
Found: mail.77p2p Status: 400 [Size: 301]
Found: mail.8591 Status: 400 [Size: 301]
Found: 5278 Status: 400 [Size: 301]
Found: mail.5278 Status: 400 [Size: 301]
Found: 228 Status: 400 [Size: 301]
Found: mail.85cc Status: 400 [Size: 301]
Found: www.7 Status: 400 [Size: 301]
Found: 109 Status: 400 [Size: 301]
Found: 129 Status: 400 [Size: 301]
Found: 128 Status: 400 [Size: 301]
Found: 105 Status: 400 [Size: 301]
Found: 118 Status: 400 [Size: 301]
Found: 119 Status: 400 [Size: 301]
Found: 212 Status: 400 [Size: 301]
Found: 121 Status: 400 [Size: 301]
Found: 126 Status: 400 [Size: 301]
Found: 000 Status: 400 [Size: 301]
Found: 106 Status: 400 [Size: 301]
Found: 11091521400593 Status: 400 [Size: 301]
Found: 230 Status: 400 [Size: 301]
Found: 234 Status: 400 [Size: 301]
Found: 080 Status: 400 [Size: 301]
Found: 233 Status: 400 [Size: 301]
Found: 170 Status: 400 [Size: 301]
Found: www.19 Status: 400 [Size: 301]
Found: www.25 Status: 400 [Size: 301]
Found: 93 Status: 400 [Size: 301]
Found: www.17 Status: 400 [Size: 301]
Found: www.18 Status: 400 [Size: 301]
Found: 97 Status: 400 [Size: 301]
Found: 95 Status: 400 [Size: 301]
Found: 59 Status: 400 [Size: 301]
Found: 36 Status: 400 [Size: 301]
Found: 72 Status: 400 [Size: 301]
Found: 73 Status: 400 [Size: 301]
Found: 92 Status: 400 [Size: 301]
Found: 03 Status: 400 [Size: 301]
Found: 38 Status: 400 [Size: 301]
Found: 205 Status: 400 [Size: 301]
Found: mail.666av Status: 400 [Size: 301]
Found: mail.080 Status: 400 [Size: 301]
Found: 1111 Status: 400 [Size: 301]
Found: 235 Status: 400 [Size: 301]
Found: www.2010 Status: 400 [Size: 301]
Found: 211 Status: 400 [Size: 301]
Found: 192 Status: 400 [Size: 301]
Found: 2006 Status: 400 [Size: 301]
Found: 209 Status: 400 [Size: 301]
Found: 117 Status: 400 [Size: 301]
Found: 130 Status: 400 [Size: 301]
Found: 007 Status: 400 [Size: 301]
Found: 137 Status: 400 [Size: 301]
Found: www.6 Status: 400 [Size: 301]
Found: www.5 Status: 400 [Size: 301]
Found: www.14 Status: 400 [Size: 301]
Found: 237 Status: 400 [Size: 301]
Found: 169 Status: 400 [Size: 301]
Found: 131 Status: 400 [Size: 301]
Found: 134 Status: 400 [Size: 301]
Found: 162 Status: 400 [Size: 301]
Progress: 19983 / 19984 (99.99%)
===============================================================
Finished
===============================================================
root@ip-10-10-87-205:~# 

No luck with enumeration

username=admin&password=admin

Looking to see what error we get when passing in admin/admin
	Error reports wrong password, means likely we could pass a password list.
		Possibly a red herring because when trying other passwords for admin other than "admin" we see that either the username or the password are invalid.
		Running cluster attack against usernames and passwords in attempt to find a possible redirect
		---------------------------------------------
		Will pick up from here
