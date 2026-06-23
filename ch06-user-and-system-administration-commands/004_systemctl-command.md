# systemctl Command </br>  
In Linux distributions, the **systemctl** command is used to control **systemd** which manages **services** and **units**. **systemctl** can check the **status** of a service, **start**, **stop**, **restart**, **enable**, and **disable** services. </br>  
I have installed the **nginx** package in my Ubuntu VM and will demonstrate the use of **systemctl** commands: </br>  
<img width="767" height="356" alt="Install nginx" src="https://github.com/user-attachments/assets/ef9ba312-09d8-4d2a-9a42-7cd022641f4a" /> </br>  

### Checking status of a service </br>  
<img width="1036" height="397" alt="systemctl status" src="https://github.com/user-attachments/assets/95b6c4b7-5bb3-4940-afc8-7e800c1ffe40" /> </br>  
As shown in the image above, the **nginx** service is currently **enabled**, by default **enabled**, and currently **running**. </br>  

### Stopping, Starting, and Restarting a service </br>  
Modiying the current status of a service requires elevated privileges. Hence, I need to use **sudo** for the following commands: </br>  
<img width="1036" height="397" alt="Stop nginx" src="https://github.com/user-attachments/assets/a273e003-2291-4005-80c7-261ea3963cf2" /> </br>  
<img width="1042" height="424" alt="Start nginx" src="https://github.com/user-attachments/assets/f1804d40-565f-4e83-8481-6e1ad711a3fd" /> </br>  
<img width="1042" height="424" alt="Restart nginx" src="https://github.com/user-attachments/assets/b6369a09-d33d-4f04-9c7c-b9db0c3f40a9" /> </br>  

### Disabling and Enabling a service </br>  
