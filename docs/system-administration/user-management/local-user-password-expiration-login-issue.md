# Local User Account Password Expiration Issue - Login Failure

## Overview

A user was unable to log in to their local Windows account due to password expiration policy enforcement.

---

## Issue Description

The user reported login failure when attempting to access their workstation. The system indicated authentication failure, and the account required a password change due to expiration.

The local account was configured with a password expiration policy, which caused the login issue when the password reached its expiration period.

---

## Scope / Impact

- **Affected:** Single User Workstation
- **System:** Windows Desktop (Local Account)
- **Configuration:** Local security policy / account password expiration enabled
- **Impact:** User unable to log in due to expired password requirement

---

## Analysis / Troubleshooting Steps

- Verified user login failure at Windows sign-in screen
- Confirmed system is using a local account (not domain-joined)
- Checked for password expiration behavior
- Identified that the account password had reached its expiration period
- Confirmed that password expiration policy is enabled for the local user account
- Determined that login failure was caused by expired password enforcement

---

## Resolution

- Logged in using administrative priviledges (hidden Administrator account)

---

### 1. Primary Method (CMD - Standard Approach)

- Reset user password using Command Prompt:
```cmd
net user USERNAME newpassword
```
- Verified password reset completed successfully

### 2. Check Password Expiration Status

- Verified account policy using PowerShell:
```powershell
Get-LocalUser -Name "USERNAME" | Select-Object Name, PasswordExpires, PasswordRequired
```

### 3. Disable Password Expiration (Fallback Method - Powershell)

- If CMD or legacy tools are insufficient, use:
```powershell
Set-LocalUser -Name "USERNAME" -PasswordNeverExpires $true
```

### 4. Legacy Method (Deprecated / Not Recommended)
- WMIC method (may not work on modern Windows versions):
```cmd
wmic useraccount where name="USERNAME" set PasswordExpires=False
```
- Logged out from Administrator account
- Logged back in using updated credentials

---

## Outcome

- User successfully regained access to the system
- Login issue resolved after password reset
- Password expiration no longer affects the account

---

## Root Cause

Local user account had password expiration enabled, and the password reached its expiration period, causing login failure until reset.

---

## Recommendations

- Use CMD (`net user`) as primary method for password reset
- Use PowerShell (`Set-LocalUser`) for modern Windows systems
- Avoid relying on deprecated WMIC commands
- Review password expiration policies on standalone systems
- Disable expiration for non-managed local accounts if not required
- Apply password policies only in domain-managed environments
- Maintain at least one administrative recovery account

---

## Notes

- WMIC is deprecated and may not work on newer Windows versions
- Preferred modern method is PowerShell `Set-LocalUser`
- Password policies are managed via Local Security Policy or system configuration
- Applies only to local accounts, not domain accounts
- Hidden Administrator account was used for recovery access