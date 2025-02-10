# DNS Enumeration

**dig**

```bash
dig ns <target domain>
dig @<domain of name server> <target domain> axfr
```

**nslookup**

nslookup Command Source: [https://docs.microsoft.com](https://docs.microsoft.com/)
Attackers use the nslookup command on Windows-based systems to query the DNS name servers and retrieve information about the target host addresses, name servers, mail exchanges, etc. As shown in the screenshot, attackers use the following command to perform DNS zone transfer: nslookup set querytype=soa <target domain> The above command sets the query type to the Start of Authority (SOA) record to retrieve administrative information about the DNS zone of the target domain [certifiedhacker.com](http://certifiedhacker.com/). The following command is used to attempt to transfer the zone of the specified name server: /ls -d <domain of name server>

**DNSRecon**

```bash
dnsrecon -t axfr -d <target domain>
```

---

# DNS cache Snooping

dig

![image.png](DNS%20Enumeration/image.png)

---

# DNSSEC Zone Walking

![image.png](DNS%20Enumeration/image%201.png)

---

# DNS and DNSSEC Enumeration Using Nmap

DNS Enumeration

```bash
nmap --script=broadcast-dns-service-discovery <Target Domain>
nmap -T4 -p 53 --script dns-brute <Target Domain>
```

tools:

Knock ([https://github.com](https://github.com/)) 

Raccoon ([https://github.com](https://github.com/)) 

Subfinder ([https://github.com](https://github.com/)) 

Turbolist3r ([https://github.com](https://github.com/)

DNS Security Extensions (DNSSEC) Enumeration 

```bash
nmap -sU -p 53 --script dns-nsec-enum --script-args dns-nsec-enum.domains= eccouncil.org <target>
```