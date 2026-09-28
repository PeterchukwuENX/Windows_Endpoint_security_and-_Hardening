# Windows Endpoint Security & Hardening Toolkit

## Project Status
**In Progress**

## Overview

This project is a practical Windows endpoint security assessment and hardening exercise.

The goal is to assess a Windows 10 endpoint, identify common security weaknesses, apply appropriate security controls, and verify that the changes improve the system's security posture.

The project follows a simple security workflow:

**BASELINE → IDENTIFY → HARDEN → VERIFY → DOCUMENT**

Rather than applying random security settings, each change will be assessed, implemented, and verified with supporting evidence.

---

## Objective

The main objectives of this project are to:

- Establish a security baseline for a Windows endpoint
- Identify weaknesses in common endpoint security configurations
- Apply practical Windows security hardening measures
- Verify that security controls are functioning as expected
- Document the process and findings
- Develop hands-on experience relevant to Security Operations and Blue Team roles

---

## Scope

The assessment will focus on five key areas:

### 1. Account & Password Security
Review and strengthen local account and password security settings.

### 2. Microsoft Defender
Review and configure endpoint protection and real-time security controls.

### 3. Windows Firewall
Review firewall profiles and strengthen inbound/outbound network protection.

### 4. PowerShell & Security Logging
Review PowerShell security configuration and enable relevant logging for improved visibility.

### 5. Windows Audit Policies
Configure security auditing to improve visibility into authentication, account, and system activity.

---

## Methodology

Each phase of the project will follow:

```text
ASSESS
   ↓
IDENTIFY WEAKNESSES
   ↓
APPLY HARDENING
   ↓
VERIFY
   ↓
DOCUMENT EVIDENCE
```

The emphasis will be on understanding **why** a security control is being applied rather than simply changing settings.

---

## Lab Environment

| Component | Configuration |
|---|---|
| Operating System | Windows 10 |
| Environment | Virtual Machine |
| User | Local administrative account |
| Primary Interface | PowerShell / Windows Security Tools |
| Purpose | Security assessment and hardening |

---

## Planned Project Phases

- [ ] Establish Windows security baseline
- [ ] Harden account and password security
- [ ] Configure Microsoft Defender
- [ ] Harden Windows Firewall
- [ ] Configure PowerShell security logging
- [ ] Configure Windows audit policies
- [ ] Perform post-hardening verification
- [ ] Document final findings and lessons learned

---

## Evidence & Documentation

Screenshots, configuration outputs, verification results, and relevant findings will be added progressively as each phase is completed.

The repository will therefore reflect the actual development of the project rather than presenting the final result without showing the process.

Each major phase will be documented using:

**Action → Evidence → Analysis → Verification**

---

## Skills Demonstrated

This project is intended to demonstrate practical experience with:

- Windows endpoint security
- Security hardening
- Microsoft Defender
- Windows Firewall
- PowerShell
- Windows security auditing
- Security logging
- Baseline assessment
- Security verification
- Technical documentation
- Blue Team security practices

---

## Project Structure

The repository will be developed progressively:

```text
Windows-Endpoint-Security-Hardening/
│
├── README.md
├── baseline/
├── hardening/
├── verification/
├── screenshots/
└── documentation/
```

Additional files and evidence will be added as each phase is completed.

---

## Security Mindset

The purpose of this project is not simply to make configuration changes.

The objective is to understand the security problem, apply an appropriate control, verify the result, and document the evidence.

**DETECT → UNDERSTAND → HARDEN → VERIFY → DOCUMENT**

---

**Project Status:** In Progress  
**Focus:** Windows Endpoint Security & Blue Team Practices
