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

## User, Group, Other placeholders: </br>  
<img width="472" height="130" alt="Screenshot From 2026-07-21 11-09-40" src="https://github.com/user-attachments/assets/6fa36da6-4a0b-4a72-a431-ad35f63bdc47" /> </br>  
In the image above, the first placeholder - marked in RED, denotes the **Type of File**. A **Regular File** file, like the one in the image, has a blank for this placeholder. A **Directory** would have **d** at this spot. </br>  
The **Second set** - marked in BLUE - denotes the permissions for the **User Owner** to the resource. This Second set has three placeholders for Read, Write, and Execute. Similarly, the **Third set** - marked in GREEN - denotes the permissions for the **Group Owner** to the resource. The **Fourth set** - marked in YELLOW - denotes the permissions for **Other** to the resource. </br>  
As per the image below, the User Owner, the Group Ownver, and Other have Read, Write, and Execute permissions for the file file1.txt. This can be inferred from the -rwxrwxrwx permissions for the file.</br>  
<img width="472" height="130" alt="Screenshot From 2026-07-21 11-17-57" src="https://github.com/user-attachments/assets/44ebf3c7-8c53-4ccd-b58c-79787af8a99a" /> </br>  

