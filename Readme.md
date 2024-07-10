# Disabling SSID "www.excitel.com" in excitel router.

## Device Details
- **Device Gateway Type:** Titanium-2122A
- **Hardware Version:** C40-210
- **Software Version:** T2122-1.19EXU

## Setup Instructions

### 1. Reset the Router
Reset the router using the reset button.

### 2. Access Router Settings
- Open a web browser and go to your router's IP address. Typically, it's [http://192.168.1.1](http://192.168.1.1).

### 3. Login to Router
- Use the following credentials:
  - **Username:** excitel
  - **Password:** exc@123

### 4. Download Configuration File
- Download the configuration file `romfile.cfg` from [http://192.168.1.1/romfile.cfg](http://192.168.1.1/romfile.cfg) after logging in.

### 5. Modify `romfile.cfg`
- Open `romfile.cfg` in a text editor.
- Search for "www.excitel.com".
- Locate the line `<Entry1 SSID="www.excitel.com" ... EnableSSID="1" ...`.
- Change `EnableSSID="1"` to `EnableSSID="0"` and save the file.

### 6. Upload Modified Configuration
- Navigate to [http://192.168.1.1/cgi-bin/upgrade.asp](http://192.168.1.1/cgi-bin/upgrade.asp) in your browser.

### 7. Select File to Upload
- Choose "romfile" as the upgrade type.

### 8. Upload Modified `romfile.cfg`
- Select the modified `romfile.cfg` using the file upload option.

### 9. Confirm Upload
- Press "OK" to upload the file.

### 10. Reboot Router
- The router will automatically reboot.
- After rebooting, "www.excitel.com" will no longer appear as a hotspot.

---

This guide provides step-by-step instructions to configure your Titanium-2122A router.
