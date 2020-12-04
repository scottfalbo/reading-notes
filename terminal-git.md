# Terminal and Git Commands

## Terminal Basics
+ `pwd` - print working directory
+ `cd directory` - change directory
+ `cd ..` - go back a directory
+ `ls` - see the contents of current directory
  + `ls -a` - to see hidden files
+ `mkdir name` - create new folder(s)
  + `rmdir` - removes an empty directory
+ `touch fileName.md` - creates new file(s)
+ `rm file.md` - removes a file
  `rm -r folderName` - recursively removes folder and everything inside of it.
  + `rm -rf folder` remove and override (`-f` - force) any overwrites. 
    + *be 100% sure before forcing things*
+ `cp` copy a file
  + `cp <file to copy> <new copy name>`
    + You can move files from one directory to another like this.
    + `cp folder/directory/file.md folder/otherDirectory/file.md`
    + You can copy files from any where to your current working directory by using a `.` as the destination.
    + `cp folder/directory/someFile.md .`
  + If you are copying an entire folder you need to do it recursively to copy all of it's contents.
    + `cp -r directory/folderOfThings .` - Will copy the entire contents of the folderOfThings to the current working directory.
+ `mv folder/file.md newFolder`
  + `mv file.md newFile.md` - will rename a file in place
+ `clear` - clear the terminal window
+ `help`- terminal help, including commands

    

## Git Commands
+ Set up things
  + `git config --global user.name "Spaceghost"`
  + `git config --global user.email Handsome@loaf.com`
+ `git clone url` - clone down a repo
+ `git status` - lists files that have been changed but not committed
+ `git pull origin branchName` - fetch and merge changes from remote to local
+ **ACP**
  + `git add file.md file2.md` -  add files to be committed
    + `git add .` - add all files to commit
  + `git commit -m "message"` - commit files to be pushed
  + `git push origin branchName` push to gitHub
    + `git push` - defaults to main
+ `git restore file.md` - restore to last commit
+ **Branches**
  + `git branch` - list all branches
  + `git checkout branchName` - switch to a new branch
  + `git checkout -b name` - create and checkout a new branch
  + `git branch -d branchName` - delete branch
  + `git push --all origin` - push all branches to remote repo
  + `git push origin :branchName` - delete branch on remote repo
+ **Forking and Upstreaming** allows you to make changes in your own version of a repo while still being able to pull changes made to the main repo.
  1. Fork and clone the Repo
  2. From inside the repo directory
    + `git remote add upstream MAIN_REPO_URL`
  3. `git pull upstream main` - to get updates on main repo
+ `git remote remove upstream` - remove upstream
+ **Initializing and pushing a new local repo to gitHub**
  1. Create an empty repo on gitHub
  2. `git init` - initialize the directory
  3. `git add README.md`
  4. `git commit -m "first commit"`
  5. `git branch -M main`
  6. `git remote add origin REPO_URL`
  7. `git push -u origin main`



## Others

### Heroku
+ Replicating a local PG database to Heroku:
  + `heroku pg:psql -f folder/schema.sql --app your-app-name`


### node
+ `npm init` - initialize node
+ `node server.js` - run node server
  + `nodemon` - run server with live refresh
+ `npm install dependencyName` - install dependencies
+ `npm install` - automatically install dependencies `in package.json`


### PG
+ `psql -f folder/schema.sql -d databaseName` - put sql data into local PG database
+ `psql` - enter the pg database
  + `\l` - lists databases
  + `\c databaseName` - move to database
    + `\dt` - list available tables
    + `\d tableName` - describe a table
    + `\dn` - lists available schema
+ SQL commands all work in here as well.

### React
1. `npx create-react-app appName` - this sets up your react development environment 
2. `cd appName`
3. `npm start`



  