EXPERIMENT 3: BASIC NETWORK TRAFFIC ANALYSIS WITH WIRESHARK

OBJECTIVE

To capture and examine network packets using Wireshark and identify suspicious activity and cleartext credentials within a simulated network environment.

PROCEDURE

1. Configure VM Network

Set both Kali Linux and Metasploitable network adapters to Host-Only / Internal Network.

Kali:
ip a

Metasploitable:
ifconfig

2. Install Required Packages

sudo apt update
sudo apt install nmap wireshark tcpdump tshark -y

Launch Wireshark:

sudo wireshark

EXECUTION STEPS

Step 1: Verify Connectivity

ping -c 3 192.168.56.101

Step 2: Port and Service Scanning

sudo nmap -sS -Pn 192.168.56.101

Step 3: Start Wireshark Capture

Open Wireshark and select the network interface connected to the Host-Only network. Click the blue shark fin icon to start packet capture.

Step 4: Generate Lab Traffic

HTTP:
curl http://192.168.56.101/

FTP:
ftp 192.168.56.101

Username: msfadmin
Password: msfadmin

Telnet:
telnet 192.168.56.101

Username: msfadmin
Password: msfadmin

Step 5: Filter and Analyze Traffic

Target IP:
ip.addr == 192.168.56.101

FTP credentials:
ftp.request.command == "USER" || ftp.request.command == "PASS"

Telnet:
telnet

Right-click a packet → Follow → TCP Stream

HTTP:
http

HTTP authentication:
http.authorization

Step 6: Save Capture and Export Evidence

Stop the capture and select File → Save As.

Save as:
lab_capture.pcap

To export HTTP objects:
File → Export Objects → HTTP

RESULT

Network traffic was successfully captured and analyzed using Wireshark. HTTP, FTP, and Telnet traffic were examined to demonstrate how unencrypted protocols can expose sensitive information such as usernames and passwords.
