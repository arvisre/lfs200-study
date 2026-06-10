# Disk Formatting Utilities </br>  
The tutorial lists 5 tools - **fdisk**, **sfdisk**, **parted**, **gnome-disks**, and **gparted**. </br>  
I have used **gparted** in the previous exercise. **gnome-disks** is a also a graphical tool like **gparted**. </br>  
Hence, I am going to use **fdisk** a purely command-line based disk utility. </br>  
The command **lsblk -p** prints the list of block devices along with their directory path. </br>  
<img width="510" height="544" alt="Screenshot From 2026-06-10 18-54-29" src="https://github.com/user-attachments/assets/762bce6e-0afe-4806-937c-33330dac4566" /> </br>  

In this exercise, I am going to use the **fdisk** tool, to delete existing partitions, initialise disks, and create partitions. </br>  

## Selecting a disk to work with: </br>  
<img width="864" height="298" alt="Screenshot From 2026-06-10 18-59-19" src="https://github.com/user-attachments/assets/d5966329-4c2c-4d36-8d6d-a5902813bdac" /> </br>  

## Creating a GPT partition table on a disk </br>  
<img width="696" height="534" alt="Screenshot From 2026-06-10 19-01-07" src="https://github.com/user-attachments/assets/146775b7-2231-4fab-8507-43e662cd54bb" /> </br>  

## Displaying the details of the disk </br>  
<img width="537" height="245" alt="Screenshot From 2026-06-10 19-02-47" src="https://github.com/user-attachments/assets/9d44961a-e240-4e03-9d48-fc9153e9100b" /> </br>  

## Creating a new partition of Size 1 GB </br>  
<img width="976" height="185" alt="Screenshot From 2026-06-10 19-09-43" src="https://github.com/user-attachments/assets/8f3b4202-af3e-4926-98fa-8260bb6e4aee" /> </br>  

## Writing changes to disk </br>  
<img width="884" height="145" alt="Screenshot From 2026-06-10 19-10-25" src="https://github.com/user-attachments/assets/ac204c46-3cee-41e1-91a2-2408428798d3" /> </br>  

## Creating a second partition with rest of the available space </br>  
<img width="884" height="167" alt="Screenshot From 2026-06-10 19-11-47" src="https://github.com/user-attachments/assets/729087e6-4abd-4fe1-8c66-86c6c66ee32a" /> </br>  

## Writing changes to disk </br>  
<img width="884" height="135" alt="Screenshot From 2026-06-10 19-12-02" src="https://github.com/user-attachments/assets/b53efbdd-fb21-4641-8ba8-ae5db9229a74" /> </br>  

## Selecting a disk to work with (for deleting a partition): </br>  
<img width="856" height="529" alt="Screenshot From 2026-06-10 19-15-26" src="https://github.com/user-attachments/assets/c7724c90-fe6d-4cbc-81b2-a663b8d666bc" /> </br>  

## Deleting a partition from the disk: </br>  
<img width="524" height="538" alt="Screenshot From 2026-06-10 19-15-59" src="https://github.com/user-attachments/assets/cef146b3-f4bd-4bea-abe0-e317a7690865" /> </br>  

## Writing changes to disk </br>  
<img width="524" height="538" alt="Screenshot From 2026-06-10 19-16-10" src="https://github.com/user-attachments/assets/fb214e4f-7dd7-4cc8-8cce-e50e53a4b462" /> </br>  

## Verifying that 2 partitions have been created and 1 partition has been deleted </br>  
<img width="524" height="623" alt="Screenshot From 2026-06-10 19-17-18" src="https://github.com/user-attachments/assets/57b57557-1c01-43b2-8d16-59b5cb0b5ef6" /> </br>  

Using the **fdisk** utility, we have initialised **/dev/sdb** as GPT disk, created two partitions in it, and we have deleted one partition from **/dev/sda**  












