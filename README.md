### What is Git?
   Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency. Git was created by  ‎Linus Torvalds, the person who designed linux operating system.
## Version Control System
   A version Control system is a system which maintains different versions of your project when we work in a team or as an individual. As the project progresses, new features get added to it. It maintains all your different versions of your project for you and you can rollback to any version you want without causing any trouble for maintaining different versions by giving serial names of your choice.
# Distributed Version Control System:
   Distributed Version control system means every person working on a team project has a local respository of the project in his/her local machine unlike central where team members should have an internet connectionto everytime update their work to main central repository.
# Repository:
   A directory or storage space where your projects can live. You can keep code files, text files, image files, you name it, inside a repository.
1.Local Repository : this is your local repository where you commit changes to the
project before pushing them to central repository on Github. This is what is provided by distributed version control system.
2.Central Repository : This is the main project on the central server, a copy of which
is with every team member as local repository.

### What is a GitHub?
a. Github is designed as a Git repository hosting services.
b. It is completely cloud based. 
c. You can share your code with others, giving them the power to edit.
In short, GitHub is an online service to developers who use Git where they can connect and upload or download resources.

### Commands:
# 1.Initialize directory :
git init 
initializes your directory to work with git and
makes a local repository. .git folder is made
OR
git clone <http_url> 
This is done if we have an existing git repository.

# # change into the `repo` directory/to move to ur repository
cd repo

# 2.Git user configuration (First Step)
git --version (to check git version)
git config --global user.name "your name here"
git config --global user.email "your email here"

# 3.To add a file to central Repository:
git add <filename>
AND
git commit
Does adding and committing in two steps.
OR
git commit -a -m "message for commit"
This command adds and commits the files in single step.
-a : commit all files and for files which have been 
     staged earlier need not to be git add once more
-a options does that automatically.

# 4.
git push origin master -> pushes your files to 
                         github master branch
                         helps keep everything up-to-date.

# 5.
git status -> command to see which files git knows exist.

# 6.To make a new branch while staying on master branch
 git branch -d <filename>
 Helps create new branch.
 AND
 git checkout <branchname>
 This command will automatically help you move to any other branch while staying on a branch.

 # 7.To confirm branch formation
 git branch 
 command helps to confirm that your branch was created.

 # 8.To push the current branch and set the remote as upstream/To push changes to github
 git push --set-upstream origin <filename> 

 # 9.# update all remote tracking branches, and the currently checked out branch
git pull


