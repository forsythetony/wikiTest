### Windows 7
* Open Windows File Explorer
* Right-click on This PC and choose Properties from the shortcut menu
* In the Computer name, domain, and workgroup settings section of the System window click Change settings
* On the Computer Name tab of the System Properties dialog box click the Change button to rename the computer
* In the Computer name field of the Computer Name/Domain Changes dialog box type the new name in the format CERT-HOSP-nnn, where nnn is the incremental number of this system
* Click OK to close the Computer Name/Domain Changes dialog box
* Enter IT Pro credentials in the Windows Security dialog box and click OK to approve the name change
* Click OK in the Computer Name/Domain Changes dialog box to acknowledge that the name change will not take effect until the system is restarted
* Click the Close button in the System Properties dialog box
* Click the Restart Now button to restart the system
* When Windows has restarted log back in to the MU ENGR CERT HOSP Kinect account
* **Note:**  
   Changing the system name here changes the name in Active Directory. Before you can clone the next system you will need to recreate the original account (CERT-HOSP-001) in the Active Directory so the machine can join the domain after it is restored.

Here is an image [[testingShot.png]]