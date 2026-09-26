# Ex.No.7 Use AFLogical OSE to Extract Data from an Android Device

## Description

AF Logical OSE (Open Source Edition) is a tool used to extract data from Android devices. It’s part of the Open Source Android Forensics project and is often used for logical extraction, which means pulling data like contacts, messages, and call logs without directly accessing the file system. Here’s a step-by-step guide to using AF Logical OSE to extract data from an Android device.

---

## Step 1: Prepare Your Environment

### 1. Download AF Logical OSE

- Visit the AFLogical OSE GitHub page and download the latest release.
- Alternatively, you can clone the repository using Git.
<img width="602" height="292" alt="image" src="https://github.com/user-attachments/assets/cc247123-68d8-461e-a0f7-f81d490ccc97" />

### 2. Install Java (if not already installed)

- AF Logical OSE requires Java to run.
- Make sure you have Java installed on your machine.
- You can download it from the official Java website.

### 3. Install Android Debug Bridge (ADB)

- ADB is a command-line tool that allows communication with Android devices.
- Download it from the Android Developer's website and install it on your system.
- Add ADB to your system's PATH environment variable to easily run ADB commands from the terminal or command prompt.

### 4. Enable USB Debugging on the Android Device

- On the Android device, go to:

  **Settings > About Phone**

- Tap **Build Number** seven times to enable Developer Options.
- Go to:

  **Settings > Developer Options**

- Enable **USB Debugging**.
<img width="602" height="204" alt="image" src="https://github.com/user-attachments/assets/e560c42b-7dfc-4796-ba7e-3bd094b6c63c" />

---

## Step 2: Connect the Android Device to Your Computer

### 1. Connect via USB

- Use a USB cable to connect the Android device to your computer.

### 2. Verify ADB Connection

- Open Command Prompt on Windows or Terminal on macOS/Linux and run:
<img width="602" height="164" alt="image" src="https://github.com/user-attachments/assets/61f3b890-dbdf-4b06-b251-2e7650841df3" />

```bash
adb devices
## Step 3: Extract Data Using AF Logical OSE

### 1. Run AF Logical OSE

- Navigate to the directory where you have downloaded or extracted AFLogical OSE.

### 2. Push the APK to the Android Device

- Run the following command to install the AFLogical OSE APK on the device:
<img width="602" height="239" alt="image" src="https://github.com/user-attachments/assets/ed41f499-1405-4589-9208-94f10fde6642" />

```bash
adb install af logical.apk
