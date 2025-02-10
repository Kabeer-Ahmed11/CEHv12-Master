# Host Discovery

## Nmap

**-sn**: disables port scan.

**-PR**: performs ARP ping scan.
**-PU**: performs the UDP ping scan.
**-PE**: performs the ICMP ECHO ping scan.
**-PP**: performs the ICMP timestamp ping scan.
**ICMP Address Mask Ping Scan**: **nmap -sn -PM [target IP address]**
**TCP ACK Ping Scan**: **nmap -sn -PA [target IP address]**

**TCP SYN Ping Scan**: **nmap -sn -PS [target IP address]**

**IP Protocol Ping Scan**: **nmap -sn -PO [target IP address]**

## Angry IP Scanner

 **SolarWinds Engineer’s Toolset** (https://www.solarwinds.com), 
**NetScanTools Pro** (https://www.netscantools.com), 
**Colasoft Ping Tool** (https://www.colasoft.com), 
**Visual Ping Tester** (http://www.pingtester.net), 
**OpUtils** (https://www.manageengine.com) to discover active hosts in the target network.