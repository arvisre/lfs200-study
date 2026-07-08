# "/etc/shadow" </br>  
The **"/etc/shadow"** file or simply **shadow** file contains the passwords for the user accounts in a system. Passwords are not stored in plaintext format - they are hashed. </br>  
Hashing in the process of applying an algorith to a string such that no matter how many times the algorithm is applied to the "**SAME**" string, the result is the "**SAME**". This means that the Hash value for the string **Hash** is different that hash value for **hash**. </br>  
Also, **Hashing** is a one-way process - that is - String+Algorithm=>Hash Value. This cannot be reversed. </br>   
Added to the **Hash** is a random string called **Salt** -generated during the password-set time- such that no two users with the same password arrive at the same **Hash** value. </br>  
I have created a user account **tech01** to demonstrate the fields in the **shadow** file. </br>  
<img width="782" height="178" alt="image" src="https://github.com/user-attachments/assets/d87630b3-6ab9-4056-ac79-71c4a15ef880" /> </br>  

Now that I have created a user account **tech01** and I have not set a password yet, I'm displaying the default values for the fields in the **shadow** file: </br>  
<img width="875" height="300" alt="Screenshot From 2026-07-08 21-01-24" src="https://github.com/user-attachments/assets/d540a0d7-9eb2-40fd-b46c-d44e5b5fa0df" /> </br>  
1. The first field is the username "**tech01**". </br>  
2. The second field holds the password. At this moment I have NOT set a password for **tech01** and that is why the password field has a **!** symbol. </br>  
I have set the password for the user **tech01** and the changes can be seen in the **shadow** file: </br>  
<img width="965" height="260" alt="Screenshot From 2026-07-08 23-10-17" src="https://github.com/user-attachments/assets/87ee6464-ff13-4de4-8101-1856ed8b69c0" /> </br>  
3. The third field is the "Last Password Change" - that is the number of days since 1st January 1970 (**epoch**). In this case it is 20642 days since 01/01/1970 (**epoch**). </br>  
4. The fourth field is the "Minimum Password Age" - that is the number of days that must pass for the password to be changed. In this case it is **0**. So there is NO restriction and I can change the password without waiting for a number of days to pass. </br>  
5. The fifth field is the "Maximum Password Age" - that is the maximum number of days a password can be valid before it must be change. In this example, the value is 99999 days </br>
6. The sixth field is the "Password Warning Period" - that is the number of days before the password expiry date the user starts getting warning messages during login. In the above image the value is set to the default 7 days. </br>
7. The seventh field is the "Password Inactivity Period" - that is the number of days AFTER PASSWORD EXPIRATION that the account is still valid before the ACCOUNT IS LOCKED OUT. In the image above this field is empty, meaning this action is NOT enforced. </br>
8. The eighth field is the "Account Expiration Date" - that is the number of days from 01/January/1970 (**epoch**) that the account must expire. In the example above this field is empty, meaning that this account does NOT expire. </br>  
9. The last and the final ninth field is reserved for future use. </br>

## Changing password at next logon for user tech01 </br>  
I have set a temporary password for **tech01** and want the user to change the password at next logon. To achieve this, I can use two commands: 1. sudo passwd -e tech01 (or) 2. sudo chage -d 0 tech01. These commands set the **third field** in the **shadow** file to **0**, which triggers the system to change password at next logon. </br>  
<img width="920" height="247" alt="Screenshot From 2026-07-08 23-37-00" src="https://github.com/user-attachments/assets/e9af8d54-b74c-4dc4-be18-574480ed350c" /> </br>  
Strangely, the "Last Password Change" field for my user account is **blank**. That is because it was created during system installation and the installer must not have updated this field. See image below: </br>  
<img width="920" height="247" alt="Screenshot From 2026-07-08 23-37-00" src="https://github.com/user-attachments/assets/f8a4abf7-b625-45a9-8743-3941179285a4" /> </br>  
Logging in as **tech01**, I am prompted to change the password: </br>  
<img width="876" height="511" alt="Screenshot From 2026-07-08 23-48-29" src="https://github.com/user-attachments/assets/21cc9005-9391-42b7-9acb-57e29e838c2c" /> </br>  
I have changed the password for **tech01** and can be verified by the different **Hash Value** and **Last Password Change** field: </br>  
<img width="955" height="206" alt="Screenshot From 2026-07-08 23-52-29" src="https://github.com/user-attachments/assets/3cc5c3ea-c174-4d07-964f-297341882f19" /> </br>  
I will force expire the **tech01** account using the command **chage**: </br>  
Executing the command **sudo chage -E 0 tech01** force expires the **tech01** account immediately and sets the **eighth** field (**Account Expiration Date**) in the **shadow** file to **0**: </br>  
<img width="966" height="224" alt="Screenshot From 2026-07-08 23-56-29" src="https://github.com/user-attachments/assets/6d6d3bb6-4d16-4634-9543-09a52940312f" /> </br>  
