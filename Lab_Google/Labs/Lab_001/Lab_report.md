# LAB-001

## General Information
- **Lab ID:** Google Cloud Skills Boost ID
- **Title:** Software packages and file storage in Windows
- **Completion Date:** 2026-05-24
- **Status:** ✅ Completed
  

## 📉Description

### In this Laboratory, you learned to install and uninstall software for the GUI and CLI of Windows.
- You'll work with compressed files.
- You'll install a text editor called = SUBLIME TEXT.
- You'll extract them and then compress them again into .tar. files.
- You'll use Windows PowerShell for installing and uninstalling in Windows Programs.
  

## ✅Objectives

### Interact with.
- Install Sublime Text, using the GUI of Windows.
- Estract files with 7-Zip and PowerShell.
- Install VLC with PowerShell on Windows.
- Uninstall GIMP with PowerShell on Windows.


## 💻Technologies Used
- Google Cloud Service
- PowerShell
- 7-Zip
- VLC
- GIMP
  

## 👨‍💻Steps Taken

### Install Sublime Text.
° It is used to write, edit, and organize code in multiple programming languages.
1. Visit the Website: https://www.sublimetext.com.
2. Download the New Version to your Local Disc.
3. Execute.
4. Install.
5. Sublime will be ready.

### How to extract a file with 7-Zip.
° 7-Zip compresses and decompresses files in multiple formats.
1. Select the file. Then right-click
2. Select the option 7-Zip. Then extract here.
3. The different files will be ready on your PC.

### How to compress a file with PowerShell.
° Compressing a file is mainly done to reduce its size.
- This is a Little Example: We will search files: “Earth,” “Mercury,” and “Venus.”
- Then 👇.
1. Select PowerShell with Administrator.
2. Command: cd C:\Users\Folder\Documents\
3. We will create a file .Zip called "Planets.Zip" using this command: Compress-Archive -Path Earth, Mercury, Venus Planets.zip
4. The compress will be ready.

### Install and Uninstall software using the Windows CLI.
° It is primarily used to automate, accelerate, and centrally manage applications, overcoming the limitations of the traditional graphical interface 
- Then 👇.
1. Select PowerShell with Administrator.
2. Specify the base URL for the software you want to install (example: VLC media player):
  - $VLC_URL = "https://get.videolan.org/vlc/last/win64/"
3. Get the list of files available in the URL:
  - $GET_HTML = Invoke-WebRequest $VLC_URL
4. Filter the installer file that ends with “win64.exe”:
  - $FILE = $GET_HTML.Links | Where-Object { $_.href.EndsWith("win64.exe") } | Select-Object -ExpandProperty href
5. Build the full installer URL:
  - $URL = $VLC_URL + $FILE
6. Set the local download folder (example):
  - $DOWNLOAD_DIR = "C:\Users\qwiklabs\Downloads\" $OUTPUT_FILE = $DOWNLOAD_DIR + $FILE
7. Download the installer file:
  -(New-Object System.Net.WebClient).DownloadFile($URL, $OUTPUT_FILE)
8. Run the installer in silent mode:
  - cmd.exe /c $OUTPUT_FILE /S
9. Check that the software has been installed correctly:
  -Get-Package -Name *vlc*

### Uninstalling software using Windows PowerShell.
1. Select PowerShell with Administrator.
2. Run the command to uninstall the program (example: GIMP):
   - cmd.exe /c "C:\Program Files\GIMP 2\uninst\unins000.exe" /VERYSILENT /NORESTART
3. Verify that the program has been uninstalled:
   - Get-Package
  
     (The uninstalled program should not appear in the list.)


