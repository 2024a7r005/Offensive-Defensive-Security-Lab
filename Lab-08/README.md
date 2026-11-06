
# Mapping Threats with MITRE ATT&CK

## Aim
To analyse a simulated FTP exploitation attack performed using Metasploit, map the observed attack techniques to the MITRE ATT&CK framework and recommend suitable security mitigations.

## Tools Used
- Kali Linux
- Metasploit Framework (MSFconsole)
- MITRE ATT&CK Framework
- Vulnerable Virtual Machine

## Experiment Overview
This experiment analyses a simulated VSFTPD 2.3.4 FTP exploitation scenario performed using Metasploit. The observed attack activities are studied and mapped to the MITRE ATT&CK framework to understand attacker techniques and possible security risks.

## MITRE ATT&CK Mapping
- **Tactic:** Initial Access
- **Technique:** Exploit Public-Facing Application
- **Technique ID:** T1190

## Procedure
1. Open MSFconsole in Kali Linux.
2. Search for the VSFTPD 2.3.4 vulnerability.
3. Select the appropriate exploit module.
4. Configure the target IP address and FTP port.
5. Execute the exploit in a controlled virtual environment.
6. Observe the resulting command session.
7. Visit the MITRE ATT&CK website.
8. Identify the relevant attack technique and study its mitigations.

## Recommended Mitigations
- Update vulnerable FTP services.
- Disable unnecessary services.
- Use secure file transfer protocols such as SFTP.
- Apply firewall restrictions.
- Monitor suspicious network activities.
- Follow least-privilege access policies.

## Result
Successfully analysed a simulated FTP exploitation attack and mapped the relevant technique to the MITRE ATT&CK framework. Identified suitable security measures to reduce similar threats.

## Reference
https://attack.mitre.org/
