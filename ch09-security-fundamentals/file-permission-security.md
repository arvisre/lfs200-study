# Linux File Permissions Security </br>  
The **ls** command with the long-listing option **-l** provides more insight about a directory or file. The information includes type of file along with file permissions, number of hard links, user owner, group owner, size in bytes, modification date, and file name. Depending on the type of file some fields may or may NOT show. </br>  
The following image shows the information **ls -l** displays for a **directory** and a **file** inside the directory. </br>  
<img width="1152" height="453" alt="Screenshot From 2026-07-21 08-05-15" src="https://github.com/user-attachments/assets/0914a738-2107-4fea-b1e6-f7d7d5de27d4" /> </br>  
Some of the file types as shown in the image below: </br>  
<img width="687" height="401" alt="Screenshot From 2026-07-21 08-21-06" src="https://github.com/user-attachments/assets/6eafc153-eb7c-40c1-9066-03a14bd30ea6" /> </br>
**c** for character device files  
**d** for directory  
**l** for links  
**b** for block device files </br>  

## File Permissions: </br>  
Each file (a directory is also considered a type of file) has permissions attached to it. The permissions are Read(**r**), Write(**w**), and Execute(**x**). These permissions are applied to three entities namely, User(**u**), Group(**g**), and Other(**o**). </br>  
Using r,w,x,u,g, and o notations is called the **Symbolic Method**. The alternative to this method is the Octal or Numerical Method in which numbers are assigned to r,w, and x permissions. </br>  
In the **Octal Method**, Read(r) is given a value of 4, Write(w) a value of 2, and Execute(x) a value of 1. These are applied to User(u), Group(g), and Other(o) placeholders. </br>  

## chmod command: </br>  
The command **chmod** is used to modify permissions on resources. Elevated privilege (**sudo**) is required for resources that the user does NOT own. </br>  

## User, Group, Other placeholders: </br>  
<img width="472" height="130" alt="Screenshot From 2026-07-21 11-09-40" src="https://github.com/user-attachments/assets/6fa36da6-4a0b-4a72-a431-ad35f63bdc47" /> </br>  
In the image above, the first placeholder - marked in RED, denotes the **Type of File**. A **Regular File** file, like the one in the image, has a blank for this placeholder. A **Directory** would have **d** at this spot. </br>  
The **Second set** - marked in BLUE - denotes the permissions for the **User Owner** to the resource. This Second set has three placeholders for Read, Write, and Execute. Similarly, the **Third set** - marked in GREEN - denotes the permissions for the **Group Owner** to the resource. The **Fourth set** - marked in YELLOW - denotes the permissions for **Other** to the resource. </br>  
As per the image below, the User Owner, the Group Ownver, and Other have Read, Write, and Execute permissions for the file file1.txt. This can be inferred from the -rwxrwxrwx permissions for the file.</br>  
<img width="472" height="130" alt="Screenshot From 2026-07-21 11-17-57" src="https://github.com/user-attachments/assets/44ebf3c7-8c53-4ccd-b58c-79787af8a99a" /> </br>  

## Providing Permissions using Symbolic method: </br>  
I am going to use the file file1.txt to add and remove permissions. As seen in the image below, the User Owner(u) has Read and Write permissions, the Group Owner(g) and Other(u) have Read permissions. </br>  
<img width="447" height="120" alt="Screenshot From 2026-07-21 11-38-53" src="https://github.com/user-attachments/assets/a8725f26-61d8-47d6-b226-b80819335734" /> </br>  
In the **Symbolic method**, the **+** symbol is used to add permissions, the **-** symbol is used to remove persmissions, and the **=** symbol is used to set exact permissions.  
For example, to **remove** WRITE permission from the **User Owner(u)**, the following command can be used: **chmod u-w file1.txt** </br>  
Since I own this file I am working on, I have NOT used elevated privilege. </br>  
To **add** EXECUTE permissions to **Other**, the following command can be used: **chmod o+x file1.txt** </br>  
To **set** WRITE and EXECUTE permissions for the **Group Owner**, the following command can be used: **chmod g=rwx file1.txt**. Alternatively, this task can be achieved by **chmod g+wx file1.txt** </br>  
<img width="552" height="567" alt="Screenshot From 2026-07-21 11-52-23" src="https://github.com/user-attachments/assets/acd75478-c8a2-440d-977e-d8907d7c6975" /> </br>  

## Providing Permissions using Octal method: </br>  
In the **Octal method** a value is assigned to each permission. Read(r)=4, Write(w)=2, and Execute(x)=1. The values are them added together for each entity User(u), Group(g), and Other(u). Instead of specifying u,g,and o, the sum of permissions is specified for each entity. </br>  
I am going to use the file file1.txt for demonstration. The file currently has rw-r--r-- for user, group, and other respectively. I am going to add execute permissions for **User Owner** using the command **chmod 744 file1.txt**. Since the User Owner already has Read(4) and Write(2) permissions, I need to add Execute(1) to the existing permissions. These values add up to 7. The **Group Owner** and **Other** have Read(4) permissions and I have to specify them also. </br>  
<img width="549" height="195" alt="Screenshot From 2026-07-21 12-19-37" src="https://github.com/user-attachments/assets/d821ead0-e6bb-45c8-aa3f-5ac63f96d4c9" /> </br>  
In the above example, if I do NOT specify the permission values for **Group Owner** and **Other** and issue the command **chmod 7 file1.txt** or **chmod 7-- file1.txt** or **chmod 700 file1.txt**, the results will vastly vary and result in unexpected outcomes. See images below: </br>  
<img width="549" height="195" alt="Screenshot From 2026-07-21 12-20-43" src="https://github.com/user-attachments/assets/9a76328d-4090-4693-b954-c5d9d2421aa4" /> </br>  
<img width="540" height="332" alt="Screenshot From 2026-07-21 12-24-28" src="https://github.com/user-attachments/assets/564127bd-d66d-429f-8ee4-2a37cb6214db" /> </br>  
Hence, **Octal method** requires that one not only be adept in permission values but also mentioning the entire permissions. </br>  
In the following image, I have added EXECUTE(1) permission to **Other**, removed WRITE(4) permission to **User Owner**, and set "only" WRITE and EXECUTE(2+1) permissions to **Group Owner**. </br>  
<img width="537" height="217" alt="Screenshot From 2026-07-21 12-32-06" src="https://github.com/user-attachments/assets/f3be1530-2e44-4e70-bcf6-6fa7e9a2b540" /> </br>  


