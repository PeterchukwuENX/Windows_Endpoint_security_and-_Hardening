# Windows Endpoint Security & Hardening Toolkit

## Project Status

**Completed**

## Overview

This project is a practical Windows endpoint security assessment and hardening exercise.

The objective was to assess the security configuration of a Windows 10 endpoint, identify relevant weaknesses, apply appropriate security controls, and verify the resulting configuration.

The project followed the workflow:

**BASELINE → IDENTIFY → HARDEN → VERIFY → DOCUMENT**

Rather than making arbitrary configuration changes, the endpoint was assessed first so that security decisions could be based on the system's existing configuration.

---

## Objectives

The project was designed to:

- Establish a Windows endpoint security baseline
- Identify weaknesses in local account and password configuration
- Review Microsoft Defender protection
- Review Windows Firewall configuration
- Review PowerShell logging
- Review Windows security auditing
- Apply appropriate hardening controls
- Verify security changes after implementation
- Document the process using configuration evidence and screenshots

---

## Lab Environment

| Component | Configuration |
|---|---|
| Operating System | Windows 10 |
| Environment | Virtual Machine |
| Administrative Interface | PowerShell |
| Assessment Type | Endpoint Security Assessment & Hardening |
| Primary Focus | Windows Blue Team / Defensive Security |

---

# Assessment Methodology

Each security area was approached using:

```text
        BASELINE
            │
            ▼
   IDENTIFY WEAKNESSES
            │
            ▼
      APPLY CONTROLS
            │
            ▼
         VERIFY
            │
            ▼
        DOCUMENT
```

This approach provided a clear before-and-after view of the endpoint's security configuration.

---

# 1. Baseline Assessment

The initial assessment established the starting security posture of the Windows endpoint.

The baseline included reviews of:

- Windows system information
- Microsoft Defender status
- Windows Firewall profiles
- Local account and password policy
- PowerShell logging
- Windows audit policy

### Key Finding

The password policy contained several weaknesses, including:

- Minimum password length: **0**
- Password history: **0**
- Password complexity: **Disabled**

These findings became the primary remediation targets for the account and password security phase.

Additional security controls were also reviewed to determine whether remediation was necessary.

[View the baseline assessment](baseline/baseline-assessment.md)

---

# 2. Account & Password Security

The account and password security phase focused on strengthening local password-policy controls.

### Changes Implemented

| Control | Initial State | Final State |
|---|---:|---:|
| Minimum password length | 0 | **12** |
| Password history | 0 | **8** |
| Password complexity | Disabled | **Enabled** |
| Lockout threshold | 10 attempts | **10 attempts** |
| Lockout duration | 10 minutes | **10 minutes** |
| Lockout observation window | 10 minutes | **10 minutes** |

The changes were applied using Windows built-in security configuration tools and subsequently verified.

[View account & password hardening](hardening/account-password-security.md)

---

# 3. Microsoft Defender

Microsoft Defender configuration was assessed as part of the endpoint security review.

The following controls were verified:

- Antivirus protection
- Real-time protection
- Behavior monitoring
- IOAV protection
- Antispyware protection

The assessed Defender controls were already enabled, so unnecessary configuration changes were avoided.

This demonstrates an important security principle:

> **Not every control requires modification. Assess first, then remediate where necessary.**



---

# 4. Windows Firewall

Windows Firewall profiles were reviewed to determine their current configuration and protection status.

The assessment included:

- Firewall profile status
- Inbound default action
- Outbound default action

The firewall configuration was documented as part of the assessment rather than making unnecessary changes without sufficient evidence that remediation was required.



---

# 5. PowerShell Security Logging

PowerShell-related logging was reviewed to determine whether relevant logging capabilities were enabled.

The assessment confirmed that the relevant PowerShell logging configuration was enabled.

No unnecessary changes were made after verification.


---

# 6. Windows Audit Policy

Windows audit policy was reviewed using the built-in Windows auditing tools.

The assessment focused on security-relevant auditing categories including:

- Logon and logoff activity
- Account management
- Policy changes
- Process-related activity
- System events

The audit configuration was reviewed as part of the endpoint visibility assessment.


---

# 7. Verification

After the configuration changes and security reviews were completed, the endpoint was checked again to confirm the resulting configuration.

The verification stage focused on confirming that:

- Password hardening changes were applied
- Microsoft Defender protection remained enabled
- Windows Firewall profiles were enabled
- PowerShell logging was enabled
- Windows security auditing had been reviewed



---

# Evidence

Screenshots were captured throughout the assessment and remediation process.

The evidence demonstrates:

**Initial Configuration → Security Finding → Remediation → Verification**

Screenshots are organized according to the phase in which they were collected.

---

# Tools Used

- Windows PowerShell
- `net accounts`
- `secedit`
- `Get-MpComputerStatus`
- `Get-NetFirewallProfile`
- `Get-WinEvent`
- `auditpol`

---

# Skills Demonstrated

### Endpoint Security
- Windows security configuration
- Endpoint hardening
- Security baseline assessment
- Security control verification

### Blue Team / SOC
- Security configuration assessment
- Identification of security weaknesses
- Security telemetry awareness
- Windows logging
- Audit policy review
- Evidence collection

### Technical Skills
- PowerShell
- Windows security utilities
- Configuration analysis
- Technical documentation

---

# Key Lessons Learned

This project reinforced several practical security principles:

1. **Establish a baseline before making security changes.**
2. **Do not change controls simply for the sake of hardening.**
3. **Verify security changes after implementation.**
4. **Use evidence to support security findings.**
5. **Document both secure configurations and weaknesses.**
6. **Separate assessment from remediation.**

---

# Project Outcome

The Windows endpoint was assessed across multiple security areas, with identified password-policy weaknesses remediated and other existing security controls verified.

The project demonstrates a practical endpoint-security workflow from initial assessment through remediation, verification, and documentation.

---

## Security Workflow

**ASSESS → IDENTIFY → HARDEN → VERIFY → DOCUMENT**

**Status: Completed**
