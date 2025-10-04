# Apache Enumeration

`msfconsole -q` 
start msf

`use auxiliary/scanner/http/http_version`
`set RHOSTS victim-1`
`run`
RHOSTS -> เป้าหมาย LHOST -> เครื่องเรา

`use auxiliary/scanner/http/http_header`
`use auxiliary/scanner/http/robots_txt`

คิดเสมอว่า พวกนี้ทำงานเหมือน curl ปกติ แต่เช็คทีละหลาย url ได้

