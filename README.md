# Ex.No.7 Use AFLogical OSE to Extract Data from an Android Device

## Description

AF Logical OSE (Open Source Edition) is a tool used to extract data from Android devices. It’s part of the Open Source Android Forensics project and is often used for logical extraction, which means pulling data like contacts, messages, and call logs without directly accessing the file system. Here’s a step-by-step guide to using AF Logical OSE to extract data from an Android device.

---

## Step 1: Prepare Your Environment

### 1. Download AF Logical OSE

- Visit the AFLogical OSE GitHub page and download the latest release.
- Alternatively, you can clone the repository using Git.
<img width="602" height="292" alt="image" src="https://github.com/user-attachments/assets/f16c2155-56ae-4933-a3b5-5c7f2e425cf3" />

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

---
<img width="602" height="204" alt="image" src="https://github.com/user-attachments/assets/e0f732db-0a08-4d49-8e03-c9ea8641a36d" />


## Step 2: Connect the Android Device to Your Computer

### 1. Connect via USB

- Use a USB cable to connect the Android device to your computer.

### 2. Verify ADB Connection

- Open Command Prompt on Windows or Terminal on macOS/Linux and run:

```bash
adb devices
```
<img width="602" height="164" alt="image" src="https://github.com/user-attachments/assets/f9131a22-d85a-406c-9c8d-7c261f5dc939" />

- This command lists connected devices.
- If your device is listed, you are ready to proceed.
- If not, ensure that USB Debugging is enabled and that the correct drivers are installed.

---

## Step 3: Extract Data Using AF Logical OSE

### 1. Run AF Logical OSE

- Navigate to the directory where you have downloaded or extracted AFLogical OSE.

### 2. Push the APK to the Android Device

- Run the following command to install the AFLogical OSE APK on the device:

```bash
adb install af logical.apk
```

- This installs the AF Logical app on the device, which will be used to collect data.

### 3. Launch the AF Logical OSE App on the Device

- On the Android device, open the AF Logical app.
- You’ll see options to extract various types of data (e.g., contacts, SMS, MMS, call logs).
- Select the data types you want to extract.

### 4. Start Data Extraction

- Once you’ve selected the data types, the app will start the extraction process.
- Data is stored in `.csv` files on the device’s storage, typically in a directory named `af logical`.

---

## Step 4: Transfer Extracted Data to Your Computer

### 1. Use ADB to Pull Data

- After extraction, you need to transfer the data files from the Android device to your computer.
- Run:

```bash
adb pull /sd card/af logical /path/to/destination
```

- Replace `/path/to/destination` with the directory path where you want to save the extracted data on your computer.

### 2. Verify the Data

- Navigate to the destination directory and check the `.csv` files to ensure all required data has been extracted.

---
<img width="602" height="239" alt="image" src="https://github.com/user-attachments/assets/e7bfc852-16cd-4ac1-91d6-f5e66abc77d7" />


## Step 5: Analyze the Extracted Data

### 1. Open the CSV Files

- Use Excel, Google Sheets, or any text editor to open and analyze the `.csv` files.
- These files contain the extracted data like contacts, SMS, MMS, and call logs.

### 2. Review and Document

- Carefully review the data for any relevant information.
- Document your findings and consider exporting the data into a report format for further analysis.

---

## Step 6: Clean Up

### 1. Uninstall AF Logical OSE

- Once data extraction is complete, you can uninstall the AFLogical OSE app from the Android device by running:

```bash
adb uninstall com.viaforensics.android.aflogical
```

### 2. Disconnect the Device

- Safely disconnect the Android device from your computer.

---

## Conclusion

By following these steps, you can use AF Logical OSE to effectively extract and analyze data from an Android device. This process is valuable for forensic investigations, especially when dealing with logical data that doesn’t require root access to the device.

---

# Result

The Android device was successfully connected and data was extracted using AFLogical OSE. Contacts, messages and call logs were collected in CSV format and transferred to the computer for forensic examination.
