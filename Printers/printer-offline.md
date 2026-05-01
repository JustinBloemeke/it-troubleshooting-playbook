# Troubleshooting a Printer Showing Offline

## Symptoms
- Printer appears as "Offline" in Windows
- Print jobs are stuck in the queue
- Unable to print documents

## Possible Causes
- Printer is powered off or disconnected
- Network connectivity issues
- Print spooler service stopped
- Incorrect printer settings
- Driver issues

## Steps to Resolve

### 1. Check Physical Connection
- Ensure the printer is powered on
- Verify USB cable is connected (if applicable)
- If wireless, confirm printer is connected to the correct WiFi network

### 2. Restart the Printer
- Turn off the printer
- Wait 10–15 seconds
- Turn it back on

### 3. Set Printer to Online
- Open **Control Panel**
- Go to **Devices and Printers**
- Right-click the printer
- Click **See what's printing**
- Click **Printer** (top menu)
- Uncheck **Use Printer Offline**

### 4. Clear the Print Queue
- Open the print queue
- Cancel all pending print jobs
- Restart the print job

### 5. Restart Print Spooler Service
- Press **Windows + R**
- Type `services.msc`
- Find **Print Spooler**
- Right-click → **Restart**

### 6. Check Network Connection (For Network Printers)
- Ensure your computer and printer are on the same network
- Ping the printer IP (optional):
  - Open Command Prompt
  - Type: `ping [printer IP]`

### 7. Reinstall the Printer
- Remove the printer from **Devices and Printers**
- Restart your computer
- Re-add the printer

## Additional Notes
- Ensure correct printer drivers are installed
- For persistent issues, update or reinstall drivers from manufacturer website
