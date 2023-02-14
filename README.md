# Basic-git-commands
Here you will get basic git commands with a little explanation...

git config --global user.name Gaurav
git config --global user.email gmaurya783@gmail.com
pwd
ls
ls -a
clear
# Go to project directory and open git bash
git init					## initialize git in project directory
ls -lart					## list hidden files/folder too
git status
## Untracked		## Unmodified		## Modified		## Staged
code .  					## to open visual studio code
touch file.py					## create a file 
git add file.py 				## add file to staging area  # Untracked/Modified --> Staged
git status					## check status of files in project directory
git rm --cached file.py				## use to unstage/untrack file	# Staged/Modified/Unmodified --> Untracked
git restore --staged file.py
git restore <file>          ## to discard changes in working directory
git rm file.py					## use to unstage and remove/delete file completely
git commit					## save the file  # Staged --> Unmodified
#An editor will be opened here write comment on your commit and close the editor
touch about.html
git add -A					## add ALL files & Folders to staging area  # Untracked/Modified --> Staged
git add .
git commit -m "Added more files" 	#GoodWay## save the file  # Staged --> Unmodified
git checkout about.html			## Match the given file from last commit
git checkout -f 			## Match all files of working directory from last commit
git log 				## Shows what we have committed
git log -p -1				## Shows last 1(or n) commits in detail with diffrences made
#type q to quit detailed view
git diff				## compares Working tree with staging area
git diff --staged			## compares staging area with last commit
git commit -a -m "Skipped staging area"	## direct commit without going to staging area # Tracked/Modified --> Commited/Unmodified/Saved
git status				## git status in short


## How to ignore files and folders
touch .gitignore			## Creates a file .gitignore
#In this write the names of files or folder you want to ignore
for eg:-
mylogs.log		#To ignore given file from anywhere in project directory
/mylogs.log		#To ignore given file from directory which contains .gitignore and also excludes subfloders
*.log			#To ignore the files having extension .log from anywhere in project directory
folder/			#To ignore a whole directory
.gitignore 		#To ignore itself		

## How to create branches in git
#In this we create a copy of main project and work on copied version
#when we have made all the changes and tested it we can merge it with master(or main) version of project
#main branch is called master branch
git branch feature1	#Creates new branch
git branch		#Shows all braches
git checkout feature1	#Switch to desired branch
git checkout -b newfeature1	#Creates & switch to new branch
#Changes made in feature1 will not effect master branch
#To merge the changes made in feature1 to our master branch follow this:-
#Go to master branch
git checkout master
git merge feature1



#### GitHub
Open gitHub -> Create a repository -> then you will get a setup code
git remote add origin https://github.com/gmaurya783/trial0.git	#Save the remote link with name origin
git branch -M main
git push -u origin main

git remote				#To check remote link names you have
git remote -v				#To check remote links you have in detail
git remote set-url origin <new link>	#To change the url of origin


#Fork -> copy the repository in your github account
#clone -> copy repo in your system with help of git
git clone <https link>
