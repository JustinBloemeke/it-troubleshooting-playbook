# New Employee Workstation Setup (IT Onboarding Guide)

## Objective
Provide a step-by-step process for preparing and deploying a workstation for a new employee, ensuring all required systems, access, and configurations are ready for first-day productivity.

## Equipment Needed
- Laptop or desktop
- Power adapter
- Monitor(s), keyboard, mouse
- Network cable or WiFi access
- Docking station (if applicable)

## Steps to Complete Setup

### 1. Prepare the Device
- Unbox and inspect hardware for damage
- Connect power and peripherals
- Power on device

### 2. If Reusing an Existing Laptop or Desktop
- Ensure the device powers on without issues
- If system is a Windows or Linux laptop or desktop, use a bootable USB drive containing the desired OS
- Restart the computer into the BIOS by rapidly hitting the BIOS key (usually **F2, Del, F12, F10, or Esc**)
- In the BIOS menu, configure the system to perform a one time boot from the USB drive
- **Tip:** If your organization uses Microsoft Intune or Autopilot, capture the device hash before reimaging:
  - Run `Get-WindowsAutopilotInfo` in PowerShell (as Administrator)
  - Export the output to a CSV file for device registration

### 3. Install or Image Operating System
- Deploy standard company image (if applicable)
- If using Windows Autopilot, press the Windows key five times at the setup screen to access provisioning options (if enabled)
- If reusing an existing laptop or desktop, make sure to delete all disk partitions when prompted
- Ensure latest OS version is installed
- Apply all system updates

### 4. Join Device to Domain / Management System
- Join device to Active Directory or Azure AD
- Enroll device in management platform (e.g., Intune)

### 5. Create or Configure User Account
- Verify user account is created
- Assign appropriate permissions and groups if needed
- Set temporary password if needed

### 6. Install Required Software
- Microsoft Office / productivity tools
- Company-specific applications
- Security software (antivirus, endpoint protection)
- VPN client (if required)
- **Tip:** Depending on your organization, this may be done automatically during device setup.
  - Double check all needed software is installed once setup is complete

### 7. Configure Email and Access
- Set up Outlook or email client
- Verify login access to internal systems
- Confirm access to shared drives or cloud storage

### 8. Connect to Network
- Configure WiFi or Ethernet connection
- Test internet connectivity
- Verify access to online company resources

### 9. Test Hardware and Functionality
- Check keyboard, mouse, monitors
- Test webcam and microphone
- Ensure printers are accessible if needed

### 10. Document Setup
- Record asset tag and assigned user
- Update asset management system and/or company database
- Document any issues or special configurations

### 11. Final User Handoff
- Provide login credentials
- Guide user through first login
- Answer basic questions
- Ensure user can access all required systems

## Additional Notes
- Follow company security policies at all times
- Ensure all devices meet compliance standards
- Maintain clear documentation for future support

## Common Mistakes
- Forgetting to install required applications
- Not verifying user permissions
- Skipping system updates
- Failing to document asset assignment
- Not grabbing device hash before system reset if using Intune or other related programs
