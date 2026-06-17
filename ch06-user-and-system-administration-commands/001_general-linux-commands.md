# Topic 1: General Linux Commands: </br>  
This chapter had a table titled "General Linux commands" - **cat, cd, find, grep, info ls, man, pwd** along with some with some command options. </br>  
Interestingly, I have not used the **-xdev** option with the **find** command and the **-l** option with the **grep** command. </br>  

## grep -l (arguments) or grep -l -R (directory) </br>  
The command **grep** with the option **-l** prints the name of the file(s) in which the specific pattern we are searching for is found. </br>  
As an example, I have created 5 text files - file1.txt - file5.txt. Some of these files have the pattern "as" in them.  
These files reside in the directory /home/as/test. </br>  
As shown in the image below: </br>  
### grep -l can be used to search a "pattern" in a list of files provided as argument. </br>  
### grep -l can be used to search a "pattern" in all the file within the current directory. </br>  
### grep -l can be used to search a "pattern" in all the files within the current directory and all its sub-directories, recursilvely, by including the option -R. </br>  
<img width="723" height="350" alt="Screenshot From 2026-06-17 17-11-20" src="https://github.com/user-attachments/assets/25ce36f0-ef8e-400f-bd71-fba8140300aa" /> </br>  


## find -xdev </br>  
The **man** page definition of the **-xdev** option is "Don't descend directories on other filesystems." </br>  
In my Fedora Linux host computer, the **/** and the **/home** directories reside on separate disk partitions and filesystems. This can be confirmed by the image below </br>  
<img width="914" height="502" alt="Screenshot From 2026-06-17 17-34-50" src="https://github.com/user-attachments/assets/b4486cfb-d79a-41e7-8c0e-e905b9476994" /> </br>  
I have created a file "findtest.txt" at the **/** directory and at **/home/as**. The following image shows the use of the **-xdev** option. </br>  
<img width="723" height="213" alt="Screenshot From 2026-06-17 17-39-56" src="https://github.com/user-attachments/assets/fd6d51ee-1112-4105-8732-c9c6484e4962" /> </br>  
Without the **-xdev** option find traverses through the **/home** directory even though it is a different filesystem. With the **-xdev** option **find** limits itself to **/**.  







