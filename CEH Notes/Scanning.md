# Scanning

[**Host Discovery**](Scanning/Host%20Discovery.md)

[**Port and Service Discovery**](Scanning/Port%20and%20Service%20Discovery.md)

[**OS Discovery**](Scanning/OS%20Discovery.md)

[**Scan beyond IDS and Firewall**](Scanning/Scan%20beyond%20IDS%20and%20Firewall.md)

[VPN](Scanning/VPN.md)

[Anonymizers](Scanning/Anonymizers.md)

## nmap

## wireshark

## hping3

```bash
hping3 <ip> --udp --rand-source --data 500(datasize)
```

```bash
hping3 -S <ip> -p <port> -c 5(count of packets)
```

## **Metasploit**

for Portscan

- **set INTERFACE eth0**
- **set PORTS 80**
- **set RHOSTS 10.10.1.5-23**
- **set THREADS 50**

 for **auxiliary/scanner/portscan/tcp**

**set RHOSTS [Target IP Address]**

**use auxiliary/scanner/smb/smb_version**

- **set RHOSTS 10.10.1.5-23**
- **set THREADS 11**