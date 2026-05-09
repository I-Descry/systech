# Workflow - SSO Account Provisioning & Transfer

---

## Overview

This workflow defines the process for creating or transferring SSO (Single Sign-On) accounts for employees, including validation, dependency checks, authorization configuration, and account delivery.

---

## Purpose

To ensure SSO accounts are properly created, assigned, authorized, recorded, and secured based on employee status and system requirements.

---

## Scope

Applies to all employees requiring SSO access, including new hires and replacement employees.

---

## Roles & Responsibility

- **IT/Admin:** Creates, transfers, configures, and manages SSO accounts
- **HR:** Provides employee information and coordinates onboarding
- **Supervisor:** Confirms employee legitimacy and operational requirements
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

- Verify completeness and accuracy of submitted information

---

### 2. Determine Account Type

#### Decision:

- **New Employee**
  - Create new SSO account

- **Replacement Employee**
  - Transfer or reassign existing SSO account
  - Update all user details
  - Review and clean previous access if necessary

---

### 3. Email Dependency Check

SSO accounts require a valid company email.

#### Rule:

- ❌ If employee has **No email account** → Do NOT create or release SSO
- ✅ If email is available → Proceed

---

### 4. Account Creation / Transfer

#### For New Employee

- Create SSO account using validated employee details

#### For Replacement Employee

- Reassign or transfer existing SSO account
- Update employee information
- Validate account ownership and access mapping

---

### 5. Authorization Configuration

After account creation or reassignment, configure account permissions and authorization settings.

#### Workflow Permissions

Navigate to:

- Workflow → Transaction

Enable only the required permissions:

- Approval
- Create Document
- Document Browser

> Access should follow least privilege and role-based access principles.

---

### 6. Status Tracking

Track account provisioning status:

- Pending
- In Progress
- Completed
- On Hold (waiting for email)

---

### 7. Completion & Recording

After provisioning and authorization:

- Record account details in internal system
- Update user and tracking records
- Document assigned permissions if applicable

---

#### Notification

Notify the following that SSO provisioning has been completed:

- Supervisor
- HR
- Relevant IT team members

---

### 8. Delivery to User

Provide SSO access details and login instructions.

SSO credentials or account access may be released by:

- IT/Admin
- IT Team
- Team Supervisor
- HR

depending on operational process and approval flow.

---

## Expected Output

- SSO account successfully created or transferred
- Account linked to correct employee
- Appropriate authorization configured
- Account recorded in internal system
- Employee receives access details

---

## Security Considerations

- Verify employee identity before account assignment
- Ensure previous user access is removed for replacement employees
- Do not create accounts using incomplete or unverified data
- Protect credentials during delivery
- Apply least privilege access principles

---

## Dependencies

- Employee email account
- HR data accuracy
- SSO system availability
- Internal authorization configuration

---

## Common Issues

- Missing employee information
- No email account yet
- Incorrect user details
- Old access not removed (replacement case)
- Incorrect authorization configuration

---

## Troubleshooting

- Verify all required fields
- Confirm email availability
- Re-check HR data
- Audit assigned permissions and authorization settings
- Validate account ownership and mapping

---

## Related Documents

- Workflow → Email Account Provisioning Request
- SOP → Endpoint Provisioning
- Reference → Access Control Policy

---

## Notes

SSO provisioning depends on email availability and accurate employee information. Delays may occur if prerequisites or approvals are incomplete.

---

## Version History

| Version | Date | Changes |
|--------|------|--------|
| 1.1 | [Date] | Added authorization configuration and controlled release process |
| 1.0 | [Date] | Initial version |