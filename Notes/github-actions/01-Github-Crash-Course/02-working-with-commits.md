# Working With Commits
Once meaningful changes have been made to your code/file, you create a new _snapshot_ called a **commit**.

Commits are a two step process:
1. Run `git add <file>`, AKA _staging_.
    * Check [branch status](#checking-branch-status)
2. Run `git commit` to create the snapshot. 

To add multiple files:

* Run `git add <file> <file2> <file3>`, separating each with white space. 
* Run `git add subfolder/`.

> It is useful to [use a .gitignore file](#ignoring-files) to ignore system generated files not necessary to deployment. 

To commit files:

* Run ` git commit -m "Some status"`. 

The above command creates a commit, and provides a brief descriptive message explaining why the commit was necessary. 

Alternatively, use VIM to edit your commit message. 
### Using VIM
To use VIM to edit a commit message:

* Run `git commit` The VIM editor opens.
* Type your commit message into the editor. 
    * VIM has [some support for markdown](https://vim.works/2019/03/16/using-markdown-in-vim/).
* Press the ESCAPE key, followed by `:wq` to save the commit message and exit VIM. 

> Generally, commit messages are short and direct. Consider instead updating a README file for longer patch notes and changelogs. 

### Checking Branch Status
The status of a branch tells you which files are ready to be committed, and which are untracked. 

To check branch status:

* In the terminal, type `git status`.
    * Items listed in green are changes to be committed. 
    * Items listed in red are untracked files.
    * `HEAD -> BRANCH` points to a branch, like `HEAD -> main`
### Finding Previous Commits
To retrieve a list of all previous commits, use `git log`.

> Warning!
>
> `git log` always lists all commits that are older than the commit that is currently checked out.
## Moving Between Commits
Temporarily loads another state of the commit/snapshot. 

Essentially, git is moving a pointer from one commit to another while hiding other versions.

To return to a specific commit/snapshot:
1. In your terminal, from the folder that contains your project, run [`git log`](#finding-previous-commits) to list all previous commits.
2. From the listed commits over time, locate the commit by its ID and commit description.
3. Highlight and copy the commit ID assigned to the commit to be retrieved.
4. Run `git checkout COMMIT####` 
5. Check that your document has changed to reflect the desired commit/snapshot.  
## Reverting Changes
`git revert` reverts the changes made to a branch to an earlier commit. This revert action also creates a new commit. 

Effectively, `git revert` is a "safe" way to undo commits by their commit ID, and return to a state prior to making those changes. However, be aware:
* `git revert` is a new commit. Even though it can revert changes, the current branch may be considered "ahead" of other branches used for comparison. 
* `git revert` reverts the commit ID, and moves the branch to the previous snapshot.

To revert changes made in a previous commit:
1. In your terminal, from the folder that contains your project, run [`git log`](#finding-previous-commits) to list all previous commits.
2. From the listed commits over time, locate the commit by its ID and commit description.
3. Highlight and copy the commit ID assigned to the commit to be retrieved.
4. Run `git revert COMMIT#####` and press the ENTER key. [An editor is opened](#using-vim). 
5. Type a commit message and exit VIM. 
<!-- Good luck -->
## Using Git Reset
Git revert keeps history clean and is preferred for reverting changes in most cases.

`git reset --hard <id>` undoes changes by deleting all commits that have occurred since the commit ID specified.

Care is required using this command for 2 reasons:
1. Changes made after the commit cannot be recovered.
2. History is rewritten. 
## Ignoring Files
`git add` doesn't scale with large projects, which often contain files that are not necessary for testing or deployment. Create a `.gitignore` file in your project's main directory to overcome this issue. 

The `.gitignore` file contains a list of files/folders that should not be staged when a commit is made. Once a file is created, and specific files/folders designated, `git add .`, `git add directory/`, or `git add *` will add all files except for those specified in `.gitignore`. 

List each folder/file, one file/folder name per line. 