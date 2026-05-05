# SOP - Endpoint Hardware Validation (Archived Devices)

> Replace placeholder values if applicable before use.

---

## Overview

This SOP defines the process for validating archived endpoint devices and peripherals (desktops, monitors, keyboards, and mouse) to determine their operational status before reuse, repair, or disposal.

---

## Purpose

To ensure that all archived devices are properly tested, accurately classified, and safely prepared for redeployment, repair, or disposal.

---

## Scope

Applies to all archived endpoint devices and peripherals, including:

- desktop units
- monitors
- keyboards
- mouse
- related accessories

---

## Roles & Responsibility

- **IT/Admin:** Performs hardware validation, classification, and asset updates
- **User (if applicable):** Receives validated and working devices

---

## Inputs / Preconditions

- Archived devices available for testing
- Power source and required cables (power, HDMI/VGA, etc.)
- Test workstation (if needed)
- Access to asset recording system

---

## Workflow / Procedure

### 1. Device Preparation

1. Retrieve device from storage/archive
2. Prepare required cables and accessories
3. Place device in testing area
4. Ensure device is free from previous user data (if applicable)

---

### 2. Physical Inspection

Check for:

- Visible damage (cracks, dents, broken parts)
- Loose or damaged ports
- Missing components (RAM, HDD, cables)

---

### 3. Power Test

- Connect device to power
- Verify device powers on properly

---

### 4. Functional Testing

#### Desktop Unit

- Boot device to operating system
- Check for:
  - Normal boot process
  - No critical errors
  - Acceptable performance

---

#### Monitor

- Connect to a working desktop/laptop
- Verify:
  - Display output is visible
  - No flickering
  - No dead pixels or display issues

---

#### Keyboard

- Test all keys
- Verify:
  - Keys are responsive
  - No stuck or non-working keys

---

#### Mouse

- Test movement and clicks
- Verify:
  - Cursor movement is smooth
  - Left/right click working
  - Scroll wheel functional

---

### 5. Asset Condition Classification

Assign a condition based on evaluation:

| Condition | Description | Value Code |
|----------|------------|-----------|
| **New** | Unused, no defects, excellent condition | NEW |
| **Good** | Fully functional, minor cosmetic wear | GOOD |
| **Fair** | Functional with noticeable wear, minor issues | FAIR |
| **Poor** | Functional but degraded performance | POOR |
| **Damaged** | Not fully usable, requires repair | DAMAGED |
| **For Repair** | Under repair or awaiting repair | REPAIR |
| **Obsolete** | Outdated, not suitable for current use | OBSOLETE |
| **For Disposal** | Approved for disposal, not cost-effective to repair | DISPOSAL |
| **Disposed** | Already removed from inventory | DISPOSED |

---

### 6. Decision Handling

Based on classification:

- **Working Conditions (NEW / GOOD / FAIR):**
  - Return device to archive
  - Set availability status to **Available**

- **Needs Attention (POOR / DAMAGED / REPAIR / OBSOLETE):**
  - Evaluate for repair or replacement
  - Tag accordingly

- **Defective / Non-usable (DAMAGED / DISPOSAL):**
  - Set condition to **For Disposal (DISPOSAL)**
  - Prepare for disposal process

---

### 7. Asset Status Update

- Update condition and availability in asset management system
- Record test results

---

### 8. Tagging & Handling

- **Available:** Store in archive for future deployment
- **For Repair:** Isolate and schedule repair
- **For Disposal:** Segregate for disposal processing

---

### 9. Archive Storage Organization

Archived devices are stored in **separate labeled boxes per computer set**.

Each box should contain:

- Desktop unit
- Monitor
- Keyboard
- Mouse
- Associated cables (power, video, peripherals)

---

#### Peripheral & Cable Storage

Loose accessories and shared components are stored in **dedicated categorized boxes**, separate from device sets.

Examples:

- HDMI / VGA cables
- LAN cables
- Mouse / Keyboard (spares)
- Power cables
- Adapters and converters

---

#### Labeling Requirements (Peripheral Boxes)

Each box must be clearly labeled with:

- Item Type (e.g., HDMI Cable, LAN Cable, Mouse)
- Quantity (optional)
- Condition (if applicable)

---

#### Storage Rules

- Do not mix different cable types in one box
- Keep peripherals organized by category
- Ensure easy access and retrieval
- Maintain separation from complete device sets

---

#### Purpose 

- Prevent mixing of components and loss of accessories
- Avoid mixing incompatible components
- Maintain complete device sets
- Improve retrieval efficiency
- Ensure accurate asset tracking
- Speed up device assembly and troubleshooting

---

## Expected Output

- Devices are tested and validated
- Accurate condition classification applied
- Asset system updated
- Devices are properly tagged and stored

---

## Security Considerations

- Ensure no residual data is accessible on devices
- Wipe storage before redeployment if applicable
- Prevent unauthorized access to archived devices

---

## Dependencies

- Power supply and cables
- Test workstation
- Asset management system
- Basic diagnostic tools

---

## Common Issues

- No power → faulty PSU or cable
- No display → cable/port/monitor issue
- Slow performance → aging hardware
- Peripheral partial failure

---

## Troubleshooting

- Swap cables or ports
- Test with known working components
- Reboot or reconnect devices
- Escalate hardware issues if necessary

---

## Related Documents

- SOP → Endpoint Provisioning
- SOP → Device Decommissioning
- Tool → Basic Hardware Diagnostics

---

## Notes

This process ensures only reliable devices are returned to service and maintains accurate asset inventory.

---

## Version History

| Version | Date | Changes |
|--------|------|--------|
| 1.1 | [Date] | Added asset condition classification and decision handling |
| 1.0 | [Date] | Initial version |