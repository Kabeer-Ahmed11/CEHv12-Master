# LDAP Enumeration

Manual LDAP Enumeration

![image.png](LDAP%20Enumeration/image.png)

![image.png](LDAP%20Enumeration/image%201.png)

![image.png](LDAP%20Enumeration/image%202.png)

![image.png](LDAP%20Enumeration/image%203.png)

![image.png](LDAP%20Enumeration/image%204.png)

Automated LDAP Enumeration

## nmap

nmap -p 389 --script ldap.base='"cn=users,dc=CEH,dc=com ldap-brute "' <Target IP Address> 

AD Explorer ([https://docs.microsoft.com](https://docs.microsoft.com/))  

LDAP Admin Tool ([https://www.ldapsoft.com](https://www.ldapsoft.com/)) 

LDAP Account Manager ([https://www.ldap-account-manager.org](https://www.ldap-account-manager.org/)) 

LDAP Search ([https://securityxploded.com](https://securityxploded.com/))

 Softerra LDAP Administrator  ([https://www.ldapadministrator.com](https://www.ldapadministrator.com/))

ldapsearch Source: [https://linux.die.net](https://linux.die.net/) 
Attackers use ldapsearch to enumerate AD users. This allows attackers to establish connections with an LDAP server to perform different searches using specific filters. The following command can be used to perform an LDAP search using simple authentication:
ldapsearch -h <Target IP Address> -x

If the above command is executed successfully, the following command can be executed to obtain additional details related to the naming contexts:
ldapsearch -h <Target IP Address> -x -s base namingcontexts
For example, from the output of the above command, if the primary domain component can be identified as DC=htb,DC=local, the following command can be used to obtain more information about the primary domain:
ldapsearch -h <Target IP Address> -x -b “DC=htb,DC=local”
The following commands can be used to retrieve information about a specific object or all the objects in a directory tree: 

ldapsearch -h <Target IP Address> -x -b "DC=htb,DC=local" '(objectClass=Employee)'→ retrieves information related to the object class Employee. 

ldapsearch -x -h <Target IP Address> -b "DC=htb,DC=local" "objectclass=*" → retrieves information related to all the objects in the directory tree. The following command retrieves a list of users belonging to a particular object class: 

ldapsearch -h <Target IP Address> -x -b "DC=htb,DC=local" '(objectClass= Employee)' sAMAccountName sAMAccountType