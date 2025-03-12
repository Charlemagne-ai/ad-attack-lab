# Active Directory Penetration Testing Lab (In Progress)

**Conducted an Active Directory penetration test within a simulated VirtualBox environment, demonstrating exploitation techniques and defensive strategies against AD-targeted attacks.**

![ad-bg](https://github.com/user-attachments/assets/b47a7624-dc81-4672-8c52-e221e491028c)


## Tools & Technologies Used
- Active Directory
- VirtualBox
- Kali Linux
- Metasploit


## Project Overview

**Status: In Progress**

This project involves building a comprehensive Active Directory penetration testing lab within a VirtualBox environment to simulate, analyze, and defend against common AD attack vectors. The lab consists of a Windows Server with Domain Controller, an attacker machine running Kali Linux, and multiple Windows client machines configured as domain members for reconnaissance and exploitation.

## Technical Implementation

The lab environment is configured with multiple network segments to facilitate various attack scenarios and defensive controls.

### Network Architecture
- **Domain Controller**: Windows Server 2019 running AD DS, DNS, and DHCP services  
- **Client Workstations**: Two Windows 10 machines joined to the domain with different security configurations  
- **Attack Machine**: Kali Linux with a comprehensive toolkit for AD penetration testing  

### Attack Vectors Implemented

#### Initial Access & Reconnaissance
- **LLMNR/NBT-NS Poisoning**: Using Responder to capture NetNTLM hashes  
- **SMB Enumeration**: Identifying shares, permissions, and vulnerable configurations  
- **User Enumeration**: Techniques for discovering valid domain accounts without authentication  
- **Network Discovery**: Passive and active techniques for mapping the AD environment  

#### Exploitation Techniques
- **Password Attacks**: Brute force, password spraying, and dictionary attacks  
- **Relay Attacks**: SMB relay and mitigation strategies  
- **Passback Attacks**: Exploiting misconfigured services  
- **LNK File Attacks**: Creating malicious shortcut files for initial access  

#### Lateral Movement & Privilege Escalation
- **Token Impersonation**: Leveraging access tokens for lateral movement  
- **Pass-the-Hash/Pass-the-Ticket**: Credential access without password knowledge  
- **Kerberoasting**: Extracting and cracking service account credentials  
- **Silver/Golden Ticket Attacks**: Creating forged Kerberos tickets  
- **GPP Attacks**: Discovering and exploiting Group Policy Preferences  

#### Post-Exploitation
- **Credential Dumping**: Using Mimikatz for extracting credentials from memory  
- **Domain Persistence**: Establishing backdoors and persistence mechanisms  
- **Domain Dominance**: Complete domain compromise techniques  

### Defense & Mitigation Strategies

For each attack vector, the lab implements corresponding defense mechanisms:

- LLMNR/NBT-NS Poisoning Mitigation via Group Policy  
- Strong SMB signing and encryption policies  
- Network segmentation and proper firewall rules  
- Multi-factor authentication implementation  
- Privileged Access Management (PAM) strategies  
- Advanced Audit Policies for early detection  
- Just-In-Time administration and temporary privileges  

## Project Goals

This project aims to:

1. Create a realistic environment for practicing AD penetration testing techniques  
2. Document the methodology and indicators of compromise for each attack  
3. Develop effective defense strategies and configuration hardening guides  
4. Demonstrate both attacker and defender perspectives for comprehensive security understanding  
5. Create practical examples of detection mechanisms for common AD attacks  

As the project progresses, I will be adding detailed documentation for each attack vector, including technical walkthroughs, detection methods, and mitigation procedures that can be applied to production environments.
