---
title: "HW01: Practice editing .md and .Rmd"
date: 2022-09-29T13:30:00-06:00  # Schedule page publish date
#publishdate: 2019-03-01

draft: true
#type: post
aliases: ["/hw01-edit-README.html"]

summary: "Test software installation, GitHub setup, and homework submission process, as well as demonstrate basic competency in Markdown and R Markdown. Due Oct 7, 2022"
---



# Overview

Due by 11:59pm on Friday, October 7th.

The goal is to test your software installation, your GitHub setup, and the homework submission process, as well as demonstrate basic competency in Markdown and R Markdown.

# Accessing the `hw01` repository

Go [here](https://github.coecis.cornell.edu/cis-fa22) and find your copy of the `hw01` repository. It follows the naming convention `hw01-<USERNAME>`. Clone the repository to your computer using the process below.

Whenever possible, this will be the preferred route for setting up your R projects:

* In RStudio or RStudio Workbench, start a new Project

* ADD: accept the homework report

* *File > New Project > Version Control > Git*. In the "repository URL" paste the URL of your new GitHub repository.
* Decide where to store the local directory for the project. Don't scatter everything around your computer - have a central location, or some meaningful structure. For example, for repositories you create in this course, you can setup a `css` directory and clone all your repos there.
* I suggest you check "Open in new session", as that's what you'll usually do in real life.
* Click "Create Project" to create a new sub-directory, which will be all of these things:
    * a directory on your computer
    * a Git repository, linked to a remote GitHub repository
    * an RStudio Project

{{% callout note %}}
Make sure you followed the configuration steps [here](/setup/git-configure/) and are able to authenticate yourself before completing the above steps.
{{% /callout %}}

# General workflow

[Your general workflow](/faq/homework-guidelines/#homework-workflow) will be:

<!--
* Pull from GitHub (just an empty precaution now, but will matter when you collaborate with others)
-->
* ADD: accept the repo and store it in a a location of your pc (see above)

* Make changes locally to the files (here `README.md` and `Rcode.rmd`) in RStudio
* Save your changes
* Stage-Commit-Push: stage and commit your changes to your local repo; then push them online to GitHub (You can complete these steps using the Git GUI integrated in RStudio).


# What you need to submit

Written assignments for this course will be submitted using Markdown and R Markdown: 

[Markdown](https://daringfireball.net/projects/markdown/) (.md) is a lightweight text formatting language that easily converts between file formats. Regular Markdown files (.md) are rendered on the GitHub website and can be directly read on the website. They are also integrated directly into [R Markdown](https://rmarkdown.rstudio.com/) (.rmd or .Rmd), which combines R code, output, and written text into a single document. GitHub includes [a guide](https://guides.github.com/features/mastering-markdown/) for writing Markdown documents.

For this assignment you need to modify and push to your GitHub homework repo the following two files: `README.md` and `Rcode.rmd`


## `README.md` 

When you create the repository, you will notice there is already a `README.md` file in the repo. Your task is to edit this file by adding a brief biography of yourself. To achieve full marks, your README.md should include the following elements:

* Headers (one or more)
* Emphasis (italics or/and bold)
* Lists
* Images: add a picture (of yourself or of something else) to your repo and embed it in your readme
* Links
* A summary and reflection of the GitHub workflow you adopted for this homework, and your experience with Markdown 


## `Rcode.rmd`

When you create the repository, you will notice there is already a `Rcode.rmd` file in the repo. Your task is to edit this file by adding more YAML specifications and at least two R code chunks. To achieve full marks, your `Rcode.rmd` should include the following elements:

* At least two new Yaml Header specifications (you can add a date, define the output, etc. review the readings for more info)
* At least two code chunks 
* A brief text that explains what each code chunk does
* Show the output of each code chunk


# Submit the assignment

Follow instructions on [homework workflow](/faq/homework-guidelines/#homework-workflow).

# Rubric

Needs improvement: `README.md` says equivalent of "This is the repository of Benjamin Soltoff". `Rcode.rmd` contains R code chunks, but no explanation nor additional yaml headers are added. All work done via browser at github.com ... but that's just a guess, because student doesn't actually say how it was done. 

Satisfactory: something in between

Excellent: `README.md` provides a proper introduction of student to the class. It also demonstrates experimentation with several aspects of the Markdown syntax (e.g., section headers, links, bold, italic, bullet points, image embed, etc.) The student describes how they got the changes into `README.md` and offers a few reflections on their GitHub workflow and their experience with Markdown. `Rcode.rmd` knits properly and contains yaml headers, R code chunks, with detailed explanation of them.

## Acknowledgments


* This page is derived in part from ["UBC STAT 545A and 547M"](http://stat545.com), licensed under the [CC BY-NC 3.0 Creative Commons License](https://creativecommons.org/licenses/by-nc/3.0/).

* This page has been developed starting from Benjamin Soltoff’s “Computing for the Social Sciences” course materials, licensed under the CC BY-NC 4.0 Creative Commons License.
