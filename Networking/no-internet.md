# Troubleshooting No Internet Connection

## Symptoms
- Unable to access websites
- "No Internet" or "Limited Connectivity" message
- WiFi connected but no internet access
- Network icon shows disconnected

## Possible Causes
- Network outage
- Incorrect IP configuration
- Faulty network adapter
- DNS issues
- Router/modem problems
- Disabled network adapter

## Steps to Resolve

### 1. Check Physical Connections
- Ensure Ethernet cable is securely connected (if wired)
- Confirm WiFi is turned on (if wireless)
- Check router/modem lights for connectivity status

### 2. Restart Devices
- Restart your computer
- Power cycle modem and router:
  - Unplug both devices
  - Wait 30 seconds
  - Plug back in and allow them to fully restart

### 3. Check Network Status
- Click network icon in taskbar
- Confirm you are connected to the correct network

### 4. Run Windows Network Troubleshooter
- Go to **Settings → Network & Internet**
- Click **Network Troubleshooter**
- Follow prompts

### 5. Check IP Configuration
- Open Command Prompt
- Run: **ipconfig**
- Verify:
- IP address is not 169.254.x.x (indicates no DHCP)

### 6. Renew IP Address
- In Command Prompt: **ipconfig /release**
- Then in Command Prompt: **ipconfig /renew**

### 7. Test Connectivity
- Ping a known IP: **ping 8.8.8.8** for example
- If successful, internet connection exists but DNS may be the issue

### 8. Flush DNS Cache
- Run: **ipconfig /flushdns**

### 9. Check Network Adapter
- Open **Device Manager**
- Expand **Network Adapters**
- Ensure adapter is enabled
- Update or reinstall drivers if needed

### 10. Try Another Network
- Connect to a different WiFi network (e.g., hotspot)
- Helps determine if issue is local or network-related

## Additional Notes
- If multiple devices cannot connect, issue is likely router or ISP-related
- If only one device is affected, focus on device-specific troubleshooting

## Common Mistakes
- Forgetting to restart networking equipment
- Not checking if other devices are affected
- Ignoring IP address errors (169.254.x.x)
