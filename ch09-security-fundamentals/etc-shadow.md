# "/etc/shadow" </br>  
The **"/etc/shadow"** file or simply **shadow** file contains the passwords for the user accounts in a system. Passwords are not stored in plaintext format - they are hashed. </br>  
Hashing in the process of applying an algorith to a string such that no matter how many times the algorithm is applied to the "**SAME**" string, the result is the "**SAME**". This means that the Hash value for the string **Hash** is different that hash value for **hash**. </br>  
Also, **Hashing** is a one-way process - that is - String+Algorithm=>Hash Value. This cannot be reversed. </br>   
Added to the **Hash** is a random string called **Salt** -generated during the password-set time- such that no two users with the same password arrive at the same **Hash** value. </br>  
I have created a user account **tech01** to demonstrate the fields in the **shadow** file. </br>  
<img width="782" height="178" alt="image" src="https://github.com/user-attachments/assets/d87630b3-6ab9-4056-ac79-71c4a15ef880" /> </br>  

Now that I have created a user account **tech01** and I have not set a password yet, I'm displaying the default values for the fields in the **shadow** file: </br>  
<img width="875" height="300" alt="Screenshot From 2026-07-08 21-01-24" src="https://github.com/user-attachments/assets/d540a0d7-9eb2-40fd-b46c-d44e5b5fa0df" /> </br>  
The first field is the username "**tech01**". </br>  
The second field holds the password. At this moment I have NOT set a password for **tech01** and that is why the password field has a **!** symbol. </br>  
I have set the password for the user **tech01** and the changes can be seen in the **shadow** file: </br>  
<img width="965" height="260" alt="Screenshot From 2026-07-08 23-10-17" src="https://github.com/user-attachments/assets/87ee6464-ff13-4de4-8101-1856ed8b69c0" /> </br>  

