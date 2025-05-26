Task 1: Scan Your Local Network for Open Ports

 Objective

To discover open ports on devices in the local network using Nmap, understand which services are exposed, and identify basic security risks.

---

 Tools Used

- Kali Linux
- Nmap – for network scanning
- Wireshark(optional) – for packet analysis
- VS Code / Mousepad – for notes and markdown editing

---

 Steps Performed

 1. Opened Terminal on Kali Linux  

---

 2. Checked if Nmap is Installed  
Command:  
which nmap

3. Found Local IP Address and Subnet
Command:
ip a
Subnet Identified: 10.0.2.0/24

4. Ran a TCP SYN Scan with Nmap
Command:
nmap -sS 10.0.2.0/24 -oN local_network_scan.txt

5. Viewed and Analyzed Scan Results
Command:
cat local_network_scan.txt

6. (Optional) Captured Packets with Wireshark
Applied filter for Nmap target IP:
ip.addr == 10.0.2.2

7. Researched Common Services

8. Identified Security Risks
Added notes in risks.md. Examples:
Port 22 (SSH) can be brute-forced if passwords are weak.
Port 445 (SMB) often targeted in ransomware attacks.
PostgreSQL should not be exposed to the internet.

 Outcome
By completing this task, I gained hands-on experience in network reconnaissance using Nmap. I also developed an understanding of:
Identifying exposed services
Researching what common ports do
Recognizing basic network security risks
