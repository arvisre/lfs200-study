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
One of the first commands to execute is the **id** command - to check whether my user id has the permissions to run the command **sudo**. By default my user id has been
added to the group **wheel** and consequently will have permissions to run the **sudo** command. </br>  
Then I run the command **zypper --help** to display the list of command options - as shown in the image below:  
<img width="1141" height="947" alt="image" src="https://github.com/user-attachments/assets/d1ff6d7a-0309-4ea0-b612-8e7e43445495" /> </br>  
The option **--help** display a long list of options categorised under various tasks, and to being with, I am going to focus on the **Update Management** category.  
<img width="890" height="952" alt="image" src="https://github.com/user-attachments/assets/7393c4df-7e19-4598-9176-637977fee26e" /> </br>  

The command **sudo zypper update** provided detailed information about packages that will be upgraded, that will not be upgraded, and those that require a reboot - as shown in the images below:
<img width="943" height="288" alt="image" src="https://github.com/user-attachments/assets/6d3bce87-330d-44bd-bef5-8d32c25b1935" /> </br>  
<img width="1072" height="325" alt="image" src="https://github.com/user-attachments/assets/b5383162-0bc1-4080-a912-d66283dfb76c" /> </br>  
<img width="845" height="308" alt="image" src="https://github.com/user-attachments/assets/1621e73f-89c4-4102-82e0-8aae03785a19" /> </br>  









