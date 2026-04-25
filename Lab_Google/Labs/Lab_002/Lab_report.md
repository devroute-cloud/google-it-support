# LAB-002

## General Information
- **Lab ID:** Google Cloud Skills Boost ID
- **Title:** Software packages and file storage in Linux
- **Completion Date:** 2026-05-24
- **Status:** ✅ Completed
  

## 📉Description

### In this Laboratory, you will learn to install and uninstall Linux software.
- How to work with compressed files.
- You'll install a text editor called SUBLIME TEXT.
- You'll extract them and then compress them again into .tar. files.
- You'll use APT for installing and uninstalling Linux Programs.
  

## ✅Objectives

### Interact with.
- Sublime Text.
- Extract a file
- Store files
- Install 7-Zip
- Uninstall GIMP


## 💻Technologies Used
- Google Cloud Service
- Linux
- Bash

  

## 👨‍💻Steps Taken

### How to install Sublime Text.
1. First, use "dpkg" to install the Sublime Text text editor
Command: sudo dpkg -i /home/ejemplo/downloads/sublime-text_build-3211_amd64.deb
  *You'll see some errors after using this command, but that's normal.
   The Sublime Text package has dependencies that aren't installed on your computer yet.
   That's why "dpkg" warns you that you need to install them.*

2. To fix this error, use apt to correct the missing dependencies. Do this with the following command
Command: sudo apt install -f
   *To do this, type "Y" (for "yes").*

3. Sublime Text is now successfully installed. You can verify this using the next command.
Command: dpkg -s sublime-text


### How to extract a file.
1.  You will extract a .tar file. The "extract_me.tar" file is located in "/home/example/downloads/". Use the following command.
Command: cd /home/example/downloads

2. Next, you can use the following Linux "tar" command to extract it.
Command: sudo tar -xvf extract_me.tar

3. sudo tar -xvf extract_me.tar 
   1. home/example/extract_me/ ✅
   2. home/example/extract_me/great_job ✅
   

### How to store files
1. First, you will return to the original directory.
Command: cd ~
   Points. (You can also use the "tar" command to reverse the operation and create an archive.)
   Exercise 1. You'll create three files named "Thursday", "Wednesday", and "Monday" on your PC   
            2. in the "/home/example/documents" folder
            3. Use the following "tar" command *one line* to store them in the "Days.tar" archive.
Command: tar -cvf Days.tar --absolute-names /home/example/documents/Thursday /home/example/documents/Wednesday /home/example/documents/Monday

2. Then, "Days.tar" will be added to your current directory, which will contain the three days' files:
   1. /home/example/documents/Thursday
   2. /home/example/documents/Wednesday
   3. /home/example/documents/Monday

### How to install 7-Zip
1. You can use apt to install 7-Zip this it.
Command: sudo apt install p7zip-full
   *To confirm, type "Y" (for "yes"). 7-Zip will then be installed.*

2. You can verify the installation using the following command:
Command: dpkg -s p7zip-full

### How to uninstall GIMP
1. To uninstall it, use apt with the following command:
Command: sudo apt remove gimp
   *To confirm, type "Y" (for "yes"). GIMP will then be uninstalled.*

2. To verify this, use (just like before)the following command:
Command: dpkg -s gimp

## Conclusion
That's amazing. You successfully installed and uninstalled programs on Linux.
