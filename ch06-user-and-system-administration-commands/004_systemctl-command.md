# systemctl Command </br>  
In Linux distributions, the **systemctl** command is used to control **systemd** which manages **services** and **units**. **systemctl** can check the **status** of a service, **start**, **stop**, **restart**, **enable**, and **disable** services. </br>  
I have installed the **nginx** package in my Ubuntu VM and will demonstrate the use of **systemctl** commands: </br>  
<img width="767" height="356" alt="Install nginx" src="https://github.com/user-attachments/assets/ef9ba312-09d8-4d2a-9a42-7cd022641f4a" /> </br>  

### Checking status of a service </br>  
<img width="1036" height="397" alt="systemctl status" src="https://github.com/user-attachments/assets/95b6c4b7-5bb3-4940-afc8-7e800c1ffe40" /> </br>  
As shown in the image above, the **nginx** service is currently **enabled**, by default **enabled**, and currently **running**. </br>  
The **preset** field indicates the default behaviour of the service. </br>  

### Stopping, Starting, and Restarting a service </br>  
Modiying the current status of a service requires elevated privileges. Hence, I need to use **sudo** for the following commands: </br>  
<img width="1036" height="397" alt="Stop nginx" src="https://github.com/user-attachments/assets/a273e003-2291-4005-80c7-261ea3963cf2" /> </br>  
<img width="1042" height="424" alt="Start nginx" src="https://github.com/user-attachments/assets/f1804d40-565f-4e83-8481-6e1ad711a3fd" /> </br>  
<img width="1042" height="424" alt="Restart nginx" src="https://github.com/user-attachments/assets/b6369a09-d33d-4f04-9c7c-b9db0c3f40a9" /> </br>  

### Disabling and Enabling a service </br>  
Similar to Stop, Start, and Restart, disabling and enabling a service requires **sudo** permissions: </br>  
The **preset** field for the **nginx** service is set to **enabled**. Hence, I am going to modify this behaviour. </br>  
The command **sudo systemctl disable nginx** sets the service behaviour to **disabled**. This change means that **nginx** service will not **start** running after a reboot. However, this change takes effect only after I reboot my computer. Until the time I reboot my computer, the service will be **active(running)** - unless I issue the command **sudo systemctl stop nginx**. </br>  
Alternatively, I can issue the command **sudo systemctl disable --now nginx** to immediately **stop** the service and **disabled** it from starting from the next reboot onwards. See image below: </br>  
<img width="990" height="498" alt="disable--now" src="https://github.com/user-attachments/assets/6bd3e9de-2274-4ce1-85d2-1d918992e6b5" /> </br>  
After a reboot, I note that **sudo systemctl disable nginx** command has disabled the service from running automatically. </br>  
<img width="839" height="209" alt="Screenshot From 2026-06-23 18-02-17" src="https://github.com/user-attachments/assets/6ad0c17c-2b3b-44d5-a534-5f9fc541708c" /> </br>  
The command **sudo systemctl enable nginx** enables the service. However, a reboot is required for changes to take effect. This can be seen in the image below:  
<img width="907" height="321" alt="Screenshot From 2026-06-23 18-06-43" src="https://github.com/user-attachments/assets/1d57b62f-2a20-41ff-ba21-c896a6d61f2c" /> </br>  


### Poweroff and Reboot computer </br>  
**systemctl** can be used to **reboot** and **poweroff** a computer. The commands **systemctl reboot** and **systemctl poweroff** gracefully restart and shutdown a computer. </br>  
For more aggressive restart or shutdown, the **--force** switch can be used. Example **sudo systemctl reboot --force** or **sudo systemctl poweroff --force** </br>  





