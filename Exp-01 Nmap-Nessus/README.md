# Experiment 1: Scanning for Vulnerabilities in a Network
## Objective : To identify active hosts and open ports on a target network using Nmap, and to detect known vulnerabilities on those hosts using Nessus.

## Procedure
### Step 1: Identify IP address of Kali machine

Open the terminal in the Kali Linux machine and execute:
**ifconfig**

The IP address of the Kali machine is identified as **192.168.56.102**.

---

### Step 2: Identify IP address of target machine

Open the terminal in the Metasploitable machine and identify its IP address.

The IP address of the Metasploitable machine is **192.168.56.101**.

Then, from Kali, verify the connection using:

**ping 192.168.56.101**

---

### Step 3: Verify connectivity between Kali and target machine

From the Kali terminal, send ICMP packets to the target machine using:

**ping 192.168.56.101**

The successful replies verify connectivity between the Kali and target machines.

---

### Step 4: Scan the target machine using Nmap

Use Nmap to scan the target machine and identify open ports and running services.

First, identify open ports and running services:

**nmap -sS 192.168.56.101**

Identify service version:

**nmap -sV -O 192.168.56.101**

Save the Nmap scan result:

**nmap -sV -oN nmap_scan_results.txt 192.168.56.101**

The Nmap scan identifies the open ports and available services on the target machine.

---

### Step 5: Launch Nessus

Open the Nessus web interface in a browser:

**https://localhost:8834**

Launch Nessus and proceed to the Nessus interface.

---

### Step 6: Configure and run Nessus scan

Create a new scan and enter the target IP address:

**192.168.56.101**

Save and launch the scan. Nessus analyzes the target for known security vulnerabilities.

---

### Step 7: Review Nessus vulnerability results

After the scan is completed, open the scan result. Nessus displays the vulnerabilities according to their severity, such as **Critical, High, Medium, Low and Informational**.


---

## Demo Video

[Watch the Experiment 1 Demo](demo/demo-video-link.md)
