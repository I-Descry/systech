# Workflow - User Password Reset Request

---

## Overview

This workflow defines the process for handling employee password reset, requests, including validation, reset procedures, notification, and credential release.

---

## Purpose

To ensure password reset requests are securely validated, properly processed, and accurately communicated to authorized personnel and users.

---

## Scope

Applies to all employees requesting password reset assistance for company-managed accounts or systems.

---

## Roles & Responsibility

- **IT/Admin:** Validates request, performs password reset, and communicates updates
- **Supervisor:** Receives notification regarding password reset activity
- **HR:** Receives password reset message from IT/Admin Team or Supervisor telling its done
- **User (Employee):** Requests password reset and receives updated credentials

---

## Inputs / Requirements

Required information before processing reset:

- Employee Name
- Employee ID
- Username / Account
- System or application affected

---

## Workflow Process

### 1. Request Verification

- Receive password reset request from employee
- Verify employee identity and account ownership

---

### 2. Initial Credential Validation

Before resetting the password:

#### Attempt 1

- Test if the account still accepts the default password

#### Attempt 2

- Ask user to verify and retry previously changed password (maybe capslock is on or wrong input)

---

#### Decision

- Password works → No reset required
- Password still invalid → Proceed with password reset

---

### 3. Password Reset

- Perform password reset through system/application
- System automatically applies the default password

> Password reset is completed through built-in reset functionality.

---

### 4. Status Tracking

Track reset request status:

- Pending
- In Progress
- Completed
- Cancelled

---

### 5. Completion & Recording

After successful reset:

- Record reset activity if required
- Update internal tracking records if applicable

---

#### Notification

Notify the following that the password has been reset:

- IT Team
- Supervisor
- HR

if operationally required.

---

### 6. Credential Release

- Provide updated credentials or default password to the requesting employee
- Ensure credentials are only released to verified account owner

---

## Expected Output

- Password successfully reset
- User regain account access
- Relevant teams informed of reset activity

---

## Security Considerations

- Verify user identity before resetting password
- Avoid releasing credentials to unauthorized individuals
- Do not expose password publicly
- Encourage user to change password after login if applicable

---

## Dependencies

- Account management system
- user identity verification
- Password reset functionality

---

## Common Issues

- User forgot updated password
- Incorrect username/account
- User unable to access account after reset
- Account locked or disabled

---

## Troubleshooting

- Reconfirm username and employee identity
- Retry reset process
- Verify account status
- Escalate system-related issues if necessary

---

## Related Documents

- Workflow → SSO Account Provisioning & Transfer
- Workflow → Email Account Provisioning Request
- Reference → Access Control Policy

---

## Notes

Password resets should only be performed for verified users and according to company access control policies.

---

## Version History

| Version | Date | Changes |
|--------|------|--------|
| 1.0 | 05/09/2026 | Initial version |