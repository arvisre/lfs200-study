# Demonstration of basic Git Concepts </br>  
I am going to demonstrate some basic Git Concepts with commands. Git is available in Rocky Linux 10.2, by default. </br>  
<img width="833" height="785" alt="Screenshot From 2026-07-26 10-08-22" src="https://github.com/user-attachments/assets/79a5919e-f85f-43a3-8dfd-c727f4417bcc" /> </br>  

## Configuring Git Global Settings </br>  
The following basic Global Configuration settings have been applied: </br>  
<img width="1027" height="129" alt="Screenshot From 2026-07-26 10-14-58" src="https://github.com/user-attachments/assets/9adc2bf3-044c-4517-93b3-c148ab4ec036" /> </br>  

## Creating a Working Directory </br>  
I have created a working directory named "test-app" under my home directory and will "**initialise**" this directory with git. </br>  
<img width="1447" height="885" alt="Screenshot From 2026-07-26 10-28-20" src="https://github.com/user-attachments/assets/11589bb1-63fb-4068-b300-ea6a6fa2703a" />

## Basic Git Commands </br>  
In this demo, I will use the basic Git commands - "*git status*", "*git add*", "*git commit*", and "*git log*". </br>  
I will be creating a simple text file called "**my-code**" in the working directory, execute git commands, and perform the staging and commit functions. </br>  
I ran the "**git status**" command even before I create any files in my working directory. Then create a file using the "nano" text editor. </br>  
<img width="696" height="192" alt="Screenshot From 2026-07-26 10-38-49" src="https://github.com/user-attachments/assets/83f2cd11-48c0-4164-9a35-7212c4262ecf" /> </br>  
Using the "nano" text editor, I input some lines in "**my-code**" file and then executed the "**git add**" command for the first time. </br>  
Then, to view the current status of my work, I executed the "**git status**" command to check my work. </br>  
<img width="899" height="506" alt="Screenshot From 2026-07-26 10-42-43" src="https://github.com/user-attachments/assets/86d2fe4b-2b57-4758-81ad-94ed0913938f" /> </br>  
As displayed in the image above, because I executed the **git add** command, the snapshot of the file "**my-code**" is now in the "**Staging Area**" and yet to be committed. Hence, at this moment the file "**my-code**" is in "**Staged**" status. </br>  
As the next step, I am going to execute the command **git commit** to save the file to the local repository. </br>  
As soon an I executed the **git commit** command, a new window opened with the following self-explanatory message: </br>  
<img width="899" height="506" alt="Screenshot From 2026-07-26 10-51-48" src="https://github.com/user-attachments/assets/69e535ea-b8cd-4494-8aa3-950190b88a05" /> </br>  
This is a **text editor** window and it is opened with the **VI**/**VIM** text editor. Since I knew the very basic commands in **VIM**, I pressed the alphabet **i** to enter the **INSERT MODE**. One can enter text when the editor is in **INSERT MODE**. </br>  
I entered the text "first commit to the file my-code" (for lack of a better comment). Then pressed the "**ESC**" key to go back the **COMMAND MODE** in the VIM editor. </br>  
Then to save the changes (the comment I just entered), I pressed the **:** colon symbol followed by the alphabets **wq** for "write changes and quit file". This action **committed the changes** </br>  
Executing the command **git status** shows the current status of the file. </br>  
<img width="786" height="416" alt="Screenshot From 2026-07-26 10-53-37" src="https://github.com/user-attachments/assets/bc98c3c2-5dc5-4f73-be70-9e67ca15532a" /> </br>  
