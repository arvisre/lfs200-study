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
At the moment, the file **my-code** is in status **Committed**. </br>  
I am going to open the file **my-code** again to enter some more line of text. But, on this occasion, I am NOT going to run the **git add** command. </br>  
<img width="908" height="430" alt="Screenshot From 2026-07-26 11-09-12" src="https://github.com/user-attachments/assets/6f26a8dc-03d1-4fd7-ad27-9348ff708729" /> </br>  
As shown in the image above, I have added some lines of text to the file, but I have not executed the **git add** command to **stage** the file. Instead, I executed the **git status** command and I note that the file is now in **Modified** status. This means that this file is now **ONLY** part of my working directory and a snapshot has not been captured in the **Staging Area**. The suggestions shown in the terminal are the further actions that I can do with the file - whether I want to stage the file or discard the changes. </br>  
By executing the **git add** command, I move the changes to the **Staging Area**. </br>  
I made a mistake in executing the **git add** command. I did NOT specify the file name. This was un-intentional, and git is suggesting further actions based on the error on my part. I then execute the right command **git add my-code** and the results are displayed:  </br>  
<img width="916" height="287" alt="Screenshot From 2026-07-26 11-15-23" src="https://github.com/user-attachments/assets/54bf1983-21c6-4b39-9ffd-b2153c41163e" /> </br>  

## Displaying the log </br>  
I executed the command **git log** hoping to see all the actions that I have taken since creating my first git file. However, it only showed the only **commit** action and its details - the Author, timestamp, and the comment I provided during commit. Hence, I executed the **git commit** command again to commit the changes from the Staging Area to the repository. Now I see details about both the commits, as shown in the image below: </br>  
<img width="901" height="593" alt="Screenshot From 2026-07-26 11-20-12" src="https://github.com/user-attachments/assets/c570ca97-6420-4431-92e2-5b51a0aba7b5" /> </br>  

