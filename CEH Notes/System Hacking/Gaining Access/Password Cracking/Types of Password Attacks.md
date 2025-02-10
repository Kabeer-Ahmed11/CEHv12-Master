# Types of Password Attacks

## Non-Electronic Attacks

### Social Engineering

In computer security, social engineering is used to denote a non-technical type of intrusion that exploits human behavior. Convincing people to reveal passwords

### Shoulder Surfing

Looking at either the user’s keyboard or screen while he/she is logging in.

### Dumpster Diving

Searching for sensitive information in the user’s trash-bins, printer trash bins, and in/on the user’s desk for sticky note.

## Active Online Attacks

### Dictionary Attack

### Brute-Force Attack

### Rule-based Attack

**Hybrid Attack**

This type of attack depends on the dictionary attack. Often, people change their passwords merely by adding some numbers to their old passwords. In this case, the program would add some numbers and symbols to the words from the dictionary to try to crack the password. For example, if the old password is “system,” then there is a chance that the person will change it to “system1” or “system2.”

**Syllable Attack**

Hackers use this cracking technique when passwords are not known words. Attackers use the dictionary and other methods to crack them, as well as all possible combinations of them.

### Password Spraying Attack

CrackMapExec Source: [https://github.com](https://github.com/)

crackmapexec smb <IP> -u users.txt -p passwords.txt 

Run the following command to cross-check whether lockout occurred during the spraying process: [spray.sh](http://spray.sh/) -smb <targetIP> <usernameList> <passwordList> <AttemptsPerLockoutPeriod> <LockoutPeriodInMinutes> <DOMAIN>

The following are some additional password spraying attack tools: 

Kerbrute ([https://github.com](https://github.com/)) 

Invoke-DomainPasswordSpray ([https://github.com](https://github.com/)) 

Spray ([https://github.com](https://github.com/))  

Omnispray ([https://github.com](https://github.com/))

### Mask Attack

hashcat Source: [https://hashcat.net](https://hashcat.net/)

### Password Guessing

### Default Passwords

o [https://open-sez.me](https://open-sez.me/) 

o [https://www.fortypoundhead.com](https://www.fortypoundhead.com/) 

o [https://cirt.net](https://cirt.net/) 

o [http://www.defaultpassword.us](http://www.defaultpassword.us/) 

o [https://www.routerpasswords.com](https://www.routerpasswords.com/) 

o [https://default-password.info](https://default-password.info/) 

o [https://192-168-1-1ip.mobi](https://192-168-1-1ip.mobi/)

### Trojans/Spyware/Keyloggers

### Hash Injection/Pass-the-Hash (PtH) Attack

### LLMNR/NBT-NS Poisoning

LLMNR/NBT-NS Poisoning Tools 

o Responder Source: [https://github.com](https://github.com/)

### Internal Monologue Attack

The internal monologue attack is similar to the attack performed using Mimikatz, except that the memory area of the Local Security Authority Subsystem Service (LSASS) process is not dumped, thereby avoiding Windows Credential Guard and antivirus.

### Cracking Kerberos Password

**AS-REP Roasting (Cracking TGT)**

**Kerberoasting (Cracking TGS)**

### Pass-the-Ticket Attack

Mimikatz Source: [https://github.com](https://github.com/) 

Mimikatz allows attackers to pass Kerberos TGT to other computers and sign in using the victim’s ticket. The tool also helps in extracting plaintext passwords, hashes, PIN codes, and Kerberos tickets from memory. It is an open-source tool that enables anyone to see and store authentication data such as Kerberos tickets. Attackers can leverage this for privilege escalation and credential stealing.

### Combinator Attack

In a combinator attack, attackers combine the entries of the first dictionary with those of the second dictionary. The resultant list of entries can be used to produce full names and compound words. Attackers use this wordlist to crack a password on the target system and gain unauthorized access to the system files. 

### Fingerprint Attack

In a fingerprint attack, the passphrase is broken down into fingerprints consisting of single-and multi-character combinations that a target user might choose as his/her password. For example, for a word ‘password’, this technique would create fingerprints “p”, “a”, ”s”, ”s”, ”w”, ”o”, ”r”, “d”, “pa” , “ss”, “wo”, “rd”, etc. Attackers usually perform this attack to crack complex passwords such as “pass-10”. To perform this attack, attackers create a list of unique password hashes from a leaked password hash database, and then perform a brute-force attack to obtain a wordlist and further start the fingerprint attack.

### PRINCE Attack

A PRobability INfinite Chained Elements (PRINCE) attack is an advanced version of a combinator attack in which, instead of taking inputs from two different dictionaries, attackers use a single input dictionary to build chains of combined words. This chain can have between 1 and n words from the input dictionary concatenated together to form a chain of words. For example, if the length of characters to be guessed is 5, then the following combinations are created from the input dictionary:
5-letter word 

3-letter word + 2-letter word 

2-letter word + 3-letter word 

1-letter word + 4-letter word 

### Toggle-Case Attack

In a toggle-case attack, attackers try all possible upper-case and lower-case combinations of a word present in the input dictionary. For example, if a word in the input dictionary is “xyz”, the following set of combinations is generated: 

Xyz 

Xyz 

XYz 

XYZ 

xYz

### Markov-Chain Attack

In Markov-chain attacks, attackers gather a password database and split each password entry into two-and three-character syllables (2-grams and 3-grams); using these character elements, a new alphabet is developed, which is then matched with the existing password database.

### GPU-based Attack

Graphics processing units (GPUs) are specialized circuits used in advanced computing devices to display graphics. GPUs can also be used by web browsers to expedite application processing in data centers and cloud environments.

## Passive Online Attacks

### Wire Sniffing

### Man-in-the-Middle/Manipulator-in-the-Middle and Replay Attacks

## Offline Attacks

### Rainbow Table Attack

A rainbow table attack uses the cryptanalytic time–memory trade-off technique, which requires less time than other techniques. It uses already-calculated information stored in memory to crack the encryption. In the rainbow table attack, the attacker creates a table of all the possible passwords and their respective hash values, known as a rainbow table, in advance.

Tool to Create Rainbow Tables: 

rtgen Source: [http://project-rainbowcrack.com](http://project-rainbowcrack.com/)

### Distributed Network Attack