# SNMP Enumeration

## Snmp Walk

```bash
snmpwalk -v1 -c public <Target IP Address> 
```

Other SnmpWalk Commands: ▪ Command to enumerate SNMPv2 with a community string of public: 

snmpwalk -v2c -c public <Target IP Address>
▪ Command to search for installed software: 

snmpwalk -v2c -c public <Target IP Address> hrSWInstalledName
▪ Command to determine the amount of RAM on the host: 

snmpwalk -v2c -c public <Target IP Address> hrMemorySize
▪ Command to change an OID to a different value: 

snmpwalk -v2c -c public <Target IP Address> <OID> <New Value>
▪ Command to change the sysContact OID: 

snmpwalk -v2c -c public <Target IP Address> sysContact <New Value>

## Nmap

```bash
nmap -sU -p 161 --script=snmp-processes <Target IP Address>
```

Other Nmap commands to perform SNMP enumeration:
▪ nmap -sU -p 161 --script=snmp-sysdescr <Target IP Address> → Retrieves information regarding SNMP server type and operating system details.
▪ nmap -sU -p 161 --script=snmp-win32-software <Target IP Address> → Retrieves a list of all the applications running on the target machine.

The following are some additional SNMP enumeration tools:

▪ snmp-check (snmp_enum Module) Source: [https://www.nothink.org](https://www.nothink.org/)

 SoftPerfect Network Scanner( [https://www.softperfect.com](https://www.softperfect.com/))

▪ Network Performance Monitor ([https://www.solarwinds.com](https://www.solarwinds.com/)) 

▪ OpUtils ([https://www.manageengine.com](https://www.manageengine.com/)) 

▪ PRTG Network Monitor ([https://www.paessler.com](https://www.paessler.com/)) 

▪ Engineer’s Toolset ([https://www.solarwinds.com](https://www.solarwinds.com/))