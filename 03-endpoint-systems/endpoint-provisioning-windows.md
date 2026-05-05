# SOP - Endpoint Provisioning (Windows & Firmware Security)

> Replace placeholder values (e.g., USERNAME, PASSWORD) before use.

---

## Overview

This SOP defines the process for provisioning a new laptop or desktop device, including OS setup, user configuration, security hardening, and asset tagging.

---

## Purpose

To ensure all endpoint devices are securely configured, standardized, and properly assigned before deployment to employees.

---

## Scope

Applies to standalone Windows-based laptops and desktops.

---

## Roles & Responsibility

- **IT/Admin:** Performs provisioning, configuration, and security setup
- **User:** Receives device and signs accountability

---

Inputs / Preconditions

- New or reformatted device
- Administrative access (CMD via OOBE)
- BIOS access
- Required applications/installers
- Asset recording system

---

Workflow / Procedure

### 1. Initial Setup (OOBE)

1. Power on the device
2. Proceed with Windows setup until the internet connection screen

---

### 2. Open Command Prompt

Press:

`Shift + F10`

---

### 3. Bypass Microsoft Account Requirement

#### Laptop:

```cmd
oobe\bypassnro
```

#### Desktop:

```cmd
start ms-cxh:localonly
```

> Note:

- `start ms-cxh:localonly` is faster but may not work on all systems
- `oobe\bypassnro` is more consistent

---

### 4. Create Local User

- Create default user:

`Username:User`

- Complete setup and login

---

### 5. Network & Application Setup

- Connect device to the internet
- Install required applications based on employee role

---

### 6. Configure Administrative Access

#### Enable Built-in Administrator:

```cmd
net user Administrator /active:yes
```

#### Set Administrative Password

```cmd
net user Administrator [PASSWORD]
```

> Password must be known only to IT team

---

### 7. Configure User Permissions:

#### Add user to standard users:

```cmd
net localgroup Users USERNAME /add
```

#### Remove user from administrators:

```cmd
net localgroup Administrators USERNAME /delete
```

> Enforces least privilege principle

---

### 8. Configure BIOS Security

1. Enter BIOS during startup
2. Navigate to Security settings

Set the following:

- **Supervisor Password**
- **System Management Password**

> Restricted to IT personnel only

---

### 9. Enable Firmware Access Controls

Enables the following BIOS settings:

- System Management Password Access Control
- BIOS Setup Configuration Protection

> These settings typically:
  
  - "Require authentication before modifying BIOS settings"
  - "Restrict unauthorized configuration changes"
  - "Protect critical system settings (boot, firmware, security)"

> Note: BIOS setting names and behavior may vary depending on device manufacturer.
---

## Expected Output

- Device is fully configured
- User has standard (non-admin) access
- Administrative access is controlled
- BIOS is secured
- Device is ready for deployment

---

## Asset Management & Accountability

Record the following:

- Manufacturer
- Model
- Serial Number
- Employee Name
- Employee ID
- Department
- Position

### Asset Tagging

- Assign device to employee
- Register in asset management system

### Accountability

- Employee signs accountability form

---

## Security Considerations

- Built-in Administrator uses shared credentials
- BIOS password mismanagement may cause lockout
- Local accounts lack centralized identity control

---

## Dependencies

- Internet connection
- Admin command access
- BIOS access
- Application installers

---

## Common Issues

- OOBE bypass not working
- Missing drivers after setup
- User still has admin privileges
- BIOS password misconfiguration

---

## Troubleshooting

- Try alternate OOBE method if one fails
- Reapply user group commands if permissions incorrect
- Verify BIOS access and credentials
- Reinstall missing drivers or applications

---

## Related Documents

- SOP → Device Decommissioning
- Incident → User Permission Issues
- Tool → Windows CMD Commands

---

## Notes

This process applies to standalone environment and may differ in domain-managed or enterprise setups.

## Version History

| Version | Date | Changes |
|--------|------|--------|
| 1.0 | [Date] | Initial version |