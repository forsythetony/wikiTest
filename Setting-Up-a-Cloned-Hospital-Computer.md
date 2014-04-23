### Setting Up a Cloned Hospital Computer

1. Shut down the Kinect software
1. Reset Clock
1. In `\ProgramData\Microsoft\Windows\Start Menu\Programs\Startup\`
   * Rename **10000-Kinect** to **10NNN-Kinect**
1. In `%userprofile%\Desktop\Kinect\`
   1. Rename **10000-Kinect** to **10NNN-Kinect**
   1. Right-click **10NNN-Kinect**, choose **Pin to Taskbar**
   1. Edit **config.txt**, update `-SALERTS 10000` to `-SALERTS 10NNN`
   1. Edit **MountElektro.bat**, use correct path in Z: mount 
1. Connect the correct  Z: drive:
   1. In Windows Explorer, right-click **Z:** and choose **Disconnect** from the shortcut menu
   1. Open command prompt
   1. Type `umount z:` *Yes, umount, not unmount*
   1. Type `%userprofile%\Desktop\Kinect\MountElektro.bat` to connect the correct drive mapping
1. Capture Wi-Fi MAC Address
   1. In the open command prompt
   1. Type ipconfig /all
   1. In **Wireless LAN adapter Wi-Fi** section
   1. Capture **Physical Address:** field
1. Rename computer to **CERT-HOSP-NNN** *IT Pro must approve this*
1. Restart computer
1. Add **CERT-HOSP-000** back into Active Directory *IT Pro must do this*
1. Make sure **Z:** is mapped to the correct network location
1. Delete the contents of `%userprofile%\Desktop\KinectData` folder
1. Turn off the computer and move onto the next one
