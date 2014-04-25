### Cloning a CERT Sensor Monitor with Clonezilla

1. Connect the system:
   * Network Cable
   * Keyboard and Mouse USB
   * VGA Video cable
   * Power Adapter
   * Clonezilla Thumb Drive or Clonezilla USB CD drive
   * USB Drive containing system image  
1. Turn on the system
1. Press `F12` to enter boot menu  
1. Select the UEFI Clonezilla USB boot device and press `Enter`  
1. Press `Enter` to accept Clonezilla live (Default settings: VGA 800x600)
1. Press `Enter` to accept English
1. Press `Enter` to accept the default keymap
1. Press `Enter` to start Clonezilla
1. Press `Enter` to work with images
1. Press `Enter` to use local_dev
1. Press `Enter` so the OS can detect the USB device
1. Use the arrow keys to select the USB drive containing the System Image **sdc1 2.7T_ntfs_HarrisBHExt** then press `Enter`
1. Use the arrow keys to select the **BHHPartitionImages** directory and press `Enter`
1. Press `Enter` to accept Beginner Mode
1. Use the arrow keys to seelct restoredisk - Restore an image to a local disk then press `Enter`
1. Use the arrow keys to select **Hosp-Disk_YYY-MM-DD_hh-mm** (the file with the latest date) then press `Enter`
1. Use the arrow keys to select the only internal drive in the computer (something like **500GB_WDC_WD5000BPVT-2**) for overwriting then press `Enter`
1. Note the command being run and press `Enter`
1. Type `y` then press `Enter` to confirm overwriting the drive
1. Type `y` then press `Enter` again to re-confirm overwriting the drive
1. *The overwriting process should take about 7-10 minutes*
1. When everything is done, press `Enter` to continue
1. Use the arrow keys to select **Poweroff** then press `Enter`
1. After the computer shuts down disconnect the USB drives from the system
1. Restart the computer
1. Wait for Windows 8.1 to start up. This could take a while the first time since it will have to get the devices set up. Eventually it should automatically log on to the desktop, start the sensor logger applications, and then lock the desktop.
1. Log into Windows using the TP Sensor Monitor account to make sure the system is working correctly. 
1. Refer to the guide [[Setting Up a Cloned Hospital Computer]] to customize the settings for this computer
1. Turn off the computer and move on to the next one
