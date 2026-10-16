# Experiment 5: ARP Spoofing and Session Hijacking

## Overview
This experiment demonstrates ARP spoofing, network traffic analysis using Wireshark, and the concept of session hijacking in a controlled virtual lab environment.

## Objective
- Understand the working of ARP spoofing (ARP poisoning).
- Capture and analyze network packets using Wireshark.
- Understand the risks of transmitting sensitive data over insecure HTTP connections.
- Study how session hijacking can occur through compromised session cookies.

## Tools and Technologies
- **Kali Linux** – Used for security testing and ARP spoofing demonstrations.
- **Metasploitable 2** – Intentionally vulnerable virtual machine used as the lab target.
- **Wireshark** – Used to capture and analyze network traffic.
- **arpspoof** – Tool used to demonstrate ARP poisoning.
- **Oracle VirtualBox** – Used to create the virtual lab environment.

## Lab Setup
The experiment uses an isolated virtual network containing:

| Component | Purpose |
|---|---|
| Kali Linux | Security testing machine |
| Metasploitable 2 | Target machine |
| Gateway | Routes network traffic |

## Procedure
1. Configure Kali Linux and Metasploitable 2 in an isolated virtual network.
2. Verify IP addresses and connectivity between the lab machines.
3. Enable IP forwarding on Kali Linux for the controlled demonstration.
4. Use `arpspoof` to demonstrate ARP poisoning between the target and gateway.
5. Start Wireshark and capture traffic on the appropriate network interface.
6. Generate test HTTP traffic from the target machine and analyze the captured packets.
7. Examine session-cookie handling using a designated test account to understand session hijacking risks.
8. Stop the demonstration and restore normal network connectivity.

## Expected Observations
- ARP poisoning can alter the ARP table entries of devices on a local network.
- Wireshark can display ARP packets and relevant HTTP traffic.
- Unencrypted HTTP traffic may expose sensitive information.
- Session cookies require proper protection to prevent unauthorized session access.

## Result
The experiment demonstrates ARP spoofing and network traffic analysis using Wireshark, while explaining the security risks associated with insecure HTTP communication and session hijacking.

## Security Measures
- Use HTTPS to encrypt web communication.
- Enable secure cookie attributes such as `Secure` and `HttpOnly`.
- Use network protections such as Dynamic ARP Inspection where supported.
- Perform security testing only in authorized, isolated lab environments.

## Conclusion
This experiment provides practical understanding of ARP spoofing, packet analysis, and session hijacking risks, highlighting the importance of secure network communication and session management.
