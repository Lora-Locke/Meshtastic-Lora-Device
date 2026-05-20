# Flashing Meshtastic Firmware 📡

The XIAO ESP32S3 + Wio SX1262 kit comes pre-flashed with Meshtastic 
firmware straight out of the box, so in most cases you won't need to 
do anything here at all. However if you need to update to a newer version 
of Meshtastic, or if something has gone wrong and you need to reflash, 
this guide will walk you through it.

The whole process takes about 2 minutes and requires no technical knowledge 
beyond being able to plug in a USB cable. Which hopefully you can manage. 🔌

---

## What You Need

- Your LoRa device
- A USB-C cable
- A computer running Google Chrome or Microsoft Edge
  (Firefox won't work here — the web flasher uses Web Serial API 
  which Firefox doesn't support yet, sorry Firefox fans)
- An internet connection

---

## Step by Step

### 1. Connect your device
Plug your device into your computer using a USB-C cable. 
You don't need to power it on first, just plug it in.

### 2. Open the Meshtastic Web Flasher
Go to 👉 [flasher.meshtastic.org](https://flasher.meshtastic.org)

This is the official Meshtastic web flasher tool. 
It runs entirely in your browser and no software installation is required.

### 3. Select your device
From the device dropdown menu select:

**Seeed Studio XIAO S3**

If you don't see this option, make sure you're using Chrome or Edge 
and that your USB-C cable supports data transfer 
(some cheap cables are charge only — classic).

### 4. Select the firmware version
The flasher will show you the latest stable release of Meshtastic. 
Unless you have a specific reason to use an older version, 
always go with the latest stable release.

### 5. Flash the device
Click the **Flash** button.

The flasher will ask you to select a serial port — 
a popup will appear showing available ports. 
Select the one that corresponds to your device 
(it will usually show up as something like COM3 on Windows 
or /dev/ttyUSB0 on Linux/Mac).

The flashing process takes around 30 seconds. 
You'll see a progress bar. Don't unplug the device during this time 
or you'll have a bad time.

### 6. Done!
Once complete the device will automatically reboot with the new firmware. 
You're ready to go.

---

## Setting Up the Meshtastic App

Once your device is flashed and powered on:

1. Download the **Meshtastic app** on your phone
   - iOS: [App Store](https://apps.apple.com/app/meshtastic/id1586432531)
   - Android: [Google Play](https://play.google.com/store/apps/details?id=com.geeksville.mesh)

2. Open the app and tap **+** to add a new device

3. Select your device from the Bluetooth list

4. Enter the default PIN: **123456**

5. You're on the mesh! 🎉

From the app you can configure your device name, set your region 
(make sure to set this to **EU_868** for UK use to ensure you're 
operating on the correct frequency band), 
join or create channels, and send messages to other nodes.

---

## Troubleshooting

**My device isn't showing up in the flasher**
- Try a different USB-C cable — data only cables are a common culprit
- Make sure you're using Chrome or Edge
- Try a different USB port on your computer

**The flash failed halfway through**
- Don't panic. Just try again from Step 3.
- If it keeps failing, try holding the BOOT button on the XIAO module 
  while plugging in the USB cable to force it into bootloader mode

**My device isn't connecting to the app after flashing**
- Make sure you've set your region in the app on first setup
- Try restarting both the device and your phone's Bluetooth

---

## Further Help

The Meshtastic community is large, active, and very helpful.
If you're stuck, the best places to get help are:

- 📖 [Meshtastic Documentation](https://meshtastic.org/docs/)
- 💬 [Meshtastic Discord](https://discord.gg/ktMAKGBnBs)
- 🐙 [Meshtastic GitHub](https://github.com/meshtastic/Meshtastic-device)
