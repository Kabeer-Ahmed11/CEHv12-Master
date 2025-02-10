# Executing Applications

▪ **Backdoors:** 

Program designed to deny or disrupt the operation, gather information that leads to exploitation or loss of privacy, or gain unauthorized access to system resources.
**▪ Crackers:** 

Components of software or programs designed for cracking a code or passwords.
▪ **Keyloggers:** 

These can be hardware or software. In either case, the objective is to record each keystroke made on the computer keyboard.
**▪ Spyware:** 

Spy software may capture screenshots and send them to a specified location defined by the hacker. For this purpose, attackers have to maintain access to victims’ computers. After deriving all the requisite information from the victim’s computer, the attacker installs several backdoors to maintain easy access to it in the future.

## Remote Code Execution Techniques

### **Exploitation for Client Execution**

Insecure coding practices in software can make it vulnerable to various attacks. Attackers can exploit these underlying vulnerabilities in software through focused and targeted exploitations with an objective of arbitrary code execution to maintain access to the target remote system. Different types of exploitations for client execution are as follows: 

o **Web-Browser-Based Exploitation** 

Attackers target web browsers through spear phishing links and drive-by compromise. The remote systems can be compromised through normal web browsing or through several users who are targeted victims of spear phishing links to attacker-controlled sites used to exploit the web browser. This type of exploitation does not need user intervention for execution.

o **Office-Applications-Based Exploitation**
Attackers target common office applications such as Microsoft Office through different variants of spear phishing. Emails containing links to malicious files are directly sent to the end-users for downloading. To run the exploit, end-users are required to open a malicious document or file.

o **Third-Party Applications-Based Exploitation**
Attackers can also exploit commonly used third-party applications deployed as part of the software. Applications such as Adobe Reader, Flash, etc. are usually targeted by attackers to gain access to remote systems.

### Service Execution

System services are programs that run and operate at the backend of an OS. Attackers run binary files or commands that can communicate with Windows system services such as Service Control Manager. This code execution technique is performed by creating a new service or by modifying an existing service at the time of privilege escalation or maintaining access.

### Windows Management Instrumentation (WMI)

WMI is a feature in Windows administration that manages data and operations on Windows and provides a platform for accessing Windows system resources locally and remotely. Attackers can use the WMI feature to interact with the target system remotely, gather information on system resources, and further execute code for maintaining access to the target system.

### Windows Remote Management (WinRM)

WinRM is a Windows-based protocol designed to allow a user to run an executable file to modify system services and the registry on a remote system. Attackers can use the winrm command to interact with WinRM and execute a payload on the remote system as a part of lateral movement.

## Tools for Executing Applications

▪ Dameware Remote Support 

Source: [https://www.dameware.com](https://www.dameware.com/)

▪ Ninja ([https://github.com](https://github.com/)) 

▪ Pupy ([https://github.com](https://github.com/)) 

▪ PDQ Deploy ([https://www.pdq.com](https://www.pdq.com/)) 

▪ ManageEngine Desktop Central ([https://www.manageengine.com](https://www.manageengine.com/)) 

▪ PsExec ([https://docs.microsoft.com](https://docs.microsoft.com/)

## Keylogger

Remote Keylogger Attack Using Metasploit

![image.png](Executing%20Applications/image.png)

### Anti-Keyloggers

▪ Zemana AntiLogger 

Source: [https://www.zemana.com](https://www.zemana.com/)

▪ GuardedID ([https://www.strikeforcecpg.com](https://www.strikeforcecpg.com/)) 

▪ KeyScrambler ([https://www.qfxsoftware.com](https://www.qfxsoftware.com/)) 

▪ Oxynger KeyShield ([https://www.oxynger.com](https://www.oxynger.com/)) 

▪ Ghostpress ([https://schiffer.tech](https://schiffer.tech/)) 

▪ SpyShelter Silent Anti Keylogger ([https://www.spyshelter.com](https://www.spyshelter.com/))

## Spyware

![image.png](Executing%20Applications/image%201.png)

### Spyware Tools

▪ Spytech SpyAgent 

Source: [https://www.spytech-web.com](https://www.spytech-web.com/)

▪ Power Spy 

Source: [https://ematrixsoft.com](https://ematrixsoft.com/)

### Types of Spyware

▪ **Desktop Spyware** 

Desktop spyware is software that allows an attacker to gain information about a user’s activity or personal information, send it via the Internet to third parties without the user’s knowledge or consent. It provides information regarding what network users did on their desktops, how, and when. 

The following is the list of desktop and child-monitoring spyware: 

o ActivTrak ([https://activtrak.com](https://activtrak.com/)) 

o Veriato Cerebral ([http://www.veriato.com](http://www.veriato.com/)) 

o NetVizor ([https://www.netvizor.net](https://www.netvizor.net/)) 

o SoftActivity Monitor ([https://www.softactivity.com](https://www.softactivity.com/)) 

o SoftActivity TS Monitor ([https://www.softactivity.com](https://www.softactivity.com/))

▪ **Email Spyware** 

Email spyware is a program that monitors, records, and forwards all incoming and outgoing emails.

▪ **Internet Spyware**
Internet spyware is a tool that allows you to monitor all the web pages accessed by users on your computer in your absence. It makes a chronological record of all visited URLs.

▪ **Child-Monitoring Spyware**
Child-monitoring spyware allows you to track and monitor what children are doing on the computer, both online and offline.

▪ **Screen-Capturing Spyware** 

Screen-capturing spyware is a program that allows you to monitor computer activities by taking snapshots or screenshots of the computer on which the program is installed. 

▪ **USB Spyware**
USB spyware is a program designed for spying on a computer, which copies spyware files from a USB device onto the hard disk without any request or notification.

The following is the list of USB spyware: 

o USB Analyzer ([https://www.eltima.com](https://www.eltima.com/)) 

o USB Monitor ([https://www.hhdsoftware.com](https://www.hhdsoftware.com/)) 

o USBDeview ([https://www.nirsoft.net](https://www.nirsoft.net/)) 

o Advanced USB Port Monitor ([https://www.aggsoft.com](https://www.aggsoft.com/)) 

o USB Monitor Pro ([https://www.usb-monitor.com](https://www.usb-monitor.com/))

▪ **Audio Spyware**
Audio spyware is a sound surveillance program designed to record sound onto a computer. 

The following is the list of audio spyware: 

o Spy Voice Recorder ([http://www.mysuperspy.com](http://www.mysuperspy.com/)) 

o Digital Voice Logger ([https://www.securityplanet.co](https://www.securityplanet.co/)) 

o USB Stick Grey Recorder ([https://www.spytec.com](https://www.spytec.com/)) 

o Audio Spyware Snooper ([https://www.snooper.se](https://www.snooper.se/))

▪ **Video Spyware**
Video spyware is software for video surveillance installed on a target computer without the user’s knowledge.

The following is the list of video spyware: 

o Movavi Video Editor ([https://www.movavi.com](https://www.movavi.com/)) 

o iSpy ([https://www.ispyconnect.com](https://www.ispyconnect.com/)) 

o NET Video Spy ([https://www.sarbash.com](https://www.sarbash.com/)) 

o Eyeline Video Surveillance Software ([https://www.nchsoftware.com](https://www.nchsoftware.com/)) 

o WebCam Looker ([https://felenasoft.com](https://felenasoft.com/))

▪ **Print Spyware** 

Attackers can monitor the printer usage of the target organization remotely by using print spyware. Print spyware is printer usage monitoring software that monitors printers in the organization.

▪ **Telephone/Cellphone Spyware**
Telephone/cellphone spyware is a software tool that gives you full access to monitor a victim’s telephone or cellphone.

The following is the list of telephone/cellphone spyware: 

o Phone Spy ([https://www.phonespysoftware.com](https://www.phonespysoftware.com/)) 

o XNSPY ([https://xnspy.com](https://xnspy.com/)) 

o iKeyMonitor ([https://ikeymonitor.com](https://ikeymonitor.com/)) 

o OneSpy ([https://www.onespy.in](https://www.onespy.in/)) 

o TheTruthSpy ([https://thetruthspy.com](https://thetruthspy.com/))

▪ **GPS Spyware** 

GPS spyware is a device or software application that uses the Global Positioning System (GPS) to determine the location of a vehicle, person, or other attached or installed asset. An attacker can use this software to track the target person.

The following is the list of GPS spyware: 

o SPYERA ([https://spyera.com](https://spyera.com/)) 

o mSpy ([https://www.mspy.com](https://www.mspy.com/)) 

o MobiStealth ([https://www.mobistealth.com](https://www.mobistealth.com/)) 

o FlexiSPY ([https://www.flexispy.com](https://www.flexispy.com/)) 

o EasyGPS ([https://www.easygps.com](https://www.easygps.com/))

### Anti-Spyware

▪ SUPERAntiSpyware 

Source: [https://www.superantispyware.com](https://www.superantispyware.com/)

▪ Kaspersky Total Security 20 ([https://support.kaspersky.com](https://support.kaspersky.com/)) 

▪ SecureAnywhere Internet Security Complete ([https://www.webroot.com](https://www.webroot.com/)) 

▪ Adaware Antivirus Free ([https://www.adaware.com](https://www.adaware.com/)) 

▪ MacScan ([https://www.securemac.com](https://www.securemac.com/)) 

▪ Norton AntiVirus Plus ([https://us.norton.com](https://us.norton.com/))