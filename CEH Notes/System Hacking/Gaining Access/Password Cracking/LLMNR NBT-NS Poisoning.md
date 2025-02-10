# LLMNR/NBT-NS Poisoning

How to Defend against LLMNR/NBT-NS Poisoning

▪ Disabling LMBNR 

o Open the Local Group Policy Editor. 

o Navigate to Local Computer Policy → Computer Configuration → Administrative Templates → Network → DNS Client.
o In the DNS Client, double-click Turn off multicast name resolution.

o Select the Enabled radio button and then click OK.

▪ Disabling NBT-NS
o Open the Control Panel, navigate to Network and Internet → Network and Sharing Center, and click on the Change adapter settings option on the right-hand side.
o Right-click on the network adapter and then click Properties, select TCP/IPv4, and then click Properties.
o Under the General tab, go to Advanced → WINS.
o From the NetBIOS setting options, check the “Disable NetBIOS over TCP/IP” radio button and click OK.

![image.png](LLMNR%20NBT-NS%20Poisoning/image.png)

## Tools to Detect LLMNR/NBT-NS Poisoning

▪ Vindicate 

Source: [https://github.com](https://github.com/)

▪ Respounder 

Source: [https://github.com](https://github.com/)

▪ got-responded 

Source: [https://github.com](https://github.com/)