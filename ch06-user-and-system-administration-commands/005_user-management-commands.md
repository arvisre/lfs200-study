# Basic User Management Commands </br>  
The basic commands to perform User Administration tasks are **useradd**, **usermod**, and **userdel***. </br>  

## Adding a User Account </br>  
The command **useradd** can be used to add a new user to the system. User administration commands require elevated privileges. </br>  
While the command **sudo useradd (username)** will add a new user, command options can include additional information and set preferences. </br>  
For example, I will be using the command **sudo useradd -c "Tech Support01" -m tech01** to create a user **tech01**. The **-c** option allows me to add a comment field that I have used to specify the account's name. The **-m** option specifies the creation of a **home** directory for the user. </br>  
The following image shows the user account creation operation. </br>  
<img width="713" height="147" alt="Screenshot From 2026-06-24 16-25-30" src="https://github.com/user-attachments/assets/ab9457f6-473d-4118-a8af-20e20eaae2c6" /> </br>  
I can confirm whether the account has been created by checking the **passwd** file at **/etc/**. Using the command **cat /etc/passwd**, I can confirm this action. </br>  
<img width="909" height="150" alt="Screenshot From 2026-06-24 16-27-22" src="https://github.com/user-attachments/assets/57b11891-738a-4303-b8ac-c0e08a165b97" /> </br>  
As shown in the image above, the **login shell** for this user is **/bin/bash**. I can specify this value while creating the user account. When not specified, some default values are applied while user account creation. </br>  
The default values that may be applied can be found in the file **/etc/default/useradd**. Image below: </br>  
<img width="561" height="283" alt="Screenshot From 2026-06-24 16-32-02" src="https://github.com/user-attachments/assets/8b1b67aa-f908-4f66-b00e-b1f21890a53e" /> </br>  

## Setting password for the new user account </br>  
I have to set a password for the user account that I have created. Setting password for other user's account require elevated privileges. </br>  
Using the command **passwd** I have set the initial password for the user account **tech01**. </br>  
Passwords are stored in a secure manner in the **/etc/shadow** file. The following images show the entries for user **tech01** in the **shadow** file before and after setting the password. </br>  
<img width="887" height="270" alt="before passwd" src="https://github.com/user-attachments/assets/19afef2d-50fe-4cfc-91d5-a9309a7bd83f" /> </br>  
<img width="580" height="180" alt="passwd change" src="https://github.com/user-attachments/assets/38cb32d2-0d71-4d53-96bf-26f75ed593ae" /> </br>  
<img width="946" height="180" alt="after passwd" src="https://github.com/user-attachments/assets/1a75de7b-d2bc-4935-9fe2-ec429f39da92" /> </br>  
I can see that before I set the password for **tech01** the entry had an exclamation symbol (!) and after setting the password I can see a long string of alphanumerals and symbols. </br>

Although I have set the initial password for **tech01**, I can use the **--expire** option with the passwd command to expire the password and force the user to change password at next login. </br>  
