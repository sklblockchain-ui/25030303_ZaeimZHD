# TMS6064 Cyber Security – Assignment 1

## Disclaimer
This project is for educational purposes only. All testing was performed in a controlled lab environment using virtual machines and authorized targets.

---

## Student Name: ZAEIM HUZAIRY  
## Matric Number: 25030303
## Course: TMS6064 Cyber Security  

# Task 1: Reconnaissance
Reconnaissance, a pen tester collects preliminary information or intelligence on the
target, enabling better planning for the actual attack.

## a. nmap reconnaissance

![Nmap Screenshot 1](nmap-1.png)

![Nmap Screenshot 2](nmap-2.png)


### Target Selection

For this exercise, the loopback IP address `127.0.0.1` (localhost) was used as the scanning target. This ensures that all reconnaissance activities were conducted within a controlled and authorized lab environment without targeting external or third-party systems.## Conclusion for Nmap

Nmap is a powerful reconnaissance tool that allows penetration testers to identify open ports, detect service versions, and determine operating system information. It provides critical intelligence that supports further exploitation phases in penetration testing.

This command performs a TCP port scan to identify open or filtered ports on the target system. It helps determine which network services are exposed and may require further security assessment.


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

This command performs DNS enumeration to gather domain-related information such as name servers and record types. It is used to assess how much infrastructure information is publicly exposed.

Overall, DNSRecon provides valuable insight into domain configurations and potential exposure points, making it an important tool in reconnaissance activities.


## d. hping3 reconnaissance

Hping3 is a network packet crafting tool used during reconnaissance to send custom TCP/IP packets to a target system. It is commonly used for firewall testing, port scanning, and network diagnostics.

### Feature 1: Basic ICMP Ping
![hping3 Screenshot 1](hping3-1.png)

Feature 2 - TCP SYN Packet to Specific Port
![hping3 Screenshot 1](hping3-2.png)

Feature 2 - Scan specific port to once
![hping3 Screenshot 1](hping3-3.png)


---


## Conclusion for Hping3

Hping3 allows penetration testers to craft and send custom network packets to evaluate system responses and firewall behavior. It is useful for low-level network probing and testing port accessibility during reconnaissance.
This command sends crafted TCP SYN packets to test whether a specific port responds. It is useful for evaluating firewall behavior and network accessibility.

# Tool Comparison and Overall Conclusion

Each reconnaissance tool serves a different purpose during penetration testing:

- Nmap focuses on network scanning, port discovery, and service detection.
- Recon-ng provides structured OSINT gathering through modular domain intelligence collection.
- DNSRecon specializes in DNS enumeration and domain record analysis.
- Hping3 allows low-level packet crafting and network probing for firewall and port testing.

Nmap and DNSRecon are primarily focused on technical network enumeration. Recon-ng is more structured and suitable for organized intelligence gathering projects. Hping3 operates at a lower network layer, allowing detailed packet manipulation and testing.

Overall, combining these tools provides a comprehensive reconnaissance approach, covering port scanning, DNS analysis, OSINT collection, and packet-level testing.

# References

1. How to Install Linux on Mac. (n.d.). YouTube. https://youtu.be/bcaF1OSivYI?si=RcfSMhyXuvbSTU6a  

2. Nmap Tutorial for Beginners. (n.d.). YouTube. https://youtu.be/W7076RPIgfQ?si=DRO1e0qxH0lg2bcy  

3. Recon-ng Tutorial and Usage Guide. (n.d.). YouTube. https://youtu.be/HLf2ANp7NwM?si=XXWPM2UyA7WLrkl0  

4. DNSRecon Tutorial for Kali Linux. (n.d.). YouTube. https://youtu.be/KvMI3ICQWGY?si=ifqiH0UobfsK6x09  

5. Hping3 Tutorial and Demonstration. (n.d.). YouTube. https://youtu.be/EuLowz1aLwQ?si=BsAIrSPydh6hl1zz


# Task 2: Reconnaissance
Maintaining access, this phase requires the pen tester to continue dominating the
target system as long as possible and cause more destruction. It requires tools that can
allow stealthy behavior and under-the-ground operations.

## a. weevey
What is Weevely?
Weevely is a stealth PHP web shell used to maintain access to compromised web servers.

Step 1 - create lab directory + webshell +start php server
![weevely Screenshot 1](create.lab-1.png)
![weevely Screenshot 1](create.lab-2.png)

Step 2 - generate webshell
![weevely Screenshot 1](create.lab-3.png)

Feature Demonstrated :
![weevely Screenshot 1](shell.php-1.png)
![weevely Screenshot 1](shell.php-2.png)
![weevely Screenshot 1](shell.php-3.png)

-Remote Command Execution
Allows execution of system-level commands via URL parameters.
- Persistent Backdoor Access
As long as the webshell file remains on the server, remote access is possible.
-Lightweight Deployment
The webshell requires only a small PHP file and minimal configuration.

Conclusion for Weevely

Weevely demonstrates how attackers can maintain persistent access through web-based backdoors. By generating a password-protected PHP shell, it highlights the risks associated with insecure web server configurations.

## b. cryptcat

Tool Overview

Cryptcat is an enhanced version of Netcat that provides encrypted communication between two systems. It is commonly used in post-exploitation phases to maintain remote access securely through encrypted channels.

---

Feature 1: Display Help Menu
![cryptcat Screenshot 1](cryptcat-1.png)


Feature 2: Terminal 1 - Listerner Mode
![cryptcat Screenshot 1](cryptcat-3.png)

Feature 3: Terminal 2 - Local Encrypted Local connection
![cryptcat Screenshot 1](cryptcat-2.png)

Conclusion for Cryptcat
Cryptcat enables encrypted communication between systems, making it useful for maintaining secure access during post-exploitation activities. By configuring listener mode and encryption keys, it demonstrates how secure remote sessions can be established and maintained in a controlled lab environment.
This command starts a listener that waits for encrypted connections. It demonstrates how secure remote communication channels can be established during post-exploitation.

## c. Webshells

Webshells are commonly used in post-exploitation phases to maintain persistent access. Therefore, organizations must implement strict access controls, secure coding practices, and regular security monitoring to prevent unauthorized script execution.


Feature 1: Display Help Menu
![webshells Screenshot 1](webshell-1.png)

Note: The webshell was created and analyzed in a controlled lab environment for educational purposes only. It was not deployed to any external or unauthorized system.

Conclusion for Webshells

The webshell demonstration highlights how a simple script can be used to execute system commands remotely if uploaded to a vulnerable web server. Although the example was created in a controlled lab environment, it illustrates the serious security risks associated with improper file upload validation and insecure web server configurations.
This script demonstrates how a web-based backdoor can execute system commands if uploaded to a vulnerable server. It highlights the risks associated with improper file upload validation.

# Task 2 Tool Comparison and Conclusion

The maintaining access tools demonstrate different persistence techniques:

- Cryptcat establishes encrypted communication channels for remote access.
- Weevely generates a stealth PHP backdoor for web-based remote control.
- Webshell scripts provide simple command execution capabilities through web servers.

Cryptcat focuses on encrypted communication channels, while Weevely and Webshells target web server persistence. These tools highlight how attackers maintain long-term access after initial exploitation.

Understanding these techniques is essential for implementing proper firewall controls, web application security, and intrusion detection mechanisms.


