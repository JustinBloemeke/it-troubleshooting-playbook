# Troubleshooting Password Reset and Account Access Issues

## Symptoms
- Unable to log in to computer or account
- Incorrect password error
- Account locked after multiple attempts
- User cannot access email or applications

## Possible Causes
- Forgotten password
- Incorrect keyboard input (Caps Lock, Num Lock)
- Account lockout due to failed login attempts
- Expired password
- Domain or account synchronization issues

## Steps to Resolve

### 1. Verify Basic Input
- Ensure Caps Lock is off
- Check Num Lock (for laptops/external keyboards)
- Confirm correct username is being used

### 2. Attempt Password Reset
- Use "Forgot Password" option (if available)
- Follow prompts to reset password using email or security questions

### 3. Unlock Account (If Locked)
- Wait 10–15 minutes for automatic unlock (if policy allows)
- If using Active Directory:
  - Open **Active Directory Users and Computers**
  - Locate user account
  - Right-click → **Properties**
  - Unlock account

### 4. Reset Password Manually (IT/Admin)
- Open user management system (Active Directory or local accounts)
- Reset password
- Require user to change password on next login

### 5. Check Network Connection
- Ensure device is connected to network (especially for domain accounts)
- Try logging in while connected to company network or VPN

### 6. Verify Account Status
- Confirm account is not disabled or expired
- Check group membership and permissions if access issues persist

### 7. Test Login
- Have user log in with new credentials
- Confirm access to required systems (email, applications, etc.)

## Additional Notes
- Encourage strong password practices
- Recommend password managers for users
- Document all resets for security and auditing purposes

## Common Mistakes
- Forgetting to check Caps Lock or keyboard input
- Not verifying if account is locked vs incorrect password
- Resetting password without confirming user identity
