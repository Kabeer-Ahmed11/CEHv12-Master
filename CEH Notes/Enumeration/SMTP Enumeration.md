# SMTP Enumeration

Tools:

NetScanTools Pro ([https://www.netscantools.com](https://www.netscantools.com/)) 

smtp-user-enum Source: [http://pentestmonkey.net](http://pentestmonkey.net/)

```bash
smtp-user-enum.pl [options] (-u username|-U file-of-usernames) (-t host|-T file-of-targets)
```

### VRFY

![image.png](SMTP%20Enumeration/image.png)

### EXPN

![image.png](SMTP%20Enumeration/image%201.png)

### RCPT

![image.png](SMTP%20Enumeration/image%202.png)

### Nmap

 The following command, when executed, lists all the SMTP commands available in the Nmap directory: 

nmap -p 25, 365, 587 -script=smtp-commands <Target IP Address >
▪ Run the following command to identify SMTP open relays: 

nmap -p 25 -script=smtp-open-relay <Target IP Address>
▪ Run the following command to enumerate all the mail users on the SMTP server: 

nmap -p 25 –script=smtp-enum-users <Target IP Address>

### Metaslpoit

▪ Step 1: Launch Metasploit msfconsole and switch to the relevant auxiliary scanner to initiate the process: auxiliary/scanner/smtp/smtp_enum. msf > use auxiliary/scanner/smtp/smtp_enum msf auxiliary(smtp_enum) >
▪ Step 2: Use the command show options to view the entire list of options required to perform this task. Alternatively, the command show evasion can be used to view the list of options to evade security solutions.

▪ Step 3: Use the option set RHOST to set the target SMTP server’s IP address or a range of IP addresses.
▪ Step 4: By default, the Metasploit framework uses default wordlists located at /usr/share/64etasploit-framework/data/wordlists/unix_users.txt to enumerate SMTP users. The USER _FILE option can be set to use custom wordlists.
msf auxiliary(smtp_enum) > set USER_FILE <location of wordlists file>
▪ Step 5: Use the command show advanced to view the complete list of available options in the SMTP user enumeration module.