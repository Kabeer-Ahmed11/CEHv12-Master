# Maintaining Persistence

## Maintaining Persistence by Abusing Boot or Logon Autostart Executions

### Executing Logon Autostart:

Startup Folder Attackers can also inject malicious applications in the startup folder that run automatically when a user attempts to sign into their account. Attackers perform privilege escalation by manipulating the startup folder locations. 

o Abusing Startup Folder Using icacls The misconfigured locations in a startup folder can be exploited by an attacker to inject malicious payloads such as remote access Trojans (RATs) to maintain persistence. The following command is used to enumerate the permissions: icacls
Menu\Programs\Startup" 

o Using accesschk.exe for Identifying Permissions
Attackers also use accesschk.exe, which is a part of the Sysinternals tool for checking the permissions. accesschk.exe
/accepteula "C:\ProgramData\Microsoft\Windows\Start Menu\Programs\Startup”

### Executing Logon Autostart:

Registry Run Keys Attackers can conduct persistence attacks or privilege escalation if they identify a service with all the necessary permissions that is connected with the registry key. When any authorized user attempts to log in, the service link associated with the registry runs automatically. O Enumerating Assign Permissions Using WinPEAS Attackers can use the WinPEAS script to search for the possible paths that can be leveraged to perform privilege escalation within Windows. They can find permissions by executing the following command: 

winPEASx64.exe quiet applicationinfo The above command allows attackers to enumerate all permissions that are designated for a valid user against a particular service.

## Golden Ticket Attack

![image.png](Maintaining%20Persistence/image.png)

## Silver Ticket Attack

![image.png](Maintaining%20Persistence/image%201.png)