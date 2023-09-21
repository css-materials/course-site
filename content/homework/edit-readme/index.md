---
title: "HW01: Practice editing .md and .Rmd"
date: 2022-09-29T13:30:00-06:00  # Schedule page publish date
#publishdate: 2019-03-01

draft: true
#type: post
aliases: ["/hw01-edit-README.html"]

summary: "Test software installation, GitHub setup, and homework submission process, as well as demonstrate basic competency in Markdown and R Markdown."
---



# Overview

**Due by 11:59 pm on Friday, October 7th.**

The goal is to test your software installation, your GitHub setup, and the homework submission process, as well as demonstrate basic competency in Markdown and R Markdown.

# Accessing your `hw01` repository

* Go [at this link](https://classroom.github.com/a/GJXNztug) to accept and create your private `hw01` repository on GitHub. Once you do so, your repository will be built in a few seconds. It follows the naming convention `hw01-<USERNAME>`  
* Once the your repository has been created, click on the link you see, which will take you to your repository. 
* Finally, clone the repository to your computer (or R workbench) following the process below.

# Cloning your `hw01` repository

After you have accessed the `hw01` repository (see above), follow these steps to clone it. Whenever possible, this will be the preferred route for setting up your R projects:

* In RStudio or RStudio Workbench, start a new Project with *File > New Project > Version Control > Git*. In the "repository URL" paste the URL of your newly created GitHub repository: go back to the repository, click on the green button "Code" and grab the correct link, either SSH or HTTPS (the one you used to set up your cache credentials). The repository name should automatically populate; if not, type your `hw01-<USERNAME>` as name. 
* Decide where to store the local directory for the project. Don't scatter everything around your computer - have a central location, or some meaningful structure. For example, for repositories you create in this course, you can setup a `css` directory and clone all your repos there.
* Before proceeding, check the little box "Open in new session", as that's what you'll usually do in real life.
* Click "Create Project" to create a new sub-directory, which will be all of these things:
    * a directory on your computer
    * a Git repository, linked to a remote GitHub repository
    * an RStudio Project

{{% callout note %}}
Before completing the above steps, ensure you followed the configuration steps [here](/setup/git-configure/), and everything works as expected.
{{% /callout %}}

# General workflow

Your general workflow will be:

<!--
* Pull from GitHub (just an empty precaution now, but it will matter when you collaborate with others)
-->
* Accept the repo and clone it (see above)
* Make changes locally to the files (here `README.md` and `Rcode.rmd`) in RStudio
* Save your changes
* Stage-Commit-Push: stage and commit your changes to your local Git repo; then push them online to GitHub. You can complete these steps using the Git GUI integrated into RStudio -- if you have not yet, I strongly recommend to go through the [Using Git with R Studio](/setup/git/git-with-rstudio) tutorial to get comfortable with the workflow. In general, you do not want to directly modify your online GitHub repo; instead modify your local Git repo, then stage-commit-push your changes up to your online GitHub repo. 


# What you need to submit

Written assignments for this course will be submitted using Markdown and R Markdown: [Markdown](https://daringfireball.net/projects/markdown/) (.md) is a lightweight text formatting language that easily converts between file formats. Regular Markdown files (.md) are rendered on the GitHub website and can be directly read on the website. They are also integrated directly into [R Markdown](https://rmarkdown.rstudio.com/) (.rmd or .Rmd), which combines R code, output, and written text into a single document. GitHub includes a [guide](https://guides.github.com/features/mastering-markdown/) for writing Markdown documents.

For this assignment, you need to modify and push to your GitHub homework repository the following two files: `README.md` and `Rcode.rmd`


## `README.md` 

You will notice there is already a `README.md` file in the repo. A README is usually a plain .txt or .md file. The purpose of a README file in a repository is to communicate important information about your project (software, how to run the code, preview of the results, etc.). The goal of this assignment is to practice generating and editing README.

Your task is to edit this file by adding a brief biography of yourself. To achieve full marks, your README should include the following elements:

* Headers (one or more)
* Emphasis (italics or/and bold)
* Lists
* Images: add a picture (of yourself or something else) to your repo and embed it in your README
* Links
* A summary and reflection of the Git/GitHub workflow you adopted for this homework, and of your experience with Markdown (e.g., provide a summary of the workflow you adopted, and add some comments about something new you learned, something that surprised you, etc.)


## `Rcode.rmd`

You will notice there is already a `Rcode.rmd` file in the repo. Your task is to edit this file by adding more YAML arguments (see readings) and at least two R code chunks. To achieve full marks, your `Rcode.rmd` should include the following elements:

* At least one new YAML Header argument. You can modify one of three arguments that are already there or add a new one to them (e.g., author, subtitle, table of contents, etc.)
* At least two R code chunks:
  * Rely on the in-class materials "intro to R" as starting point, but do not copy the exact code we have seen in class: make some changes to customize or expand it
  * Notice the code chunks must execute correctly and your final knitted document (which you should submit as well, preferably as md or html) must display both the code and the results
* Before each code chunk, add a brief text that explains what each code chunk does


# Submit the assignment

To submit the assignment, simply push to your repository the last version of your assignment before the deadline. Then copy your repository URL (e.g. https://github.com/css-fall22/hw1-brinasab) and submit it to Canvas under HW01 before the deadline.

# Rubric

Needs improvement: `README.md` says the equivalent of "This is the repository of Name Surname" with little details. `Rcode.rmd` contains R code chunks, but no explanation nor additional YAML headers are added. All work done via Git/Github ... but that's just a guess, because the student doesn't explain how it was done. 

Satisfactory: Something in between.

Excellent: `README.md` provides a proper introduction of the student. It also demonstrates experimentation with several aspects of the Markdown syntax (e.g., section headers, links, bold, italic, bullet points, image, etc.). The student describes how they got the changes into `README.md` and offers a few reflections on their Git/GitHub workflow and their experience with Markdown. `Rcode.rmd` knits properly and contains one or more new YAML headers, R code chunks, with a detailed explanation of them.

For further details, see the [general rubric](/faq/homework-evaluations/) we adopt for grading.


# Acknowledgments


* This page is derived in part from ["UBC STAT 545A and 547M"](http://stat545.com), licensed under the [CC BY-NC 3.0 Creative Commons License](https://creativecommons.org/licenses/by-nc/3.0/).

* This page has been developed starting from Benjamin Soltoff’s “Computing for the Social Sciences” course materials, licensed under the CC BY-NC 4.0 Creative Commons License.
