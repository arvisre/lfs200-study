# "/etc/passwd"  
The /etc/passwd file contains information about every user account in the system. Every entry in the file has 7 fields that are separated by a colon (:). </br>  
<img width="779" height="538" alt="image" src="https://github.com/user-attachments/assets/79f2890a-0476-4bca-b357-85f42abe41f1" /> </br>  
The first field is the **username**, which we use to login to the system, followed by the **password** field. This field shows **x** to denote that the password for this user is encrypted. Passwords are stored in another file called **shadow**. </br>  
The third field is the **user id (uid)** and is followed by the **group id (gid)**. Each of these fields have numbers in them. </br>  
The fifth field is **GECOS** aka **Comment** field, which can be used to provide First and Last Name of the user. The argument for **-c** option in **useradd** and **usermod** commands lands in this **GECOS/Comment** field. </br>  
The sixth field is the **home directory** path field and is followed by the seventh and the last field, which holds the **default shell** path. </br>  
In the image below, I have sorted the /etc/passwd file based on **uid**. </br>  
<img width="999" height="298" alt="image" src="https://github.com/user-attachments/assets/1303987b-0b6d-4a7d-92a0-b740cb74ba0f" /> </br>  

