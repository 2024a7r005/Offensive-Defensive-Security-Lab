# Password Guessing with Hydra

## Aim
To understand brute-force attacks by using Hydra to test simple passwords on an SSH or FTP service in a controlled lab environment.

## Tools Used
- Kali Linux
- THC Hydra
- SSH or FTP Service
- Password Wordlist

## Introduction
Hydra is a password-testing tool used to identify weak login credentials. It attempts multiple username and password combinations against services such as SSH and FTP using a wordlist.

## Procedure

1. Open the Kali Linux terminal.
2. Check the system's IP address using:
   ```bash
   ip a
   ```
3. Verify that Hydra is installed:
   ```bash
   hydra -h
   ```
4. Create a sample password wordlist:
   ```bash
   nano passwords.txt
   ```
5. Add a few test passwords, save the file and exit.
6. Identify the IP address of your authorized lab target and confirm that its SSH or FTP service is running.
7. Run Hydra against the lab service. For SSH, use:
   ```bash
   hydra -l testuser -P passwords.txt ssh://TARGET_IP
   ```
8. For FTP, use:
   ```bash
   hydra -l testuser -P passwords.txt ftp://TARGET_IP
   ```
9. Observe the terminal output to check the login attempts and whether a matching password is found.
10. Record the results and understand how weak passwords can make accounts vulnerable.

*Replace `TARGET_IP` and `testuser` with the details of your authorized lab machine and test account.*

## Result
Successfully explored password-guessing attacks using Hydra and understood how weak passwords can be identified.

## Security Measures
- Use strong and unique passwords.
- Enable Multi-Factor Authentication (MFA).
- Implement account lockout policies.
- Restrict repeated login attempts.
- Use SSH key-based authentication where possible.

## Conclusion
This experiment demonstrated how Hydra tests login credentials and highlighted the importance of strong passwords and secure authentication practices.

**Note:** Perform password testing only on systems for which you have permission.
