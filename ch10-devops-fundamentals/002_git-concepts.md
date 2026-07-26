# Git Concepts </br>  

### Repository </br>  
This is the place where the source code is stored. A repository can be local in my machine (**Local Repository**) or can be remote (**Remote Repository**) stored in the Cloud. If I am the only person working on the repository or many people in the same location use the same machine to write code, then it makes sense to have a Local Repository. However, if many people spread over different geographical regions are adding code, then a Remote Repository makes sense. GitHub - the tool I am using now is an example of a Remote Repository.

### Working Directory </br>  
This is the directory on my machine where I am creating files, writing code, and editing those files. </br>  

### Staging Area </br>  
This is space for files that have the status set to "staged" and will be part of the next "commit" action. The files in which I have made changes are going to be in this location. As an example, let's say I use Dropbox; I have a word document in my Dropbox (in Cloud) and the same document is also available in my Dropbox directory in my computer. Let's say, at the moment, I don't have the Dropbox App running. The changes I make to the document are stored in my local computer (staging area), but the moment I initiate the Dropbox App, this file (with status staged) is going to be synced to the Cloud (like performing a commit action). </br>  

### File States </br>
1. A file has the status "**Staged**" when the "Staging Area" has a snapshot of the modifications that has been carried out on the file. </br>
2. A file has the status "**Modified**" when the "Staging Area" does NOT have a snapshot of the modifications that has been carried out on the file. This file exists only in the "Working Directory". </br>
3. A file has the status "**Committed**" when the changes made to the file have been saved to the repository. </br>  
