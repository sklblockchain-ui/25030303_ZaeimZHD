# TMS6064 Cyber Security – Assignment 1

## Disclaimer
This project is for educational purposes only. All testing was performed in a controlled lab environment using virtual machines and authorized targets.

---

## Student Name: ZAEIM HUZAIRY  
## Matric Number: 25030303
## Course: TMS6064 Cyber Security  
## Task 1: Reconnaissance
## a. nmap reconnaissance

### Command:nmap

![Nmap Screenshot 1](nmap-1.png)

![Nmap Screenshot 2](nmap-2.png)


### Target Selection

For this exercise, the loopback IP address `127.0.0.1` (localhost) was used as the scanning target. This ensures that all reconnaissance activities were conducted within a controlled and authorized lab environment without targeting external or third-party systems.## Conclusion for Nmap

Nmap is a powerful reconnaissance tool that allows penetration testers to identify open ports, detect service versions, and determine operating system information. It provides critical intelligence that supports further exploitation phases in penetration testing.


## b. recon-ng reconnaissance
Step 1 - marketplace search
![recon-ng Screenshot 1](recon-ng-1.png)

Step 2 - module install and load
![recon-ng Screenshot 1](recon-ng-2.png)

Step 3 - insert and fix domain in options + run
![recon-ng Screenshot 1](recon-ng-3.png)

The `options set SOURCE` command defines the target domain for enumeration.  
The `run` command executes the selected reconnaissance module against the specified domain.

### Conclusion for Recon-ng

Recon-ng is a modular reconnaissance framework designed for open-source intelligence (OSINT) gathering. Unlike single-command tools, Recon-ng provides a structured environment with workspaces, module management, and database integration to organize reconnaissance activities efficiently.

Through marketplace search, module installation, module loading, and execution using defined options, the framework demonstrates how reconnaissance can be conducted in a systematic and organized manner. The workspace feature further enhances project separation and data management.

Overall, Recon-ng is powerful for domain enumeration and intelligence gathering, making it highly suitable for structured penetration testing engagements.

## c. DNSrecon reconnaissance

Feature 1 - basic enumeration
![DNSrecon Screenshot 1](DNSrecon-1.png)
![DNSrecon Screenshot 1](DNSrecon-2.png)

Feature 2 - zone transfer 
![DNSrecon Screenshot 1](DNSrecon-3.png)
The zone transfer attempt failed because the DNS server does not allow unauthorized AXFR requests. This indicates proper DNS security configuration. In penetration testing, failed zone transfers are common and demonstrate that the DNS server is not misconfigured.

## Conclusion for DNSRecon

DNSRecon is an effective DNS enumeration tool used during the reconnaissance phase of penetration testing. It allows security professionals to gather critical domain information such as A records, AAAA records, name servers, and other DNS-related data.

Through basic enumeration, zone transfer attempts, and brute-force subdomain discovery, DNSRecon demonstrates how attackers may attempt to extract valuable infrastructure information from DNS servers. Even when zone transfer attempts fail, it confirms that proper security configurations are in place.

Overall, DNSRecon provides valuable insight into domain configurations and potential exposure points, making it an important tool in reconnaissance activities.



