# Workflow - cPanel Email Account Provisioning

---

## Overview

This workflow defines the process for creating employee email accounts in cPanel, including request handling, account creation, credential setup, and user notification.

---

## Purpose

To ensure standardized, secure, and trackable creation of company email accounts for employees using the cPanel administration dashboard.

---

## Scope

Applies to all employees who require a company email account hosted in cPanel for business communication.

---

## Roles & Responsibility

- **IT/Admin:** Creates and manages email accounts in cPanel
- **HR / Supervisor:** Requests or validates employee email requirement
- **Employee (User):** Receives and uses the email account credentials

---

## Inputs / Requirements

Required information before creating email account:

- Username (email prefix)
- Employee Full Name
- Department
- Requested Email Purpose (optional)
- Default Password Policy
- Account Status (New / Active Employee)

---

## Workflow Process

### 1. Request Initiation

- Receive email account request from HR, Supervisor, or employee
- Verify if the request is valid and required for business use
- Confirm employee identity and employment status

---

### 2. Validation & Approval

- Check if employee is authorized for company email access
- Confirm availability of username/email format

#### Decision:

- **Approved** → Proceed to creation
- **Rejected** → Inform requester and close request

---

### 3. Email Account Creation (cPanel)

- cPanel Dashboard → Tools
- Select **Email Accounts**
- Click **Create**

Then:

- Enter Username
- Domain is auto-assigned (company domain already configured)
- Set Password (use default company password policy)
- Set mailbox storage limit
- Click **Create**

---

### 4. Post-Creation Verification

- Confirm email account appears in the email list
- Monitor login access of the created account
- Verify that the employee can successfully log in and access the mailbox
- Ensure mailbox is active and functioning properly

---

### 5. Credential Handling

- Use default password policy for initial setup
- Ensure credentials are stored securely before delivery
- Avoid sending credentials through unsecured channels

---

### 6. Completion & Recording

- Email account creation is manually recorded for reference
- Record:
  - Email address
  - Employee name
  - Date created
  - Created by (IT/Admin)

---

### 7. Delivery to User

Notify one of the following:

- Employee directly
- Supervisor
- HR

Provide:

- Email address
- Default Password
- Login instructions

> User may be required to change password on first login depending on policy

---

## Expected Output

- Company email account successfully created in cPanel
- Account linked to correct employee
- Credentials securely delivered
- Employee successfully able to access email account

---

## Security Considerations

- Use strong default password policy
- Do not reuse passwords across users
- Ensure credentials are shared securely
- Verify identity before releasing access
- Apply least privilege principles where applicable

---

## Dependencies

- cPanel access (Admin level)
- Active company domain configuration
- HR-approved employee data
- Hosting/email service availability

---

## Common Issues

- Username already exists
- Domain misconfiguration
- Email account limit reached
- Incorrect employee details
- Login issues after creation

---

## Troubleshooting

- Verify username uniqueness
- Check domain configuration in cPanel
- Reset password if login fails
- Confirm account status in cPanel
- Coordinate with hosting provider if issues persist

---

## Related Documents

- SOP → Email Hosting Management
- Workflow → Employee Onboarding Process
- Reference → IT Access Control Policy

---

## Notes

Email accounts must only be created for verified employees. All accounts must follow company naming conventions and security standards.

---

## Version History

| Version | Date | Changes |
|--------|------|--------|
| 1.2 | 05/13/2026 | Improved workflow structure, verification process, credential handling, and internal recording details |
| 1.1 | 05/13/2026 | Updated verification and removed formal status tracking system |
| 1.0 | 05/13/2026 | Initial version |