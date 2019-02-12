## Establishing a Repository from IntelliJ and GitHub 

1.  Open the project file in IntelliJ:  File->open-> (select project)

2.  Establish Git settings against the project:  File->Settings

3.  Ignored Files:  Take the "out" directory off the ignore list (let it be committed as it will be needed).

4.  Add the .idea directory to the ignored files

5.  Add .iml files to the ignored file list

6.  Commit the files:  VCS->Commit

7.  Select all "unversioned" files

8.  Unclick Perform code analysis

9.  Add a commit message

10.  Click commit
   
11.  Set Version Control against the project:  VCS->Import into Version Control->Create Git Repository 
    
Select directory where the new Git repository will be created:  (allow default) 
(e.g.) c:\users\...\ProjectName\src\com\pluralsight\ProjectName
    
12.  Bottom frame will show Git: master as the local branch

13.  Put on GitHub:  VCS->Import into Version Control->Share Project on GitHub (allow default repository name) and (allow default for initial commit)

14.  Confirm repository is on GitHub and add a comment.

15.  Push to Github

## To create a new project from a GitHub repository

1.  Create a new project:  File->New->Project from Version Control->Git

2.  Select the repository

3.  Enter a file name on local drive

4.  Click Clone

5.  Expand the source code directory

6.  Right-mouse click the src directory and click Mark Directory As, and then choose Source

7.  Double click Main

8.  Message will say "SDK not defined" and give you a "setup SDK" link to click

9.  Add the "out" directory to the project structure as the Project compiler output in File->Project Structure





   






