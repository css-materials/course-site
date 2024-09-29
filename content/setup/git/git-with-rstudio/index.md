---
date: "2024-09-29T00:00:00-05:00"
draft: false
weight: 50
title: "Using Git within RStudio"
toc: true
type: book
aliases: ["/git05.html", "/setup/git-with-rstudio/"]
---



Complete the workflow below to verify that everything works as expected. Please, complete do this only **AFTER** you have:

* [Installed Git](/setup/git/git/) (this should be completed only if you are working with R/RStudio locally), and
* [Configured Git](/setup/git/git-configure/) (this must be completed for both local and Workbench options)

If you are not sure, begin by reading [START HERE: Software Options](/setup/).


## Step 1: Make sure RStudio can find Git

Log in to [RStudio Workbench](https://macss-r.uchicago.edu/) using your UChicago credentials. Then try the following:

* *File > New Project*. Do you see a *Version Control* option? If yes, that's good but do not select it. Instead, select *New Directory > New Project*
* Do you see a check box that says *Create a git repository*? If yes, that's good and check it.
* Under *Directory name:* give this test directory a name (e.g. test), then check the *Open in new session* box, and finally press the *Create Project* button 
* A new project should open up. Look in the upper right panel: do you see a "Git" tab next to "Environment", "History", etc.? If yes, good

**If this worked:** 
* You've set everything up correctly! Notice, if you are working on R Workbench this should automatically work 
* Now delete the project. Look in the lower right panel: you should see a "Files" tab; in that tab you should see your newly created project, go to Home, click on the project folder, then click "Delete" and close the project
* Move to step 2

**If this didn't work:** 
* It might be that Git is not installed and/or R cannot find it. A basic test for successful installation of Git is to open the Shell (Tools > Shell) and simply type `git`. If you get a complaint about `git` not being found, it means installation was unsuccessful or that it is not being found, i.e. it is not on your `PATH`
  * Try typing this in the Shell `which git` (Mac, Linux) or `where git` (most versions of Windows). If Git appears to be installed and findable, launch RStudio and try again. If it still doesn't work, quit and re-launch RStudio if there's any doubt in your mind about whether you opened RStudio before or after installing Git
  * From RStudio, go to *Tools > Global Options > Git/SVN* and make sure that the box *Git executable* points to the Git executable. It should read something like: `/usr/bin/git` (Mac, Linux) or `C:/Program Files (x86)/Git/bin/git.exe` (Windows). If you make any changes, *restart RStudio and try the steps at the top of the page again*
* If these steps worked, delete the project (see above) and move to step 2. Still not working? Try googling your problem or speak with the instructor or the TAs
  
<!--
On my computer, it looks like this:
{{< figure src="git_exec.png" caption="" >}}
-->


## Step 2: Make a new repository on GitHub

* Go to [GitHub.com](https://www.github.com) and log in. If you haven't yet, sign up, create your account and share your GitHub username with us (see Lecture 1 for details)
* Click the green "New" or New Repository" button
    * Repository name: `myrepo`
    * Set it as Public
    * Add a README file
    * No need to add a .gitignore for now, nor a license 
    * Click the green "Create repository" button
* Find and click on the green "Code" button. You should see tabs with an HTTPS or SSH url. Recall the authentication method you used when you [configured Git](/setup/git-configure/) and copy the correct url to your clipboard. If you haven't configured Git yet, do that first. If you configured Git with:
    * HTTPS: use `https://github.com/<OWNER>/<REPO>.git`
    * SSH: use `git@github.com:<OWNER>/<REPO>.git` (for R Workbench users)


## Step 3: Clone the new GitHub repository to your computer via RStudio

{{% callout note %}}

Whenever possible, the workshop described below (Github first, then Git in RStudio workflow) should be your preferred route for setting up your R projects.

{{% /callout %}}


In RStudio (on your local computer or on R Workbench), start a new Git Project: *File > New Project > Version Control > Git* 

If you do you NOT see an option to get the Project from Version Control, go back to Step 1 and make sure RStudio can find Git. 

Fill out the following fields:

* *Repository URL:* paste the URL of your new GitHub repository (Step 2)

* *Project directory name:* it should automatically populate, do not change it (if it does not automatically populate, type the same name you gave to your GitHub repository)

* *Create project as subdirectory of:* click on "Browse..." and decide where to store the local directory for the project. It is OK to leave this test directory under the Home, but for other repos try to keep things organized using some meaningful structure; for example, you can setup a `css`  folder (or give it any other name) and clone all your repos there

* Before proceeding, check the *Open in new session* box, as that's what you'll usually do in real life

* Finally, click *Create Project.* The first time you do it, you might get the following message "The authenticity of host 'github.com (IP)' can't be established etc." If so:
  * Ensure that the hash shown in the message (the long string of numbers and letters) matches one of those shown [here](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/githubs-ssh-key-fingerprints)
  * If the hash matches, then connection is indeed safe and you can type "yes" to the question asked. If you do not see the hash in the message, open the shell/terminal and type 
`ssh -T git@github.com` to visualize it. 
* If you answered "yes" and get a message that says "Permission denied. fatal: Could not read from remote repository" it likely means you have not configured Git correctly, go back and do it

* Your Project has been created! You’ll notice that your project in RStudio (or R Workbench) matches the one on GitHub. A Project" will be all of these things:
    * a directory on your computer
    * a Git repository, linked to a remote GitHub repository
    * an RStudio Project

Why set up your R projects in this specific order? The benefit of the "GitHub first, then Git in RStudio" workflow is that your remote GitHub repository is already set as the "upstream" remote for your local repository. This means you're immediately ready to push and pull commits to GitHub without any additional setup in the shell or a Git client. However, you can also start with the Git repository and then connect it to GitHub — see the "Alternative to Step 3" instructions below for more details.


## Step 4: Make local changes, save, commit

{{% callout note %}}

Do this every time you finish a valuable chunk of work, probably many times a day.

{{% /callout %}}

From RStudio or R Workbench, check file browser panel to find the `README.md` file of your project. Open it and modify it by adding the following line (or any other line):
    
```
This is a line written from R.
```

Save your changes. Next, commit these changes to your local repo using RStudio:

* From R Studio, click the "Git" tab in the upper right panel
* In the "Staged" box, select all files whose existence or modifications you want to commit (all of them in this case)
* Click "Commit"
* A new window should open up. In "Commit message" box, enter a descriptive message (this should describe for a human reader what modifications you've made to the staged files, for example in this case you could write something like "Added a test line to README")
* Click "Commit" and wait until done' then click "Close"
    
    
## Step 5: Push your local changes to GitHub

{{% callout note %}}
Do this a few times a day, but less often than you commit.
{{% /callout %}}

Now, you have new work in your local Git repository, but the changes are not on GitHub online yet (e.g., "Your branch is ahead of origin/main by 1 commit.")

If this is your first time pushing to GitHub, you might see a warning about adding your key or be prompted to enter your username and password—go ahead and do so. Once everything is done, close the window. Now, open your GitHub repository online to see the changes you have just pushed!

Notice this whole operation will fail if you have not configured Git and/or you have not used the correct authentication method (SSH or HTTPS): see [Configure Git](/setup/git/git-configure) and repeat.

**Important:** Before you *push* your changes to GitHub, first you should *pull* from GitHub. Why? If you make changes to the online GitHub repo in the browser (not recommended!) or one day a collaborator has pushed some new code to your repo, you need to pull those changes in before you attempt to push your own.
To pull: click the blue "Pull" arrow in the "Git" tab in RStudio. In most cases, nothing will happen and you see the "Already up-to-date" message, but this practice helps establish a good habit!


## The end: repeat and delete the test repo

Now, simply repeat the process: make changes, commit them, and push or pull as needed to keep your local (Git) and remote (GitHub) repositories in sync.

Since this was just a test, there's no need to keep the `myrepo` repository. Remember to delete it from both your computer (or R Workbench) and GitHub, as it's stored in both locations:

* Delete the local repository: find where you stored it on your computer (or R Workbench) and delete it

* Delete the repository from GitHub: in the browser that shows your repository on GitHub, click on "Settings", then scroll down until the end, click on "Delete this repository", and follow the instructions

<!--
* Delete the local repository in the shell:


```bash
cd ..
rm -rf myrepo/
```
-->

## Acknowledgments


* This page is derived in part from ["UBC STAT 545A and 547M"](http://stat545.com), licensed under the [CC BY-NC 3.0 Creative Commons License](https://creativecommons.org/licenses/by-nc/3.0/).

* This page has been developed starting from Benjamin Soltoff’s “Computing for the Social Sciences” course materials, licensed under the CC BY-NC 4.0 Creative Commons License.
________________________________________________________________________________

## Alternative to Step 3

Remember, Step 3 above should be your preferred route. However, sometimes you cannot always setup the GitHub repo first, or you already have an RStudio project you need to connect to a GitHub repo. This workflow is the reverse of the above and allows to connect a local RStudio project to a GitHub repository. This cannot be executed entirely from within RStudio (you will need to use the Shell or Terminal).

In R Studio, start a new RStudio project: *File > New Project > New Directory > Empty Project*:
* Directory name: `myrepo` (or whatever you named the GitHub repo)
* Decide where to store the local directory for the Project.
* Yes, check "Create a git repository". If you do you NOT see an option to get the Project from Version Control, go back to Step 1 and make sure RStudio can find Git. 
* Check the "Open in new session" box, as that's what you'll usually do in real life.
* Click "Create Project" to create a new sub-directory, which will be all of these things:
  * a directory on your computer
  * a Git repository  --linked to a remote GitHub repository-- in this case this isn't automatic: we still need to link it up
  * an RStudio Project
        
Now, you need to initiate the "upstream" or "tracking" relationship by adding a remote. In RStudio, go to *Tools > Shell* and do this, substituting the example URL for your GitHub repo (use the line for HTTPS or SSH, not both):
* HTTPS 
        ```bash
        git remote add origin https://github.com/brinsab/myrepo.git
        ```
* (or) SSH
        ```bash
        git remote add origin git@github.com:brinasab/myrepo.git
        ```
* Download all the files from the online GitHub repository (possibly just README.md, at this point)
    ```bash
    git pull origin main
    ```
* Cement the tracking relationship between your GitHub repository and the local repo by pushing and setting the "upstream" remote:
    ```bash
    git push -u origin main
    ```
