---
title: "HW01: Practice editing .md and .Rmd"
date: 2023-10-02T13:30:00-06:00 
type: book
toc: true
draft: false
aliases: ["/hw01-edit-README.html"]
categories: []
weight: 10
---

<!--
title: "HW01: Practice editing .md and .Rmd"
date: 2022-10-02T13:30:00-06:00  # Schedule page publish date
#publishdate: 2019-03-01
draft: false
#type: post
aliases: ["/hw01-edit-README.html"]

summary: "Test software installation, GitHub setup, and homework submission process, as well as demonstrate basic competency in Markdown and R Markdown."
-->



# Overview

**Due Monday, October 9th (11:59 PM).**

The goals of this first homework assignment are multiple (1) to test your software installation, your GitHub setup, and the homework submission process, and (2) to demonstrate competency in basic R syntax, Markdown, and R Markdown. I strongly encourage you to start this assignment early, so there is time to fix problems if they might arise. 


# Accessing your `hw01` repository

{{% callout note %}}
This will work only if you have provided us your GitHub username (see survey in lecture 1) and have accepted the email invitation to join our organization.
{{% /callout %}}

* Go [at this link](https://classroom.github.com/a/VnCIbRdK) to accept and create your private `hw01` repository on GitHub. Once you do so, your repository will be built in a few seconds. It follows the naming convention `hw01-<USERNAME>`  
* Once the your repository has been created, click on the link you see, which will take you to your repository. 
* Finally, clone the repository to your R Workbench (or your computer if you have installed R there) following the process below.


# Cloning your `hw01` repository

{{% callout note %}}
Before completing this part, ensure you followed the configuration steps [here](/setup/git-configure/), and everything works as expected.
{{% /callout %}}

After you have accessed the `hw01` repository (see above), follow these steps to clone it:

* In RStudio or RStudio Workbench, start a new Project with *File > New Project > Version Control > Git*. In the "repository URL" paste the URL of your newly created GitHub repository: go back to the repository, click on the green button "Code" and grab the correct link, either SSH or HTTPS (the one you used to set up your cache credentials, if you are using R Workbench this must be SSH). The repository name should automatically populate; if not, type your `hw01-<USERNAME>` as name. 
* Decide where to store the local directory for the project. Don't scatter everything around your computer - have a central location, or some meaningful structure. For example, for repositories you create in this course, you can setup a `css` directory and clone all your repos there.
* Before proceeding, check the little box "Open in new session", as that's what you'll usually do in real life.
* Click "Create Project" to create a new sub-directory, which will be all of these things:
    * a directory on your computer
    * a Git repository, linked to a remote GitHub repository
    * an RStudio Project

This will always be our homework assignments workflow. Whenever possible, I recommend using this workflow also for setting up your R projects, but other options are possible. See [Using Git with R Studio](/setup/git/git-with-rstudio) for more info.


# General workflow

Your general workflow for all homework assignments will be:

* Accept the repo and clone it (see above)
* Make changes locally to the files (for this assignment: `README.md` and `Rcode.rmd`) in RStudio
* Save your changes locally
* Pull-Stage-Commit-Push: 
  * Pull from GitHub (nothing should happen since if you work alone you should always modify the local Git repo first; but it's a good habit to pull as first step, since pulling will matter a great deal when you collaborate with others)
  * Stage and Commit your changes to your local Git repo
  * Push them online to GitHub

For this course, I assume you will complete these steps using the Git GUI integrated into RStudio. If you have not yet, I strongly recommend to go through the [Using Git with R Studio](/setup/git/git-with-rstudio) tutorial to get comfortable with the workflow.

Tip: do not directly modify your online GitHub repo; instead modify your local Git repo, then stage-commit-push your changes up to your online GitHub repo.


# Assigment descripion

All assignments for this course will be submitted using Markdown and R Markdown:
* [Markdown](https://daringfireball.net/projects/markdown/) (.md) is a lightweight and basic language for formatting text. It easily converts between file formats. For example, GitHub README files are frequently written in Markdown (that is they have an .md extension) or as plain text (with a .txt extension). Markdown files are directly rendered on the GitHub website (vs. R Markdown files which are not), and they are also well integrated into R Markdown. GitHub includes a [guide](https://guides.github.com/features/mastering-markdown/) for writing Markdown documents. You can embed R code in plain Markdown, but to execute it inside your document together with written text you need to use R Markdown.
* [R Markdown](https://rmarkdown.rstudio.com/) (.rmd or .Rmd) is a fancy version of Markdown, designed for R. It combines R code, output, and written text into a single document. We will use R Markdown files for homework assignments. 

For this assignment, you need to modify and push to your GitHub homework repository the following two files: `README.md` and `Rcode.rmd`


## `README.md` 

You will notice there is already a `README.md` file in the repo. A README is usually a plain .txt or .md file. The purpose of a README file in a repository is to communicate important information about your project to yourself and others (things like required software, how to run the code, preview of the results, etc.). The goal of this assignment is to practice generating and editing a README file.

Your task is to edit this file by replacing what is in there (instructions) with a brief biography of yourself. To achieve full marks, your biography should include the following elements:

* Headers (one or more)
* Emphasis (italics or/and bold)
* At least one list
* Images: add a picture (of yourself or something else) to your repo and embed it in your README
* At least one link
* A descriptive summary of the Git/GitHub workflow you adopted for this homework (either bullet points or full narrative, as long as the description is detailed)
* An evaluation of your experience with this homework (e.g., something new you learned, something that surprised you, etc.); these reflections will be a requirement for every homework and they should always be placed in the README file

## `Rcode.rmd`

You will notice there is already a `Rcode.rmd` file in the repo. Your task is to edit this file by adding more YAML arguments and at least two R code chunks with text explanations. To achieve full marks, your `Rcode.rmd` should include the following elements:

* At least two new YAML Header arguments. Do not modify those that are already there, simply add at least two new ones (e.g., author, subtitle, table of contents, etc. -- see readings for more)
* At least two R code chunks:
  * You are welcome to rely on the in-class materials as starting point, but do not copy the exact same code: make changes to customize or expand it; your code does not need to be complex, but should be more elaborated than assigning a value to a variable
  * All code chunks must execute correctly and your final knitted document (which you should submit as well as .md file) must display both the code and the results
  * Before each code chunk, add a brief text that explains what each code chunk does; these explanations should be a text, not a code comment


# Submit the assignment

To submit the assignment, follow these steps:
* First push to your repository the last version of your assignment before the deadline. You GitHub repository should contain: the modified `README.md` and `Rcode.rmd`, plus the final knitted document that you generated starting from the `Rcode.rmd`(this document should be a .md file)
* When you are ready to submit, copy your repository URL (e.g. https://github.com/css-fall23/hw1-brinasab) and submit it to Canvas under HW01 before the deadline. Do not submit files on Canvas, we only need the link to your repository 


# Assessment

All homework assignments are evaluated using [this general rubric](/faq/homework-evaluations/). 

Below are further guidelines for this specific homework to help you assess your work before submitting it.

*Needs improvement:* `README.md` says the equivalent of "This is the repository of Name Surname" with little details and/or not all requirements are met. `Rcode.rmd` contains R code chunks, but no explanation nor additional YAML headers are added. Code is too minimal, insufficient, or copied-pasted from the class materials. The final knitted document has not been submitted or does not work. All work done via Git/Github ... but that's a guess, because there is no clear explanation of how it was done.

*Good:* Something in between.

*Excellent:* `README.md` provides a proper introduction of the student. It also demonstrates experimentation with several aspects of the Markdown syntax (e.g., section headers, links, bold, italic, bullet points, image, etc.) and all requirements are met. The student provides a detailed description on how they got the changes into `README.md` and offers a few reflections on their Git/GitHub workflow and their experience with Markdown. `Rcode.rmd` knits properly and contains one or more new YAML headers. It also includes novel R code chunks with a detailed explanation of them. All required files have been submitted.


# Acknowledgments


* This page is derived in part from ["UBC STAT 545A and 547M"](http://stat545.com), licensed under the [CC BY-NC 3.0 Creative Commons License](https://creativecommons.org/licenses/by-nc/3.0/).

* This page has been developed starting from Benjamin Soltoff’s “Computing for the Social Sciences” course materials, licensed under the CC BY-NC 4.0 Creative Commons License.
