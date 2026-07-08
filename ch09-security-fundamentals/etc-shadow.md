# "/etc/shadow" </br>  
The **"/etc/shadow"** file or simply **shadow** file contains the passwords for the user accounts in a system. Passwords are not stored in plaintext format - they are hashed. </br>  
Hashing in the process of applying an algorith to a string such that no matter how many times the algorithm is applied to the **"SAME"** string, the result is the **"SAME"**. This means that the Hash value for the string **Hash** is different that hash value for **hash**. </br>  
Added to the **Hash** is a random string called **Salt** -generated during the password-set time- such that no two users with the same password arrive at the same **Hash** value. </br>  
I have created a user account **tech01** to demonstrate the fields in the **shadow** file. </br>  
<img width="782" height="178" alt="image" src="https://github.com/user-attachments/assets/d87630b3-6ab9-4056-ac79-71c4a15ef880" /> </br>  

