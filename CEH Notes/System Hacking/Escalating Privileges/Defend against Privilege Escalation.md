# Defend against Privilege Escalation

▪ Restrict interactive logon privileges. 

▪ Run users and applications with the lowest privileges. 

▪ Implement multi-factor authentication and authorization. 

▪ Run services as unprivileged accounts. 

▪ Implement a privilege separation methodology to limit the scope of programming errors and bugs.
▪ Use an encryption technique to protect sensitive data. 

▪ Reduce the amount of code that runs with a particular privilege. 

▪ Perform debugging using bounds checkers and stress tests. 

▪ Thoroughly test the system for application coding errors and bugs. 

▪ Regularly patch and update the kernel. 

▪ Change UAC settings to “Always Notify” to increase the visibility of the user when UAC elevation is requested.
▪ Restrict users from writing files to the search paths for applications. 

▪ Continuously monitor file-system permissions using auditing tools. 

▪ Reduce the privileges of user accounts and groups so that only legitimate administrators can make service changes.

▪ Use whitelisting tools to identify and block malicious software that changes file, directory, or service permissions.
▪ Use fully qualified paths in all Windows applications. 

▪ Ensure that all executables are placed in write-protected directories. 

▪ In macOS, prevent plist files from being altered by users by making them read-only. 

▪ Block unwanted system utilities or software that may be used to schedule tasks. 

▪ Regularly patch and update the web servers. 

▪ Disable the default local administrator account. 

▪ Detect, repair, and fix any flaws or errors running in the system services. 

▪ Keep the files read-only and provide write access to only the users and groups that require it.
▪ Incorporate the provisioning and de-provisioning of accounts to prevent the hijacking of orphaned accounts.
▪ Enable Data Execution Prevention (DEP) in Windows systems to block any executable code request.

## Defend against the Abuse of sudo Rights

▪ Implement a strong password policy for sudo users. 

▪ Turn off password caching by setting timestamp_timeout to 0 so that users must input their password every time sudo is executed.
▪ Separate sudo-level administrative accounts from the administrator’s regular accounts to prevent theft of sensitive passwords.
▪ Update user permissions and accounts at regular intervals. 

▪ Test sudo users with access to programs containing parameters for arbitrary code execution.

## Defend against DCSync Attacks

The following are the best countermeasures to defend against DCSync attacks: 

▪ Examine the permissions assigned to the users and administrators. Keep track of the accounts that request domain replication rights.
▪ Conduct security awareness training on the system configuration, system patch management, threat detection, and response systems.
▪ Deploy network surveillance tools such as Sean Metcalf and StealthDEFEND to accumulate DC IP addresses and decide which IP addresses need to be included in the replication list.

## Defend against PPID Spoofing

▪ Verify PPID fields where information is stored to detect irregularities. 

▪ Identify the legitimate parent process using the event header PID specified by ETW. 

▪ Periodically analyze Windows API calls such as CreateProcess for malicious PIDs. 

▪ Monitor system API calls exclusively assigning PPIDs to new processes.

## Defending against Spectre and Meltdown Vulnerabilities

▪ Regularly patch and update OSs and firmware 

▪ Enable continuous monitoring of critical applications and services running on the system and network
▪ Regularly patch vulnerable software such as browsers 

▪ Install and update ad-blockers and anti-malware software to block injection of malware through compromised websites
▪ Enable traditional protection measures such as endpoint security tools to prevent unauthorized system access
▪ Block services and applications that allow unprivileged users to execute code. 

▪ Never install unauthorized software or access untrusted websites from systems storing sensitive information
▪ Use data loss prevention (DLP) solutions to prevent leakage of critical information from runtime memory
▪ Frequently check with the manufacturer for BIOS updates and follow the instructions provided by the manufacturer to install the updates