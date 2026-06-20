# Network Administrator Commands </br>  
This chapter gives an introduction to the commands:- **dig, ip, netstat, ping, traceroute**. </br>  
Working in IT Support for Microsoft Systems, I have used the ipconfig, ping, tracert (traceroute), and nslookup commands for troubleshooting network related problems. 

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

## Basic explanation of how Name Resolution works in a Linux system: </br>  
Whenever there is a need for Name Resolution, say www.almalinux.org, the following steps occur:  
1. The file **/etc/nsswitch.conf** is accessed and the entry for **hosts** is read. As shown in the image below, the entries for **hosts:** are **files** **dns** **myhostname**.  
<img width="841" height="541" alt="Screenshot From 2026-06-20 23-22-53" src="https://github.com/user-attachments/assets/2c719e56-464c-44ab-8f69-c7ef07a611be" />  
2. In that order, first the **files** as in the **hosts** file is checked. The **hosts** file resides at **/etc/hosts**.  
<img width="779" height="283" alt="Screenshot From 2026-06-20 23-26-08" src="https://github.com/user-attachments/assets/262bb48e-f2f4-4fde-9deb-1caa9ba9a581" />  
3. As shown in the image above, the **hosts** file has only two entries - the IPV4 and IPV6 **loopback address** for the **localhost**.  
4. Since there is no entry for **www.almalinux.org** in the **hosts** file, the next step is to fallback to **dns**.  
5. The answer for "which dns server to ask?" lies in the file **/etc/resolv.conf**. This file has the **nameserver** entry - as shown in image below:  
<img width="551" height="141" alt="image" src="https://github.com/user-attachments/assets/67d89935-7b51-4702-87fc-21ec7ff622d4" />  
6. As shown in the image above, the **nameserver** for this Rocky Linux VM is **192.168.122.1**. Hence, name resolution queries are forwarded to this address.  
7. Step 6 can be verified by using the **dig** command - image below:  
8. <img width="739" height="518" alt="Screenshot From 2026-06-20 23-37-05" src="https://github.com/user-attachments/assets/2fc2df06-0e58-4de3-9029-6a7ed534af89" />  
9. In some distributions such as Ubuntu and Fedora, there is a daemon (service) named **systemd-resolved** that handles **name resolution** and **caching**. Although there can be differences, the **systemd-resolved** daemon (service) sounds similar to the **DNS Client** service that runs in Windows computers.  
10. Images below show the status of the **systemd-resolved** daemon in Fedora and Ubuntu computers. I could not find this daemon running in my Rocky Linux VM.  
<img width="1406" height="569" alt="Screenshot From 2026-06-20 23-46-39" src="https://github.com/user-attachments/assets/1fc30492-3247-4b51-88c6-3e71ae728c88" /> </br>  
<img width="1920" height="742" alt="Screenshot From 2026-06-20 23-47-36" src="https://github.com/user-attachments/assets/5d850a15-3d11-4967-8333-8775dddaa053" />  








