# Network Administrator Commands </br>  
This chapter gives an introduction to the commands:- **dig, ip, netstat, ping, traceroute**. </br>  
Working in IT Support for Microsoft Systems, I have used the ipconfig, ping, traceroute, and nslookup commands for troubleshooting network related problems. 

## ip command / utility </br>  
The command **ip** consists of **objects** and these **objects** have **commands** to carry out specific tasks. </br>  
For example, when we type the command **ip** in the terminal and press the TAB twice, we get to see the **objects**. Once we have chosen an **object**, pressing the TAB twice
lists the **commands** that work on these **objects**. Let's look at the image below:  
<img width="1296" height="776" alt="image" src="https://github.com/user-attachments/assets/a475da5f-5ddf-4ab0-95cd-ec785c6dce7a" /> </br>  
Typing **ip** and pressing TAB twice lists the **objects** I can use. Here I've chosen **address** as the object. Pressing TAB twice now lists the **commands** such as **add, change, del, show, etc** that work with the object **address**. </br>  
I have chosen the **command** **show** and entering this command lists the **Network Adapters** in my computer and corresponding details of each adapter. This command is equivalent to the **ipconfig /all** used in Windows environments. </br>  
Similarly, as shown below, the **ip** utility with the **object** **route** and with the **command** **list** displays the **routing** information.  
<img width="1267" height="277" alt="image" src="https://github.com/user-attachments/assets/44e95052-186f-40fd-b7ea-1bc57fa64239" />  
This command is equivalent to the **route print** command used in Windows environments. </br>  
Additionally - the **ip** command has replaced the **ifconfig** command. While my Fedora Workstation has both **ip** and **ifconfig** commands, my Ubuntu VM does NOT have **ifconfig** by default. </br>  

## dig command / utility </br>  
"**nslookup**" was one of the commands I used in Windows environments to verify name resolution. Although, **nslookup** can still be used in Linux computers, the command has been replaced by **dig**. </br>  
The basic usage of **dig** utility is **dig (domain name)** as shown in the image below:  
<img width="843" height="503" alt="Screenshot From 2026-06-20 22-36-17" src="https://github.com/user-attachments/assets/75dacd4b-5d14-4bd7-b783-d76e1e856814" /> </br>  
In the above example, the **SERVER** is 127.0.0.53 - the name resolution service in the local computer. I can also specify a **SERVER** to use for name resolution - see image below:  
<img width="786" height="564" alt="Screenshot From 2026-06-20 22-37-43" src="https://github.com/user-attachments/assets/8ce6c1e3-39bb-4b99-b04c-67e2f6c5af56" />  
In the above example, I have specified "**@1.1.1.1**" as the **SERVER** I want to use for name resolution. </br>  
**dig** can also be used for **reverse query** - that is resolving an **IP Address** to **Domain Name** - see image below:  
<img width="782" height="539" alt="Screenshot From 2026-06-20 22-40-25" src="https://github.com/user-attachments/assets/3074cad8-f044-4c82-b3a3-a067e1a99eae" />  
In the above example, I have used the **-x** option to query the **domain name** for the **ip address** </br>  


