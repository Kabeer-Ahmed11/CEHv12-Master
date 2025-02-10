# Password Recovery Tools

Elcomsoft Distributed Password Recovery 

Source: [https://www.elcomsoft.com](https://www.elcomsoft.com/)

▪ Password Recovery Toolkit ([https://accessdata.com](https://accessdata.com/)) 

▪ Passware Kit Forensic ([https://www.passware.com](https://www.passware.com/)) 

▪ hashcat ([https://hashcat.net](https://hashcat.net/)) 

▪ Windows Password Recovery Tool ([https://www.windowspasswordsrecovery.com](https://www.windowspasswordsrecovery.com/)) 

▪ PCUnlocker ([https://www.top-password.com](https://www.top-password.com/))

## Tools to Extract the Password Hashes

▪ pwdump7 Source: [https://www.tarasco.org](https://www.tarasco.org/)

▪ Mimikatz ([https://github.com](https://github.com/)) 

▪ Powershell Empire ([https://github.com](https://github.com/)) 

▪ DSInternals PowerShell ([https://github.com](https://github.com/)) 

▪ Ntdsxtract ([https://github.com](https://github.com/))
Note: The use of the above tools requires administrative privileges on the remote system.

## Password Cracking Using Domain Password Audit Tool (DPAT)

Source: [https://github.com](https://github.com/)

Steps to Crack Passwords Using DPAT 

▪ Step 1: Run the following command to dump the password hashes from the domain controller (DC). This requires sufficient space in the C drive to store the output. ntdsutil "ac in ntds" "ifm" "cr fu c:\temp" q
▪ Step 2: The dump contains two files, Active Directory\ntds.dit and registry\SYSTEM. Now, convert the output file format to the format accepted by the DPAT tool using the Python script [secretsdump.py](http://secretsdump.py/): [secretsdump.py](http://secretsdump.py/)
-system registry/SYSTEM -ntds "Active
Directory/ntds.dit" LOCAL -outputfile users This script stores the output file in the users.ntds format. -history → This flag can be included in the above command to view the password history in the report.

▪ Step 3: Create a password crack file in the format supported by the DPAT tool. The DPAT tool supports the file formats of both hashcat and John the Ripper tools.
Run the following command to crack LM hashes of users.ntds in the hashcat.pot format:
./hashcat.bin -m 3000 -a 3 users.ntds -1 ?a ?1?1?1?1?1?1?1 – increment
To crack LM hashes using John the Ripper, run the following command: john --format=LM users.ntds
▪ Step 4: Now, run the DPAT script with -h or --help arguments to view all the available options.

▪ Step 5: Next, execute the DPAT script [dpat.py](http://dpat.py/) with users.ntds and hashcat.pot as inputs. [dpat.py](http://dpat.py/) -n customer.ntds -c hashcat.pot -n → Represents hashes extracted from the domain controller (DC) -c → List of cracked passwords generated using the hashcat tool As shown in the screenshot, the output of the above command is an HTML report with clickable options, which can be opened in the default browser.

▪ Step 6: Now, click on the Details option to view more information about different passwords. For example, click on the Details option next to Password History to view the history of previously used passwords, as shown in the screenshot.

## Password-Cracking Tools

▪ L0phtCrack 

Source: [https://gitlab.com](https://gitlab.com/)

▪ ophcrack 

Source: [http://ophcrack.sourceforge.net](http://ophcrack.sourceforge.net/) 

▪ RainbowCrack 

Source: [http://project-rainbowcrack.com](http://project-rainbowcrack.com/)

▪ John the Ripper ([https://www.openwall.com](https://www.openwall.com/)) 

▪ hashcat ([https://hashcat.net](https://hashcat.net/)) 

▪ THC-Hydra ([https://github.com](https://github.com/)) 

▪ Medusa ([http://foofus.net](http://foofus.net/)) 

▪ Secure Shell Bruteforcer ([https://github.com](https://github.com/))

## How to Defend against Password Cracking

The best practices to protect against password cracking are as follows: 

▪ Enable information security auditing to monitor and track password attacks. 

▪ Do not use the same password during a password change. 

▪ Restrict the use of similar passwords and patterns for multiple accounts.

▪ Use a random string (salt) as a password prefix or suffix before performing encryption. This nullifies pre-computation and memorization. Because the salt is usually different for each individual, it is impractical for attackers to construct tables with a single encrypted version of each candidate password. Unix systems typically use a 12-bit set.
▪ Enable SYSKEY with a strong password to encrypt and protect the Security Account Manager (SAM) database. Usually, the password information of user accounts is stored in the SAM database. It is very easy for password-cracking software to target the SAM database to access passwords. SYSKEY protects password information stored in the SAM database against password-cracking software through strong encryption techniques. Encrypted passwords are more difficult to crack than unencrypted ones.
▪ Never use personal information (e.g., birth date or a spouse’s, child’s, or pet’s name) to create passwords. Otherwise, it is easy for those close to the user to crack the user’s passwords.
▪ Monitor the server logs for brute-force attacks on user accounts. Although brute-force attacks are difficult to stop, they are easily detectable if the web-server log is monitored. For each unsuccessful login attempt, an HTTP 401 status code is recorded in the web-server logs.
▪ Lockout accounts that were subjected to an excessive number of incorrect password guesses. This provides protection against brute-force and guessing attacks.
▪ Many password sniffers can be successful if a LAN manager and NTLM authentication are used. Disable LAN manager and NTLM authentication protocols only after ensuring that doing so does not affect the network.
▪ Perform a periodic audit of passwords in the organization.

▪ Check any suspicious application that stores passwords in memory or writes them to the disk.
▪ Unpatched systems can reset passwords during buffer overflow or denial-of-service (DoS) attacks. Ensure that the system is updated.
▪ Examine whether the account is in use, deleted, or disabled. Disable the user account if multiple failed login attempts are detected.
▪ Enable account lockout with a certain number of attempts, counter time, and lockout duration.
▪ One of the most effective ways to manage passwords in organizations is to set an automated password reset.

▪ Make the system BIOS password protected, particularly on devices that are susceptible to physical threats, such as servers and laptops.
▪ Train employees to thwart social engineering tactics, such as shoulder surfing and dumpster diving, which are used to steal user credentials.
▪ Configure password policies under the Group Policy object in Windows.

 ▪ Perform password screening when new passwords are created to avoid using common passwords.
▪ Use two-factor or multi-factor authentication; for example, use CAPTCHA to prevent automated attacks on critical information systems.
▪ Secure and control physical access to systems to prevent offline password attacks. 

▪ Ensure that password database files are encrypted and accessible only by system administrators.
▪ Mask the display of passwords on screen to avoid shoulder-surfing attacks. 

▪ Perform continuous user behavior analysis and blind-spot analysis. 

▪ Employ geo-lock accounts to restrict users from logging in from different locations or IP addresses.
▪ Employ programs that monitor the web for leaked passwords. Examine whether the leaked passwords are in use; if yes, change them without delay.
▪ Rename accounts with high privileges such as administrator accounts to protect against automated password-guessing programs.