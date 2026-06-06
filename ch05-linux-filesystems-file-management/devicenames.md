#  Linux Device Names  </br>  
In Linux the devices are found under the /dev directory. Devices are categorised based on the Kernel module (device driver).</br>  
For example SCSI and SATA device names begin with "**sd**" while the modern NVME SSDs have names that begin with "nvme".</br>  
I have created SCSI and SATA drives for my Ubuntu VM as shown below.</br>  
<img width="1182" height="417" alt="Screenshot From 2026-06-06 14-54-36" src="https://github.com/user-attachments/assets/f2f1a10b-92d8-4776-bc38-0fc4a7c22a19" />  </br>  
When the command **lsblk** is executed in the Ubuntu VM the list of **Block** devices are displayed.</br>  
<img width="697" height="604" alt="Screenshot From 2026-06-06 14-58-10" src="https://github.com/user-attachments/assets/412ddcac-4c9d-4e73-b5f0-fa93c42d6ed0" /> </br>  
From the image above, we find the two drives **sda** and **sdb**. Each device has a **MAJOR:MINOR** number. The Kernel Module (device driver) defines the MAJOR number while the MINOR number points to the instance of the device. </br>  
**sda      8:0    0     2G  0 disk** </br>  
**sdb      8:16   0     2G  0 disk** </br>  
The MAJOR number for sda and sdb are 8 and the MINOR numbers are 0-15 for sda and 16-31 for sdb. Each of these devices sda and sdb can have 16 partitions (instances). sda 8:0 refers to the whole disk whereas sda 8:1 refers to first partition and sda 8:15 refers to the last partition of that disk. </br>  
Similarly, sdb 8:16 refers to the whole disk, sdb 8:17 refers to the first partition and sdb 8:31 to the last partition in sdb. </br>  
Using the **gparted** graphical utility, I have initialised the disks **sda** and **sdb** and created two partitions in each of them. The following image shows the concept of MAJOR:MINOR numbers and how Linux names devices. </br>  
<img width="699" height="691" alt="Screenshot From 2026-06-06 15-22-04" src="https://github.com/user-attachments/assets/485226e6-bce6-451f-883d-35010bd35744" /> </br>  
As mentioned earlier, the disks and their partitions are listed in the **/dev** directory. Using the **ls** command we can list those devices - as shown below: </br>  
<img width="646" height="235" alt="Screenshot From 2026-06-06 15-28-03" src="https://github.com/user-attachments/assets/89ee43d9-dfce-4912-a515-e10550511c81" /> </br>  
Likewise, using the **find** command, I have listed the **nvme** devices connected to the Host Computer that runs Fedora Workstation (image below) </br>  
<img width="736" height="434" alt="Screenshot From 2026-06-06 15-33-27" src="https://github.com/user-attachments/assets/2d71497f-6b76-4788-a779-47eac32994ca" />

