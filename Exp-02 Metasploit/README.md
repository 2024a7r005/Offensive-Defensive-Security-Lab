# Experiment 2: Simulated Ethical Hacking with Metasploit

## Objective:To perform a safe exploitation of a vulnerable virtual machine using Metasploit and understand the basic ethical hacking procedure.

## Procedure
### Step 1: Start Virtual Machines

Start the Kali Linux and Metasploitable virtual machines and ensure they are connected to the same virtual network.

---

### Step 2: Identify Target IP Address

Determine the IP address of the Metasploitable machine using **ifconfig**.

The IP address of the target machine is identified from the Metasploitable machine.

---

### Step 3: Use Nmap to Identify Open Ports and Available Services

Use Nmap from the Kali Linux machine to identify open ports and available services.

**nmap -sV 192.168.56.102**

---

### Step 4: Launch Metasploit Framework

Open the Metasploit console using **msfconsole**.

---

### Step 5: Search for a Suitable Exploit

Search the Metasploit database for an exploit corresponding to a vulnerable service on the target.

**search vsftpd**

---

### Step 6: Select and Configure Exploit

Select the required exploit and configure the target IP address.

**use exploit/unix/ftp/vsftpd_234_backdoor**

Configure the required exploit options, including the target and port.

**RPORT: 21**

---

### Step 7: Execute Exploit

Run the exploit against the authorized Metasploitable virtual machine.

**exploit**

---

### Step 8: Verify the Result

Observe the Metasploit output and verify whether a session was successfully established.

---
