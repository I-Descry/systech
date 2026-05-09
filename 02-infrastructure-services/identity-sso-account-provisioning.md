# Workflow - SSO Account Provisioning & Transfer

---

## Overview

This workflow defines the process for creating or transferring SSO (Single Sign-On) accounts for employees, including validation, dependency checks, and account delivery.

---

## Purpose

To ensure SSO accounts are properly created, assigned, and secured based on employee status and system requirements.

---

## Scope

Applies to all employees requiring SSO access, including new hires and replacement employees.

---

## Roles & Responsibility

- **IT/Admin:** Creates, transfers, and manages SSO accounts
- **HR:** Provides employee information
- **User (Employee):** Receives and uses SSO account

---

## Inputs / Requirements

Required employee information:

- Username
- Employee ID (NIK/Emp. ID)
- Title
- Full Name
- Company
- Country
- Department
- Position
- Email
- Phone (optional)
- IMEI (if applicable)
- Status

---

## Workflow Process

### 1. Information Collection

- Collect employee details from:
  - HR
  - Employee (if needed)

- Verify completeness and accuracy

---

### 2. Determine Account Type

#### Decision:

- **New Employee**
  - Create new SSO account

- ** Replacement Employee**
  - Transfer or reassign existing SSO account
  - Update all user details

---

### 3. Email Dependency Check

SSO accounts require a valid company email.

### Rule:

- If employee has **No email account** → Do NOT create or release SSO
- If email is available → Proceed

---

### 4. Account Creation / Transfer

#### For New Employee:

- Create SSO account using validated details

#### For Replacement:

- Reassign existing account
- Update user information
- Review and clean previous access if needed

---

### 5. Status Tracking

Track account status:

- Pending
- In Progress
- Completed
- On Hold (waiting for email)

---

### 6. Completion & Recording

- Record account details in internal system
- Update asset/user tracking records

---

### 7. Deliver to User

- Provide SSO access details to employee
- Share login instructions or portal link

---

## Expected Output

- SSO account successfully created or transferred
- Account linked to correct employee
- User receives  access

---

## Security Considerations

- Verify employee identity before account assignment
- Ensure previous user access is removed (for replacement)
- Do not create accounts without approved or valid data
- Protect account credentials during delivery

---

## Dependencies

- Employee email account
- HR data accuracy
- SSO system availability

---

## Common Issues

- Missing employee information
- No email account yet
- Incorrect user details
- Old access not removed (replacement case)

---

## Troubleshooting

- Verify all required fields
- Confirm email availability
- Re-check HR data
- Audit account permissions

---

## Related Documents

- Workflow → Email Account Provisioning Request
- SOP → Endpoint Provisioning
- Reference → Access Control Policy

---

## Notes

SSO provisioning is dependent on email availability and accurate employee data. Delays may occur if prerequisites are not met.

---

## Version History

| Version | Date | Changes |
|--------|------|--------|
| 1.0 | [Date] | Initial version |