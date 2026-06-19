# System Administrator Commands </br>  
The following commands were listed as Sys-Admin Commands - **apt, chgrp, chmod, chown, fdisk, iostat, ps, dnf, vmstat, zypper**. </br>  

The command **zypper** is used to install, remove, and maintain software packages in SUSE systems. </br>  
Since I have a openSUSE Leap 16 virtual machine recently installed, I would like to try using **zypper** to carry out the first package maintenance activity. </br>  
Interestingly, the installation process of openSUSE presents a slightly different experience from Ubuntu and Rocky Linux. </br>  
As shown in the image below, the installer **Agama** appears to be browser based. By default, no **Graphical Environments** are selected, allowing the user to choose one.  
<img width="1321" height="877" alt="Screenshot From 2026-06-19 10-23-10" src="https://github.com/user-attachments/assets/f72c75e5-9d28-454f-b7a1-25ae95391c40" /> </br>  
Selecting the **GNOME Desktop Environment** auto-selects some additional desktop tools and utilities. These can be unselected if not required.  
<img width="1321" height="877" alt="Screenshot From 2026-06-19 10-24-49" src="https://github.com/user-attachments/assets/40b4e98a-d967-4890-9f1a-b058fcb13163" /> </br>  
The installer also provides options to install certain **Server Roles / Functions**, as shown below:  
<img width="1321" height="877" alt="Screenshot From 2026-06-19 10-25-35" src="https://github.com/user-attachments/assets/a7181a20-fc41-4ffa-8e36-38f90cfb8d33" /> </br>  
Unlike the default **ext4** filesystem in Ubuntu and the **xfs** filesystem in Rocky Linux, **btrfs** is the default filesystem for the **/** partition in openSUSE.
<img width="1059" height="728" alt="Screenshot From 2026-06-19 10-21-15" src="https://github.com/user-attachments/assets/a80ef131-cfa2-4975-99e4-2bd1cda36cab" /> </br>  
Let's use the **zypper** command to update the system.  





