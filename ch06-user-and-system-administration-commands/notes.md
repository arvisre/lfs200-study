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
<img width="723" height="350" alt="Screenshot From 2026-06-17 17-11-20" src="https://github.com/user-attachments/assets/25ce36f0-ef8e-400f-bd71-fba8140300aa" />



