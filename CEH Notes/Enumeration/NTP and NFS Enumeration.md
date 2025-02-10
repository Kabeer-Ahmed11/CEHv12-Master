# NTP and NFS Enumeration

## NTP

**ntpdate**
This command collects the number of time samples from several time sources. Its syntax is as follows:
ntpdate [-46bBdqsuv] [-a key] [-e authdelay] [-k keyfile] [-o version] [-p samples] [-t timeout] [ -U user_name] server [...]

**ntptrace** 

This command determines where the NTP server obtains the time from and follows the chain of NTP servers back to its primary time source. Attackers use this command to trace the list of NTP servers connected to the network. Its syntax is as follows: 

ntptrace [-n] [-m maxhosts] [servername/IP_address]

**ntpdc**
This command queries the ntpd daemon regarding its current state and requests changes in that state. Attackers use this command to retrieve the state and statistics of each NTP server connected to the target network. Its syntax is as follows: 

ntpdc [ -46dilnps ] [ -c command] [hostname/IP_address]

**ntpq** 

This command monitors the operations of the NTP daemon ntpd and determines its performance. Its syntax is as follows: 

ntpq [-46dinp] [-c command] [host/IP_address]

PRTG Network Monitor ([https://www.paessler.com](https://www.paessler.com/))

Nmap ([https://nmap.org](https://nmap.org/)) 

Wireshark ([https://www.wireshark.org](https://www.wireshark.org/)) 

udp-proto-scanner ([https://labs.portcullis.co.uk](https://labs.portcullis.co.uk/)) 

NTP Server Scanner ([http://www.bytefusion.com](http://www.bytefusion.com/))

---

## NFS

rpcinfo -p <Target IP Address>

showmount -e <Target IP Address>

RPCScan Source: [https://github.com](https://github.com/) 

RPCScan communicates with RPC services and checks misconfigurations on NFS shares. As shown in the screenshot, an attacker runs the following command to enumerate a target IP address for active NFS services: 

```bash
python3 [rpc-scan.py](http://rpc-scan.py/) <Target IP Address> --rpc
```

SuperEnum Source: [https://github.com](https://github.com/)
SuperEnum includes a script that performs the basic enumeration of any open port. As shown in the screenshot, an attacker uses the ./superenum script and then enters a text file name “Target.txt” having a target IP address or a list of IP addresses for enumeration.