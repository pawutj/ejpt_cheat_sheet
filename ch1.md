`nmap -sn 192.168.0.0/16` 
สแกนหาอุปกรณ์ทั้งหมดในช่วง IP 192.168.1.0 ถึง 192.168.1.255 (ใช้หาเครื่อง)

`nmap -Pn 10.4.19.218`
ไม่ตรวจว่าออนไลน์ไหม สแกนเลย (บางเครื่องปิดไม่ให้ ping แต่จริงๆเปิด port)

`nmap -Pn -p 80,443 10.4.19.218`
บังคับสแกน port 80,443

`nmap -Pn -F 10.4.19.218`
สแกนพอร์ทยอดนิยม 100 port

`nmap -Pn -sU 10.4.19.218`
สแกน UDP  ด้วย ช้ามาก 

`nmap -Pn -sV 10.4.19.218`
โชว์ version ด้วย สุดฮิต

`nmap -Pn -F -sV -O -sC 10.4.19.218 -v`
ข้าม port เช็ค 100 port แรก บังคับโชว์เวอร์ชั่น ตรวจสอบช่วงโหว่เบื้องต้น และแสดงผลละเอียด

`-T` ปรับความเร็ว
T0 (ช้ามากกก) T3 default T5 ไวจัด

`nmap target.ine.local -sV -sC`
คำสั่งทั่วไป (web ไม่มี http นะ)

`dirb http://target.ine.local` 
scan dir ทั่วไป

`dirb http://target.ine.local -w /usr/share/dirb/wordlists/big.txt -X .bak,.tar.gz,.zip,.sql,.bak.zip`
สแกนหาไฟล์ backup

`httrack http://target.ine.local -O target.html` 
mirror 