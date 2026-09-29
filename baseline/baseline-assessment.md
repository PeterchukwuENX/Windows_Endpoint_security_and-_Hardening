# Windows Endpoint Baseline Assessment

## Objective

The first phase of this project was to establish a security baseline for the Windows 10 endpoint.

The purpose of the baseline is to understand the system's current security configuration before making any hardening changes.

This provides a reference point that can later be used to verify whether the security posture improved after hardening.

---

## Baseline Areas Assessed

The following areas were reviewed:

- Windows operating system information
- Microsoft Defender status
- Real-time protection status
- Windows Firewall configuration
- Firewall default actions
- Local account and password policy

---

## Assessment

PowerShell and built-in Windows security commands were used to collect the baseline information.

The assessment focused on identifying the current configuration rather than making any changes at this stage.

The results provide the starting point for the remaining hardening phases of the project.

---

## Evidence

The baseline assessment was captured with supporting screenshots.

<img width="1024" height="768" alt="windows-baseline png" src="https://github.com/user-attachments/assets/eed24542-a0b2-4263-a2b3-16da8d80e573" />


**Figure 1:** Initial Windows endpoint security baseline collected before hardening.

---

## Why This Matters

A security baseline provides a reference for measuring changes made during hardening.

Without a baseline, it is difficult to clearly determine:

- What the original configuration looked like
- Which security settings were changed
- Whether the changes were applied successfully
- Whether the endpoint's security posture improved

This baseline will therefore be used as the reference point for the next phases of the project.

---

## Next Phase

The next phase will focus on **Account & Password Security Hardening**.

The goal will be to review the existing configuration, identify relevant weaknesses, apply appropriate security controls, and verify the changes.

**Current Status:** Baseline completed
