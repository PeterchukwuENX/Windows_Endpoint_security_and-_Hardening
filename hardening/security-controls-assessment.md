# Windows Security Controls Assessment

## Overview

Following the initial Windows endpoint baseline and account/password hardening phase, additional security controls were assessed to determine the existing security posture of the endpoint.

The assessment focused on four areas:

- Microsoft Defender
- Windows Firewall
- PowerShell logging
- Windows security auditing

The objective was not to change every configuration encountered. Each control was reviewed first, and changes were only considered where a security gap was identified.

This approach follows a practical defensive-security principle:

**Assess → Identify → Remediate → Verify**

---

# 1. Microsoft Defender

## Objective

Verify that core Microsoft Defender protections were enabled and providing endpoint protection.

## Assessment

The following Defender controls were reviewed:

- Antivirus protection
- Real-time protection
- Behavior monitoring
- IOAV protection
- Antispyware protection

The assessment confirmed that the reviewed Defender protections were enabled.

Because the controls were already active, no unnecessary configuration changes were made.

## Evidence

<img width="1024" height="768" alt="Windows_Defender" src="https://github.com/user-attachments/assets/3e95b7e2-c2a0-4431-8fdf-f5e4ff53d4ed" />

**Figure 1:** Microsoft Defender protection status verified through PowerShell.

## Result

**Status: Verified**

The endpoint had the assessed Defender protection mechanisms enabled.

---

# 2. Windows Firewall

## Objective

Review the Windows Firewall profiles and determine whether the endpoint firewall was active.

## Assessment

The following firewall properties were reviewed:

- Firewall profile status
- Default inbound action
- Default outbound action

The assessment confirmed that the Windows Firewall profiles were enabled.

The configuration was documented rather than making unnecessary changes without a clearly identified security requirement.

## Evidence

<img width="1024" height="768" alt="Firewall_status" src="https://github.com/user-attachments/assets/187b3997-aedb-43f6-8511-8c44f911c932" />


**Figure 2:** Windows Firewall profile configuration reviewed through PowerShell.

## Result

**Status: Verified**

Windows Firewall was enabled across the assessed profiles.

---

# 3. PowerShell Security Logging

## Objective

Verify that PowerShell-related logging was available for security monitoring and investigation.

PowerShell is frequently used by administrators and can also be abused by attackers. Maintaining useful logging therefore improves endpoint visibility and supports investigation of suspicious activity.

## Assessment

PowerShell-related Windows event logs were reviewed using:

```powershell
Get-WinEvent -ListLog *PowerShell* | Select-Object LogName,IsEnabled
```

The assessment confirmed that the relevant PowerShell logging configuration was enabled.

No unnecessary changes were made after verification.

## Evidence

<img width="1024" height="768" alt="powershell" src="https://github.com/user-attachments/assets/665aff26-36ea-437a-9f5c-65340f377b66" />


**Figure 3:** PowerShell-related event logging status verified through PowerShell.

## Result

**Status: Verified**

The assessed PowerShell logging capabilities were enabled and available for security visibility.

---

# 4. Windows Security Audit Policy

## Objective

Review Windows security auditing to determine whether security-relevant system activity was being audited.

Audit policies are important for defensive monitoring because they provide telemetry that can support the investigation of authentication, account management, policy changes, process activity, and other security events.

## Assessment

Windows audit policy was reviewed using:

```powershell
auditpol /get /category:*
```

The assessment reviewed security auditing categories including:

- Account management
- Logon and logoff
- Policy change
- Process-related activity
- System events

The resulting configuration was reviewed as part of the endpoint visibility assessment.

## Evidence

<img width="1024" height="768" alt="Windows" src="https://github.com/user-attachments/assets/9a6ea61e-c0a7-4d17-9f5f-486f045a5965" />


**Figure 4:** Windows security audit policy reviewed using the built-in `auditpol` utility.

## Result

**Status: Assessed**

The endpoint's Windows auditing configuration was reviewed and documented as part of the security assessment.

---

# Assessment Summary

| Security Area | Action | Result |
|---|---|---|
| Microsoft Defender | Configuration assessed | **Verified enabled** |
| Windows Firewall | Profiles assessed | **Verified enabled** |
| PowerShell Logging | Logging configuration assessed | **Verified enabled** |
| Windows Audit Policy | Audit configuration reviewed | **Assessed** |

---

# Security Approach

A key objective of this phase was to avoid making configuration changes simply for the appearance of hardening.

Existing security controls were first assessed.

Where controls were already providing the expected protection, they were documented and verified rather than unnecessarily modified.

This produced a more accurate endpoint assessment:

**Not every security control needs to be changed. Some need to be verified.**

---

# Skills Demonstrated

This phase demonstrates practical experience with:

- Windows endpoint security assessment
- Microsoft Defender verification
- Windows Firewall assessment
- PowerShell security logging
- Windows audit policy
- PowerShell-based security checks
- Security evidence collection
- Security configuration analysis
- Technical documentation

---

# Overall Result

The Windows endpoint was assessed across multiple layers of defensive security.

The account and password phase addressed identified password-policy weaknesses, while Microsoft Defender, Windows Firewall, PowerShell logging, and Windows auditing were assessed to establish the existing security posture.

The result is a documented endpoint security assessment showing the progression from:

**BASELINE → IDENTIFY → HARDEN → VERIFY → DOCUMENT**

**Assessment Status: Completed**
