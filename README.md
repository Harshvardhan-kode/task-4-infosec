# task-4-infosec
## Password Authentication
Uses a username and password to log in.
### Pros:
Easy to use
Autofill makes login quick
### Cons:
People use weak or repeated passwords
Can be guessed, stolen, or hacked
Passwords may be exposed if the server is compromised
## SSH Key Authentication
Uses a pair of keys:
Public key → stored on the server
Private key → stored on your device
The server sends a challenge that only the private key can answer.
### Pros:
Very secure (long, complex keys)
Private key is never sent to the server
Hard to brute-force
### Cons:
Private key can be lost or stolen with the device
Setup and management are more complex
Requires user training and careful key handling

## Data Protection:
Data protection is the practice of keeping sensitive data safe from loss, misuse, or unauthorized access throughout its lifecycle.
It ensures data availability, integrity, and legal compliance using methods like encryption, backups, firewalls, and monitoring, 
helping organizations protect privacy, avoid legal penalties, and reduce damage from data breaches.

## Data Transformation
Data transformation is the process of converting raw data into a clear and understandable format so that important patterns, trends, and insights can be analyzed to improve processes and decision-making.
1. Data Cleaning:
Data cleaning removes errors and inconsistencies in raw data. It includes standardizing formats (such as dates), handling missing values, removing duplicate records, and correcting incorrect data to ensure accuracy.
2. Data Aggregation:
Data aggregation combines detailed data into summarized forms like totals or averages. It groups data by time, location, or other factors to make analysis simpler and faster.

## PATH Injection / PATH Hijacking
What it is:
PATH hijacking happens when an attacker places a malicious program with the same name as a legitimate command in a directory that appears earlier in the PATH.
System runs a command (e.g., python) ,OS checks directories in PATH order,Malicious file is found first Attacker’s program runs instead.
### Why it’s dangerous:
Can lead to privilege escalation
Malicious code may run with admin/root rights
Common in poorly configured systems
### Prevention:
Use absolute paths (e.g., /usr/bin/python)
Avoid insecure PATH entries
Restrict write access to system directories
