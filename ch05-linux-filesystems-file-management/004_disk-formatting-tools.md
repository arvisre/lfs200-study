# Disk Formatting Utilities </br>  
The tutorial lists 5 tools - **fdisk**, **sfdisk**, **parted**, **gnome-disks**, and **gparted**. </br>  
I have used **gparted** in the previous exercise. **gnome-disks** is a also a graphical tool like **gparted**. </br>  
Hence, I am going to use **fdisk** a purely command-line based disk utility. </br>  
The command **lsblk -p** prints the list of block devices along with their directory path. </br>  
<img width="510" height="544" alt="Screenshot From 2026-06-10 18-54-29" src="https://github.com/user-attachments/assets/762bce6e-0afe-4806-937c-33330dac4566" /> </br>  

In this exercise, I am going to use the **fdisk** tool, to delete existing partitions, initialise disks, and create partitions.
