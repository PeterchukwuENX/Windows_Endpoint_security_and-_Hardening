# Account & Password Security Hardening

## Objective

The second phase of the Windows endpoint hardening project focused on reviewing and strengthening local account and password security controls.

The baseline assessment identified several weaknesses in the existing password policy. The configuration was subsequently hardened using built-in Windows security configuration tools and verified after implementation.

---

## Initial Assessment

The baseline identified the following configuration:

| Security Control | Initial State | Assessment |
|---|---:|---|
| Minimum password age | 0 days | No minimum age restriction |
| Maximum password age | 42 days | Configured |
| Minimum password length | 0 characters | Weak |
| Password history | 0 passwords | Password reuse not restricted |
| Password complexity | Disabled | Weak |
| Account lockout threshold | 10 attempts | Configured |
| Account lockout duration | 10 minutes | Configured |
| Lockout observation window | 10 minutes | Configured |

The primary weaknesses identified were the absence of a minimum password length, password history, and password complexity requirements.

---

## Hardening Actions

The following password security controls were implemented:

- Increased the minimum password length from **0 to 12 characters**
- Increased password history from **0 to 8 remembered passwords**
- Enabled password complexity requirements
- Retained the existing account lockout configuration

The changes were applied using Windows `secedit` and `net accounts` utilities.

---

## Verification

The resulting configuration was verified after the hardening changes were applied.

The final configuration included:

```text
Minimum password length:       12
Password history:              8
Password complexity:            Enabled
Lockout threshold:             10 attempts
Lockout duration:              10 minutes
Lockout observation window:    10 minutes
```

The exported security-policy configuration also confirmed:

```text
MinimumPasswordLength = 12
PasswordComplexity = 1
PasswordHistorySize = 8
```

---

## Evidence

### Before Hardening

<img width="1024" height="768" alt="windows-baseline png" src="https://github.com/user-attachments/assets/35da1a89-fdfd-43c7-b7f0-ecfcef95a80e" />


**Figure 1:** Initial account and password security configuration identified during the baseline assessment.

### After Hardening

<img width="1024" height="768" alt="corrected_passwordcomplexity" src="https://github.com/user-attachments/assets/92b56017-db8a-42d4-8485-6a7b3219c9aa" />



**Figure 2:** Final password-policy configuration after hardening and verification.

---

## Security Impact

The changes strengthen the endpoint's resistance to weak passwords and password reuse while maintaining the existing account lockout controls.

The phase demonstrates a complete security-control lifecycle:

**Baseline → Identify Weakness → Remediate → Verify**

Rather than changing settings without validation, the configuration was assessed before implementation and verified afterward.

---

## Tools Used

- Windows PowerShell
- `net accounts`
- `secedit`
- Windows Security Policy configuration

---

## Outcome

The account and password security phase has been completed and verified.

The endpoint now enforces:

- A **12-character minimum password length**
- **8-password history**
- **Password complexity requirements**
- Existing **10-attempt account lockout protection**

---

## Next Phase

The next phase will focus on **Microsoft Defender Endpoint Protection**.

The Defender configuration will be assessed first, followed by appropriate hardening actions and post-change verification.

**Status:** Completed
