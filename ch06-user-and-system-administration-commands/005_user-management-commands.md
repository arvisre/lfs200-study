# Basic User Management Commands </br>  
The basic commands to perform User Administration tasks are **useradd**, **usermod**, and **userdel***. </br>  

## Adding a User Account </br>  
The command **useradd** can be used to add a new user to the system. User administration commands require elevated privileges. </br>  
While the command **sudo useradd (username)** will add a new user, command options can include additional information and set preferences. </br>  
For example, I will be using the command **sudo useradd -c "Tech Support01" -m tech01** to create a user **tech01**. The **-c** option allows me to add a comment field that I have used to specify the account's name. The **-m** option specifies the creation of a **home** directory for the user. </br>  
The following image shows the user account creation operation.  
<img width="713" height="147" alt="Screenshot From 2026-06-24 16-25-30" src="https://github.com/user-attachments/assets/ab9457f6-473d-4118-a8af-20e20eaae2c6" /> </br>  
