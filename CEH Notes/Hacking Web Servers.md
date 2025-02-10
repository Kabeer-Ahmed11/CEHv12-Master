# Hacking Web Servers

## **Ghost Eye**

```bash
pip3 install -r requirment.txt 
python3 ghost_eye.py 
```

now choice but here we uses option 3 and 2 

and enter <targetip/url> 

## Netcat

**Footprint a Web Server using Netcat**

```bash
nc -vv <url> 80 (any port)
GET / HTTP/1.0
```

## Telnet

**Footprint a Web Server using Telnet**

```bash
telnet <url> 80 (any port)
GET / HTTP/1.0
```

## Nmap

**Enumerate Web Server Information using Nmap Scripting Engine (NSE)**

```bash
nmap -sV --script=http-enum <URL>

nmap --script hostmap-bfk -script-args hostmap-bfk.prefix=hostnmap- <URL>

nmap --script http-trace -d <URL>

namp -p 80 --script http-waf-detect <URL>
```

## Hydra

**Crack FTP Credentials using a Dictionary Attack**

```bash
hydra -L usernam.txt -P password.txt ftp://<IP>
```