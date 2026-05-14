# Workflow - cPanel Email Password Reset

---

## Overview

This workflow defines the process for resetting employee email account passwords in cPanel when users forget their credentials.

---

## Purpose

To ensure email password reset requests are securely processed and properly communicated to authorized users.

---

## Scope

Applies to all company email accounts managed through cPanel.

---

## Roles & Responsibility

- **IT/Admin:** Performs password reset and communicates updated credentials
- **HR / Supervisor:** May coordinate or validate password reset requests
- **User (Employee):** Requests password reset and regains email access

---

## Inputs / Requirements

Required information before resetting password:

- Employee Name
- cPanel Email Address
- Department
- Identity verification or confirmation

---

## Workflow Process

### 1. Request Verification

Receive email account creation request from:

- HR
- Supervisor
- Authorized Requester

Verify the following before proceeding:

- Employee
- HR
- Supervisor

Verify the following before proceeding:

---

### 2. Access cPanel Email Management

- cPanel Dashboard → Tools
- Select **Email Accounts**

---

### 3. Search Email Account

- Use the search function to locate the employee email account
- Verify the correct email address before proceeding

---

### 4. Open Email Account Management

After locating the email account:

- Click **Manage** on the right side of the email row

---

### 5. Reset Email Password

Inside the account management page:

- Enter the company default password

Then:

- Click **Update Email Settings**

to apply the password reset.

---

### 6. Post-Reset Verification

After resetting the password:

- Confirm password update completed successfully
- Verify account remains active and accessible
- Ensure no errors occurred during reset process

---

### 7. Notify User / HR

Notify one of the following:

- Employee
- HR
- Supervisor

Inform them that:

- Password has been reset to the company default password
- User may now access the mailbox using the default credentials

---

### 8. User Password Change

Advise the employee to:

- Login using the default password
- Change password after successful login for security purposes

---

### 9. Workflow Completion

Workflow is considered complete once:

- Password reset is successfully applied
- User or authorized personnel is notified
- Employee regains mailbox access
- Internal records are updated 

---

## Expected Output

- Email password successfully reset
- User regains mailbox access
- Authorized personnel informed of password reset
- Account remains active and accessible

---

## Security Considerations

- Verify employee identity before performing password reset
- Do not disclose passwords to unauthorized individuals
- Use company-approved default password policy
- Encourage users to change password after successful login
- Avoid sending passwords through unsecured communication channels

---

## Dependencies

- cPanel administrative access
- Active email hosting service
- Correct employee email address
- Company default password policy

---

## Common Issues

- Incorrect email address provided
- User unable to login after reset
- Password not updated correctly
- Account suspended or inaccessible
- User forgot to change password after login

---

## Troubleshooting

- Reconfirm employee email address
- Retry password reset process
- Verify mailbox status in cPanel
- Test login functionality (if necessary)
- Confirm user is accessing correct webmail/login portal

---

## Related Documents

- Workflow → cPanel Email Account Provisioning
- Workflow → User Password Reset Request
- Reference → Access Control Policy

---

## Notes

Password resets should only be performed for verified users following company security procedures.

---

## Version History

| Version | Date | Changes |
|--------|------|--------|
| 1.0 | 05/14/2026 | Initial version |