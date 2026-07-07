# System Administrator Commands </br>  
The following commands were listed as Sys-Admin Commands - **apt, chgrp, chmod, chown, fdisk, iostat, ps, dnf, vmstat, zypper**. </br>  

The command **zypper** is used to install, remove, and maintain software packages in SUSE systems. </br>  
Since I have a openSUSE Leap 16 virtual machine recently installed, I would like to try using **zypper** to carry out the first package maintenance activity. </br>  
Interestingly, the installation process of openSUSE presents a slightly different experience from Ubuntu and Rocky Linux. </br>  
As shown in the image below, the installer **Agama** appears to be browser based. By default, no **Graphical Environments** are selected, allowing the user to choose one. </br>  
<img width="1321" height="877" alt="Screenshot From 2026-06-19 10-23-10" src="https://github.com/user-attachments/assets/f72c75e5-9d28-454f-b7a1-25ae95391c40" /> </br>  
Selecting the **GNOME Desktop Environment** auto-selects some additional desktop tools and utilities. These can be unselected if not required. </br>  
<img width="1321" height="877" alt="Screenshot From 2026-06-19 10-24-49" src="https://github.com/user-attachments/assets/40b4e98a-d967-4890-9f1a-b058fcb13163" /> </br>  
The installer also provides options to install certain **Server Roles / Functions**, as shown below: </br>  
<img width="1321" height="877" alt="Screenshot From 2026-06-19 10-25-35" src="https://github.com/user-attachments/assets/a7181a20-fc41-4ffa-8e36-38f90cfb8d33" /> </br>  
Unlike the default **ext4** filesystem in Ubuntu and the **xfs** filesystem in Rocky Linux, **btrfs** is the default filesystem for the **/** partition in openSUSE. </br>  
<img width="1059" height="728" alt="Screenshot From 2026-06-19 10-21-15" src="https://github.com/user-attachments/assets/a80ef131-cfa2-4975-99e4-2bd1cda36cab" /> </br>  
Let's use the **zypper** command to update the system. </br>  
One of the first commands to execute is the **id** command - to check whether my user id has the permissions to run the command **sudo**. By default my user id has been added to the group **wheel** and consequently will have permissions to run the **sudo** command. </br>  
Then I run the command **zypper --help** to display the list of command options - as shown in the image below: </br>  
<img width="1141" height="947" alt="image" src="https://github.com/user-attachments/assets/d1ff6d7a-0309-4ea0-b612-8e7e43445495" /> </br>  
The option **--help** display a long list of options categorised under various tasks, and to being with, I am going to focus on the **Update Management** category. </br>  
<img width="890" height="952" alt="image" src="https://github.com/user-attachments/assets/7393c4df-7e19-4598-9176-637977fee26e" /> </br>  

The command **sudo zypper update** provided detailed information about packages that will be upgraded, that will not be upgraded, and those that require a reboot - as shown in the images below: </br>  
<img width="943" height="288" alt="image" src="https://github.com/user-attachments/assets/6d3bce87-330d-44bd-bef5-8d32c25b1935" /> </br>  
<img width="1072" height="325" alt="image" src="https://github.com/user-attachments/assets/b5383162-0bc1-4080-a912-d66283dfb76c" /> </br>  
Pressing **y** will continue the process of downloading the packages and updating the current system. </br>  
<img width="845" height="308" alt="image" src="https://github.com/user-attachments/assets/1621e73f-89c4-4102-82e0-8aae03785a19" /> </br>  
Restarting the computer will apply the updates that were installed. </br>  
<img width="1564" height="325" alt="image" src="https://github.com/user-attachments/assets/ea74a735-a0aa-48d8-b9a0-d6b2185372ce" /> </br>    
In RedHat-based systems the command **sudo dnf check-update** refreshes the repositories and provides a list of available updates. I was wondering if a similar command exists for SUSE-based systems. It appears that in SUSE-based systems the commands **sudo zypper refresh** and **sudo zypper list-updates** do the similar functions respectively. </br>  
<img width="998" height="747" alt="image" src="https://github.com/user-attachments/assets/9de72d6f-0606-475f-bb1a-ea03504761f1" /> </br>  
<img width="661" height="202" alt="image" src="https://github.com/user-attachments/assets/c38bac44-0f1e-4cc8-9c60-8cc909d98e65" /> </br>  

## Searching and installing a package: </br>  
Further, I am going use the **search** option to find if the package **gnome-tweaks** exists and try to install it. </br>  
<img width="1077" height="545" alt="image" src="https://github.com/user-attachments/assets/57925a56-0288-4fa2-96ed-9cba6b64ee96" /> </br>  
I find that the package **gnome-tweaks** is already installed. Hence I am going to find it in the list of all packages. </br>  
Pressing **TAB** after typing the command **sudo zypper package** gives further options and I am going to choose the option **--installed only** </br>  
<img width="1304" height="523" alt="image" src="https://github.com/user-attachments/assets/04b2db82-5e60-4cd8-87fc-5b004d15d286" /> </br>  
Since this command lists hundreds of packages, I am going to check if I can use the command **grep** to check whether I can find the package **gnome-tweaks**. For this, I am going to **pipe (|)** the output of the first command into the **grep** command. </br>  
The **pipe** operation worked and I can now see that **gnome-tweaks** was installed: </br>  
<img width="1319" height="168" alt="image" src="https://github.com/user-attachments/assets/8bbc65ef-7bd0-4ec4-a83b-e0533ffc1d01" /> </br>  

The following images display the software upgrade process in Fedora/RHEL-based systems: </br>  
<img width="879" height="977" alt="Removing and Upgrading Packages" src="https://github.com/user-attachments/assets/53ca9988-6291-40d0-8558-709b845e19fb" /> </br>  
<img width="1080" height="820" alt="Installing Packages" src="https://github.com/user-attachments/assets/75395794-921a-400e-bed9-778a40a5805e" /> </br>  
