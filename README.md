## Internship Lab Report (Task 3)
----
### Company: ApexPlanet Software Pvt. Ltd.
### Intern ID: APSPL2520241
## Objective
This project demonstrates hands-on exploitation of a classic SQL Injection vulnerability using the Damn Vulnerable Web Application (DVWA) platform. It also covers extraction and recovery of user password hashes, followed by successful cracking of those hashes using CrackStation.

### Steps Demonstrated

- *SQL Injection on DVWA:*  
  The DVWA "Vulnerability: SQL Injection" module was used to perform standard SQL injection attacks. Various payloads such as ' OR 1=1 -- and UNION SELECT were utilized to bypass authentication and extract user data, including usernames and hashed passwords.

- *Hash Extraction:*  
  The UNION SELECT payloads enabled the extraction of password hashes from the backend database, shown directly in the web application's output.

- *Password Hash Cracking:*  
  Extracted password hashes (MD5) were input into the CrackStation online hash cracker. The tool successfully resolved example hashes (e.g., 0d107d09f5bbe40cade3de5c71e9e9b7 to letmein, 8d3533d75ae2c3966d7e0d4fcc69216b to charley), demonstrating the risk posed by unsalted and weak hashing algorithms.

### Screenshots Included

1. *CrackStation hash cracking results*  
   Shows MD5 hashes being cracked to their plain-text equivalents.
2. *DVWA SQL Injection in action*  
   Multiple exploitation steps, including different payloads and resulting extracted data and hashes.

### Key Takeaways

- SQL Injection can expose sensitive authentication data if input sanitization is missing.
- Weak, unsalted hashes (like MD5) can be trivially cracked using freely available online tools.
- These exercises highlight the critical importance of secure coding practices and robust password hashing mechanisms (e.g., salted hashes with bcrypt or Argon2).
