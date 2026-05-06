# Workflow - Email Account Provisioning Request (External)

---

## Overview

This workflow defines the process for requesting and provisioning employee email accounts (Exchange) through an external IT team.

---

## Purpose

To ensure that email account requests are properly validated, approved, tracked, and delivered before provisioning.

---

## Scope

Applies to employees requiring company email accounts, subject to eligibility, approval, and external processing.

---

## Roles & Responsibility

- **Requester (User / Department):** Initiates request
- **IT/Admin:** Collects information, validates, submits, and monitors the request
- **Approver (Supervisor / Manager):** Confirms if employee is eligible for email access
- **External SysAdmin Team:** Processes and creates the email account

---

## Inputs / Requirements

Required employee information:

- Full Name
- Employee ID
- Position
- Department
- Reporting Manager

---

## Workflow Process

### 1. Request Initiation

- Collect employee details
- Ensure all required information is complete

---

### 2. Validation & Approval

- Confirm eligibility based on:
  - Employment status (e.g., regular employee)
  - Position requirements

- Seek approval from supervisor

### Decision:

- **Approved** → Proceed with request
- **Rejected** → Cancel request

---

### 3. Request Submission

- Submit request through internal ticketing system / web application
- Include all required employee details

---

### 4. External Processing (if applicable)

- Request is handled by external IT team (other country)
- Processing time may take several days or weeks

### Optional:

- Notify or follow up with external SysAdmin to help expedite processing

---

### 5. Status Tracking

Track request status using system-defined values:

- **Open** - Request is created and logged
- **Submit for Approval** - Request is awaiting approval
- **In Progress** - Request is being processed
- **Resolved** - Email account has been created
- **Closed** - Request is completed and finalized
- **Withdrawn** - Request was cancelled

#### Typical Flow

Open → Submit for Approval → In Progress → Resolved → Closed

#### Alternative Flow

Open → Submit for Approval → Withdrawn

---

### 6. Monitoring & Follow-up

- Monitor request status **daily** in the ticketing system
- Review all active requests and their current status

#### Actions Based on Status

- **Open / Submit for Approval**
  - Follow up with approver if delayed

- **In Progress**
  - Monitor processing by external team
  - Send follow-up or notification if delayed

- **Resolved**
  - Verify that the email account has been created
  - Proceed to recording and user notification

- **Closed**
  - No action required

- **Withdrawn**
  - Confirm cancellation and update records if necessary

---

#### Purpose

- Ensure no requests are left unattended
- Identify delays early
- Maintain service efficiency and accountability

---

### 7. Completion & Recording

- Once account is created:
  - Record email details in internal system
  - Update tracking records

---

### 8. Delivery to User

- Provide employee with:
  - Email account details
  - Login link or access instructions

---

## Expected Output

- Email account successfully created
- Request properly recorded
- Employee receives access details

---

## Security Considerations

- Verify employee identity before releasing account details
- Do not share credentials publicly
- Ensure only approved employees receive email access

---

## Dependencies

- Internal ticketing system
- External IT / SysAdmin team
- Supervisor approval

---

## Common Issues

- Incomplete employee information
- Delayed approval
- Long processing time from external team

---

## Troubleshooting

- Re-check submitted request details
- Follow up with approver
- Contact external SysAdmin team for status updates

---

## Related Documents

- SOP → Endpoint Provisioning
- Reference → Access Control Privacy

---

## Notes

This workflow depends on an external IT team and may experience delays beyond local control.

---

## Version History

| Version | Date | Changes |
|--------|------|--------|
| 1.1 | [Date] | Added status tracking and monitoring process |
| 1.0 | [Date] | Initial version |

