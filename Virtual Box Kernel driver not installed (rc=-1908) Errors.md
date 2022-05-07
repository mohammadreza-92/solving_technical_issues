VirtualBox VM: 


I want to set up a Windows version on VirtualBox (Mac), but there is an error rc=-1908. I followed up on these steps and the problem is solved.  

Steps: 
Open a terminal and run:

`sudo kextload -b org.virtualbox.kext.VBoxDrv`

Step 2: Go into System Preferences->Security & Privacy
Step 3: Unlock the security center
Step 4: Approve the software by Oracle
Step 5:
`
sudo kextload -b org.virtualbox.kext.VBoxNetFlt`  
`sudo kextload -b org.virtualbox.kext.VBoxNetAdp`  
`sudo kextload -b org.virtualbox.kext.VBoxUSB`

Step 6: sudo reboot 

References: 

[Kernel driver not installed (rc=-1908) Getting Errors in macOS Big Sur 11.0.1](https://stackoverflow.com/questions/65149373/kernel-driver-not-installed-rc-1908-getting-errors-in-macos-big-sur-11-0-1)
