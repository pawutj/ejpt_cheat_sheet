# Apache Enumeration

auxiliary/scanner/http/apache_userdir_enum
auxiliary/scanner/http/brute_dirs
auxiliary/scanner/http/dir_scanner
auxiliary/scanner/http/dir_listing
auxiliary/scanner/http/http_put
auxiliary/scanner/http/files_dir
auxiliary/scanner/http/http_login
auxiliary/scanner/http/http_header
auxiliary/scanner/http/http_version
auxiliary/scanner/http/robots_txt

`msfconsole -q` 
start msf

`use auxiliary/scanner/http/http_version`
`set RHOSTS victim-1`
`run`
RHOSTS -> เป้าหมาย LHOST -> เครื่องเรา

`use auxiliary/scanner/http/http_header`
`use auxiliary/scanner/http/robots_txt`

คิดเสมอว่า พวกนี้ทำงานเหมือน curl ปกติ แต่เช็คทีละหลาย url ได้

`use auxiliary/scanner/http/http_put`
`set RHOSTS victim-1`
`set PATH /data`
`set FILENAME test.txt`
`set FILEDATA "Welcome To AttackDefense"`
`run`
test put method

