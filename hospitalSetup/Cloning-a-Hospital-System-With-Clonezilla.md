## Cloning a Hospital System With Clonezilla

1. Create an account for the system in Active Directory
  * Location: ```col.missouri.edu/MU/ENGR/CIRL/Systems/Hospital/Kinect```
  * Name: **CERT-HOSP-001**  
      *This name must match the name of the source system when it was joined to the Active Directory. We will change it after the restore process is complete. You will need to recreate this account in Active Directory before cloning the next system.*
2. Place a label on the system noting the System Id in the format CERT-HOSP-nnn, where nnn is the incremental number of this system
3. Connect the system:  
   1. Power adapter
   2. Network cable
   3. Kinect USB
   4. Keyboard and mouse USB
   5. DVD Video Cable
   6. Clonezilla thumb drive
   7. USB drive containing the system image
4. Turn on the system
5. Press `F12` to enter boot menu
6. Select SanDisk Cruzer Facet 1.26 (or whatever is the name of the boot device on which Clonezilla is installed) and press Enter
7. Press `Enter` to accept Clonezilla live (Default settings, VGA 800x600)
8. Press `Enter` to accept English
9. Press `Enter` to accept default keymap
10. Press `Enter` to start Clonezilla
11. Press `Enter` to work with system images
12. Press `Enter` to use local_dev
13. Press `Enter` so the OS can detect the USB device
14. Use the arrow keys to select the USB drive containing the System Image `sdc1 2.7T_ntfs_HarrisBHExt` then press `Enter`
15. Use the arrow keys to select the partimag directory then press `Enter`
16. View the disk space usage then press `Enter`
17. Press `Enter` to accept Beginner Mode
18. Use the arrow keys to select restoredisk – Restore an image to a local disk then press `Enter`
19. Use the arrow keys to select `Hospital-Image-2013-12-16-001-img` (previously `Hospital-Image-2013-12-12-001-img`) then press `Enter`
20. Press `Enter` to overwrite the only internal drive in the computer
21. Note the command being run then press Enter
22. Type `y` then press `Enter` to confirm overwriting the drive
23. Type `y` then press `Enter` again to re-confirm overwriting the drive
24. *The overwriting process should take about 7 – 10 minutes*
25. When everything is done, press `Enter` to continue
26. Use the arrow keys to select `Reboot` then press `Enter`
27. After the USB drives are unmounted disconnect them from the system
28. Wait for Windows 8.1 to start up. This could take a while the first time while it gets the devices set up.
29. Log in to Windows using the `MU ENGR CERT HOSP Kinect` account
1. Change the System Id for the Fall Alerts email:
   1. In Windows File Explorer navigate to `C:\ProgramData\Microsoft\Windows\Start Menu\Programs\Startup`
   1. Right-click on the Kinect shortcut and choose `Properties` from the shortcut menu
   1. In the Target field of the Kinect Properties change the flag `–SALERTS 10001` to `–SALERTS 10nnn`, where nnn is the incremental number of this system
   1. Click the `OK` button to close the Kinect Properties dialog box
   1. Click the `Continue` button in the Access Denied dialog box to approve using 
1. Change the network folder for data backup:
   1. Right-click on the Notepad++ icon on the taskbar, then right-click on Notepad++ in the jump list and choose `Run as administrator` from the shortcut menu
   1. Click the Yes button in the User Account Control dialog box
   1. Click File | Open from the menus
   1. In the Open dialog box select `C:\ProgramData\Microsoft\Windows\StartMenu\Programs\Startup\MapElektro.bat` and click the `Open` button to open that file
   1. At the end of the first line change the folder name from `10001` to `10nnn` where nnn is the incremental number of this system
   1. Save the file
   1. Close Notepad++
1. Change the computer's name:  [[include:Changing the Name of a Windows PC]]
1. Close all windows
1. On the Desktop press `Alt-F4` to open Shut Down Windows dialog box
1. Select `Update and Shut Down` (or just `Shut Down` if no updates are available) then click the `OK` button to shut down the system

 