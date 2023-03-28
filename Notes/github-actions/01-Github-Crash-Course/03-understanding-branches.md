# Understanding Git Branches
Projects collect commits organized in branches. `main` is the primary branch for any git project and is created automatically when the project is initialized. 
## List Git Branches
In your terminal, from the folder that contains your project, run `git branch`. 

A list of all available branches will appear. The branch that is colored and has an asterisk (*) next to it is the current working branch.  
## Creating Branches
When creating branches, run the command `git branch <branch name>`.

> **Tip**
>
>Use `git checkout -b <branch name>` to simultaneously create a branch and switch to it. 

A new branch is created with the current commit as the starting point. 
## Merging Branches
When work on a branch is complete, merge it into `main` with `git merge <branch name>`.
## Moving Between Branches
Run `git checkout <branch name>` to switch between working branches. 
## Delete Branches
Run `git branch -D <branch name>` to delete branches.
## Merging Branches
Working between branches means managing changes between them. Usually, merging these changes is preferred as the end result includes only what was changed from both branches. 

To merge a branch with main:
1. Run `git checkout main` to switch to the main branch. 
2. Run `git merge <branch name>`
3. If conflicts were resolved, a commit messages is required. 

Git will attempt to resolve any conflicts it might encounter. 
## Using Git Pull and Git Fetch
`git pull` applies the code from a remote repository to your local repository. Precisely speaking: 
1. `git pull` runs `git fetch`
2. `git pull` then runs either `git rebase` or `git merge` to reconcile branches. 

`git fetch` fetches branches and/or tags along with objects necessary to complete their history. Fetch can be considered a "safer alternative" to `git pull` because it does not also perform a merge or rebase. 