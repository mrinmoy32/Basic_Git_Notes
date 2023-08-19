## Basic-Git-Notes

--> Mrinmoy Pal 22 March 2023 at 11:29

Following is the easy commands series to start with --

git init
git add .
git commit -m "first commit"
git remote add origin https://github.com/mrinmoy32/mongoDB_command_notes.git
git remote -v (to check remote)
git push origin master (or git push --set-upstream origin master)

---

--> Mrinmoy Pal 10 June 2023 at 03:10

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


Mrinmoy Pal 10 June 2023 at 03:32
***IMPORTANT- To revert committed changes for a single file: git checkout [commit ID]~1 -- path/to/file

e.g. git checkout 85d42de~1 -- src\shared\components\UIElement\Card.js

---

## Comparison between "Squash and Merge" and "Rebase and Merge" in Git:

| Aspect               | Squash and Merge                                   | Rebase and Merge                                    |
|----------------------|----------------------------------------------------|-----------------------------------------------------|
| Workflow             | Commits are squashed into a single commit.         | Commits are rebased onto the target branch.        |
| Commit History       | Creates a linear history with a single commit.     | Creates a linear history with rebased commits.     |
| Commit Messages      | Individual commit messages are retained.          | Individual commit messages are retained.          |
| Changes Preservation | Original commit history is lost.                  | Original commit history is preserved.             |
| Committer Information| Commits retain their original authors and timestamps.| Commits retain their original authors and timestamps.|
| Conflict Resolution | Conflict resolution occurs during merge.          | Conflict resolution can occur during rebase.      |
| Remote Repository    | May require force-pushing to remote repository.    | May require force-pushing to remote repository.   |
| Collaboration        | May lead to cleaner commit history for collaborators.| May lead to more accurate history with rebased commits.|
| Use Cases            | Suitable for feature branches or pull requests with many small commits.| Useful for feature branches where commits need to be rebased and updated.|
| Complexity           | Simpler process, especially for newcomers.        | Involves more complex interactions and conflicts handling.|
