# NetBIOS Enumeration

## nbtstat (windows)

```bash
nbtstat -A <IP Address>
nbtstat -c
```

## Nmap

```bash
nmap -sv -v --script nbstat.nse <IP Address>
nmap -sU -p 137 --script nbstat.nse [Target IP Address]
```

NetBIOS Enumerator( [http://nbtenum.sourceforge.net](http://nbtenum.sourceforge.net/) )

Global Network Inventory ([http://www.magnetosoft.com](http://www.magnetosoft.com/)) ▪ 

Advanced IP Scanner ([https://www.advanced-ip-scanner.com](https://www.advanced-ip-scanner.com/)) ▪ 

Hyena ([https://www.systemtools.com](https://www.systemtools.com/)) ▪ 

Nsauditor Network Security Auditor ([https://www.nsauditor.com](https://www.nsauditor.com/))

---

# User account

PStoolSuite

![image.png](NetBIOS%20Enumeration/image.png)

---

# Shared Resources

Enumerating Shared Resources Using Net View Net View is a command-line utility that displays a list of computers in a specified workgroup or shared resources available on a specified computer. It can be used in the following ways. 

net view \\<computername> 

In the above command, <computername> is the name or IP address of a specific computer, the resources of which are to be displayed. 

net view \\<computername> /ALL 

The above command displays all the shares on the specified remote computer, along with hidden shares.
net view /domain 

The above command displays all the shares in the domain. 

net view /domain:<domain name> 

The above command displays all the shares on the specified domain.