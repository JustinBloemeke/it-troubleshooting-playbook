# New Employee Workstation Setup (IT Onboarding Guide)

## Objective

Provide a step-by-step process for preparing and deploying a workstation for a new employee, ensuring required systems, access, software, and configurations are ready for first-day productivity.

## Equipment Needed

- Laptop or desktop
- Power adapter
- Monitor(s), keyboard, and mouse
- Network cable or WiFi access
- Docking station, if applicable

## Steps to Complete Setup

### 1. Prepare the Device

- Unbox and inspect hardware for damage
- Connect power and required peripherals
- Power on the device and confirm it starts normally

### 2. Reusing an Existing Device, If Applicable

- Confirm the laptop or desktop powers on without immediate hardware issues
- Use a bootable USB drive if the operating system needs to be reinstalled
- Restart the computer and enter BIOS/UEFI using the appropriate key, commonly **F2, Del, F12, F10, or Esc**
- Configure the system to boot from the USB drive

**Tip:** If the organization uses Microsoft Intune or Windows Autopilot, capture the device hash before reimaging when required:

- Run `Get-WindowsAutopilotInfo` in PowerShell as Administrator
- Export the output to a CSV file for device registration

### 3. Install or Image the Operating System

- Deploy the standard company image, if applicable
- If reusing an existing device, delete old disk partitions during installation when appropriate and approved
- Ensure the latest supported operating system version is installed
- Apply required system updates

**Tip:** If using Windows Autopilot, press the Windows key five times at the setup screen to access provisioning options, if enabled by the organization.

### 4. Join Device to Domain or Management System

- Join the device to Active Directory, Azure AD, or Entra ID as required
- Enroll the device in the organization’s management platform, such as Microsoft Intune
- Confirm the device appears correctly in the management portal

### 5. Create or Configure User Account

- Verify the user account has been created
- Assign appropriate groups and permissions if needed
- Set or confirm temporary password procedures according to company policy

### 6. Install Required Software

- Microsoft Office or productivity tools
- Company-specific applications
- Security software, antivirus, or endpoint protection
- VPN client, if required

**Tip:** Depending on the organization, software may install automatically during device setup. Always verify required applications are installed before user handoff.

### 7. Configure Email and Access

- Set up Outlook or the required email client
- Verify login access to internal systems
- Confirm access to shared drives, cloud storage, or department resources

### 8. Connect to Network

- Configure WiFi or Ethernet connection
- Test internet connectivity
- Verify access to online company resources

### 9. Test Hardware and Functionality

- Check keyboard, mouse, monitors, and docking station
- Test webcam and microphone
- Confirm printers are accessible if required

### 10. Document Setup

- Record asset tag and assigned user
- Update asset management system or company database
- Document any issues, special configurations, or missing equipment

### 11. Final User Handoff

- Provide login instructions according to company policy
- Guide the user through first login
- Answer basic setup questions
- Confirm the user can access required systems

## Additional Notes

- Follow company security policies at all times
- Ensure all devices meet compliance standards
- Maintain clear documentation for future support
- Follow internal escalation procedures for access, security, or hardware issues

## Common Mistakes

- Forgetting to install required applications
- Not verifying user permissions
- Skipping system updates
- Failing to document asset assignment
- Not capturing the device hash before reset when required for Intune or Autopilot
