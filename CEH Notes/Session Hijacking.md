# Session Hijacking

## **OWASP ZAP (Zed Attack Proxy)**

**Hijack a Session using Zed Attack Proxy (ZAP)**

set proxy ip of the attacker machine on the target machine and also in the zap local proxy at the setting icon on the zap tool.

also add a break tab before intercepting any request and press the green circle icon to intercept 

## Hetty

**Intercept HTTP Traffic using Hetty**

click on hetty.exe then launch the browser and visit localhost:8080

to access hetty dashboard

add proxy of attacker machine on target machine.

and see the requests in proxy logs section.

## Wireshark

**Detect Session Hijacking using Wireshark**

after starting the sniffing using  bettercap tool

now in wireshark we see huge broadcast packets on ARP protocol which is the sign of sniffing or session hijacking