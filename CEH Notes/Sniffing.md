# Sniffing

## bettercap

```bash
bettercap -iface eth0

net.probe on
net.recon on
net.sniff on 
```

## Macof

**Perform MAC Flooding using macof**

```bash
macof -i eth0 -n 10
```

## **Yersinia**

**Perform a DHCP Starvation Attack using Yersinia**

```bash
Yersinia -I
```

press F2 and then press x for available attack options(for help press h)

press 1 for sending DISCOVER packet

see using wirshark

## Wireshark

**Perform Password Sniffing using Wireshark**

we used filter http.request.method==POST

we can search in the wireshark for specific things 

clicking on search icon then change last option to String and middle option to Narrow (UTF-8 / ASCII) and first option to Packet details.

## **ARP Poisoning and Promiscuous Mode**

**Detect ARP Poisoning and Promiscuous Mode in a Switch-Based Network**

Using Cain tool

in configure option select device associated with machine in sniffer tab click ok

then press start button 

now in sniffer tab right click and click on scan mac address

in range section here we write 10.10.1.1 to 10.10.1.254

check on All Tests and ok

now In bottom click on APR then on that tab click on blue + icon and set both mac which we want  ten click on start APR icon 

then 

```bash
hping3 10.10.1.11 -c 100000
```

now in wireshark 

in edit >> options>> ARP/RARP 

check on detect ARP

in wireshark >>export info we see IP duplication

also in nmap see can see that 

```bash
nmap --script=sniffer-detect 10.10.1.19
```

**Detect ARP Poisoning using the Capsa Network Analyzer**

from [https://www.colasoft.com/download/products/download_capsa.php](https://www.colasoft.com/download/products/download_capsa.php)

download this tool trail

after installing and starting the tool

perform attack

```bash
habu.arp.poison 10.10.1.11 10.10.1.13
```

in tool 

in Diagnosis tab 

click on ARP too many

in below tab right click on security and click on resolve address