# Collaborating in Git
Permissions are one of a number of safeguards that prevent users from pushing any changes directly to a repository's `main` branch. In general, it's best practice to `git pull` from the main branch, create a fork or a new branch, make changes, then create a `git pull` request and tag another user for further review. 

Github uses `pull` requests (PRs) and code reviews to solve collaboration issues. 
## Using Issues
The issues tab allows users to reach out to creators and inform them of issues, changes, bug reports, etc. 

To access the Issues tab:
1. From any Github repository, click the **Issues** tab. The page changes to the Issues page. 
2. At the right side of the **Issues** page, click the green **New Issue** button.
3. In the Title field, enter a title for the issue. 
4. In the Comment field, enter details about the issue. 
    * Include code or markdown samples as appropriate. 
    * Describe the steps to reproduce the issue when filing a bug report. 
5. At the bottom right of the New Issues screen, click the green **Submit new issue** button. 
## Using Pull Requests
Pull requests are the typical way to merge projects into a `main` branch for deployment. 

To create a pull request, visit the Github.com repository. 
1. At the top of the repository within a working branch, click **Contribute**. A dropdown menu opens.  
2. From the dropdown menu, select **Open pull request**. 
3. In the Title field, enter a title for the issue. 
4. In the Comment field, enter details about the pull request.
    * This space can be used for longer descriptions of changes made, with specific callouts to certain sections. 
5. At the right side of the pull request creation field, click the cog wheel next to _Reviewers_. A dropdown opens containing all users who can review the pull request. 
    * Refer to your organization chart for guidance on who to tag for reviews. 
    * Up to 15 reviewers are possible. 
5. At the bottom right of the pull request creation field, click **Create pull request** to create the pull request. 

An Assignee can also be tagged if there is a designated person working on a specific issue or related pull request. 
## Using Forks
Forks allow collaboration in a safer manner. Users can fork a repository to work independent of one another. 

A fork is a clone of the repository on github. It creates a clone on github, where changes can be made and pushed without affecting the original repository. 

> Note
>
> Origin URL should be set to the origin of the forked repository. 


