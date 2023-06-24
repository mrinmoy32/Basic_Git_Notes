# Basic-Git-Notes

--> Mrinmoy Pal22 March 2023 at 11:29

Following is the easy commands series to start with --

git init
git add .
git commit -m "first commit"
git remote add origin https://github.com/mrinmoy32/mongoDB_command_notes.git
git remote -v (to check remote)
git push origin master (or git push --set-upstream origin master)


--> Mrinmoy Pal10 June 2023 at 03:10

If the remote repo lets say: https://github.com/mrinmoy32/mongoDB_command_notes.git has been already created with Readme.md or has some initial commit then that might cause tacking issue and pushing will not be successful.

To avoid this we can do--

1. Either: create a repo without any readme or noting and no initial commit, then we can easily follow the steps and push :
git init -b main
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/mrinmoy32/mongoDB_command_notes.git
git push origin main

2. Or: Create a repo that can have Readme or any initial commits then we can clone this repo in our local machine and then start coding to avoid any tracking or mismatch issue.


Mrinmoy Pal10 June 2023 at 03:32
***IMPORTANT- To revert committed changes for a single file: git checkout [commit ID]~1 -- path/to/file

e.g. git checkout 85d42de~1 -- src\shared\components\UIElement\Card.js