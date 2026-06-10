# GPT Disks and Linux Device Names </br>  
In the file devicenames.md, I learned that each SCSI and SATA disk is identified by the Kernel module and has a MAJOR number 8. </br>  
In addition to MAJOR numbers each disk and its partitions are assigned a MINOR number, and each disk can only have 16 partitions. </br>  
The MINOR numbers run from 0-15; 0 assigned to the whole disk and partitions start from 1 till 15. </br>  

## GUID Partition Table </br>  

Unlike MBR - that allowed 4 Primary Partitions (or) 3 Primary Partitions + only 1 Extended Partition (and many logical drives inside Extended Partition), GPT supports 128 partitions. </br>  
Now my question was, when GPT allows 128 partitions and Linux allows on 16 partitions for SCSI and SATA disks, isn't that conflicting? </br>  
Researching further, I learn that the 16-partition limit is legacy device numbering and modern Linux Kernels do not restrict GPT disks to 16 partitions. </br>  

## Verifying whether GPT disks can have more than 16 partitions. </br>  
In my Ubuntu Desktop virtual machine, I added a 2GB SATA disk and using **gparted** I created 20 partitions of 100MB in size. </br>  
The result of that test is shown in the image below: </br>  
<img width="559" height="545" alt="Screenshot From 2026-06-10 15-09-39" src="https://github.com/user-attachments/assets/8c307578-844e-438a-86cf-f17fa773ff97" /> </br>  

As we can see, sda1 through sda15 use major/minor 8:1 through 8:15. sda16 through sda20 no longer use major 8; they move to major 259 with minors 5 through 9. </br>  

Researching further I find as quoted in AI tool: </br>  
<img width="748" height="253" alt="Screenshot From 2026-06-10 15-13-24" src="https://github.com/user-attachments/assets/4f19702a-163f-4801-beb2-3086bd9211f1" />
