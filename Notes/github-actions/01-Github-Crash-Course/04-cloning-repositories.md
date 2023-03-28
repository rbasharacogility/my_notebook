# Using Git Clone
To improve a remote repository, it is important to download the files/code to begin work. It is possible to download as a ZIP file, but easier and faster to clone the repository. 
## Cloning Repositories
`git clone` can be run to download a remote repository, and automatically connect the local version to the remote repository. 

To clone a repository:
1. From Github, locate the repository to be cloned. 
2. At the top right of the repository, click the green **Code** button. A small modal opens containing several tabs. 
3. Copy the URL provided under the HTTP(S) tab. 
4. From the terminal, run `git clone <repository URL>`, pasting the repository URL received into the command. 
    * Optionally, enter a name for the local folder as follows: `git clone <repository URL> folder-name`
### Checking Cloned Repository Status
To confirm the clone is properly setup, use `git remote`. `git remote` is used to manage repositories tracked on a machine. 

Use `get remote get-url origin` to retrieve the URL of the original repository the cloned directory came from.  
## Pushing to a Remote Repository
To push to a remote repository, users must have proper access. Typically, users should incorporate some [best practices for github collaboration](./05-collaborating-in-git.md). 

To push to a remote repository:
1. Run `git remote set-url origin <yourgithubusername@github.com/repositoryname>`
2. Run `git push origin <branch-name>` to push the branch to the remote repository. 
3. A password for the currently logged in user is requested. Type the user's personal access token into the terminal, or into the editor as requested. 
4. The terminal informs the user of failure or success, with details.

