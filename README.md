Active Directory Blue Team Security Lab
• Overview

This project documents a hands-on Active Directory home lab designed to simulate enterprise authentication attacks, detect malicious behavior using Windows security logs, and implement mitigations such as MFA.

• Lab Architecture

Domain Controller: Windows Server (DC01)

Client Machine: Windows 10 (CLIENT01)

Domain: lab.local

Identity Integration: Azure AD with MFA

Network: Isolated internal virtual network

• Active Directory Configuration

Created Organizational Units (IT, HR, Finance, Workstations)

Configured security groups and role-based access control

Monitored privileged group membership changes 

<img width="479" height="445" alt="image" src="https://github.com/user-attachments/assets/0240464e-b86b-4bb4-9620-d33be8a3c92b" />


• Security Auditing & Logging

Enabled advanced audit policies to log:

4624 – Successful logons

4625 / 4771 – Failed authentication attempts

4728 – Privileged group membership changes

4740 – Account lockouts

Logs were analyzed using Event Viewer to identify attack patterns. 

<img width="510" height="382" alt="image" src="https://github.com/user-attachments/assets/59eba043-2bba-4b9b-91fa-9b0b5c1fa97a" />


• Attack Simulations

Password spraying across multiple domain users

Brute-force authentication attempts

Privilege escalation via group modification

Account lockout scenarios

<img width="816" height="632" alt="image" src="https://github.com/user-attachments/assets/3805bc69-1ed4-4aa4-bca9-37e7c6eb75c1" />


• Detection & Analysis

Identified password spraying through log correlation:

Multiple users

Same source IP

Grouped timestamps

Investigated account lockouts and escalation events

Differentiated normal system activity from malicious behavior

• Mitigations Implemented

Integrated Azure AD MFA to protect domain accounts

Applied account lockout policies

Demonstrated how MFA mitigates credential-based attacks

• Skills Demonstrated

Active Directory administration

Windows authentication internals

Security event analysis

Blue team detection logic

Identity security & MFA implementation
