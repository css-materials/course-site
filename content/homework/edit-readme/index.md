---
title: "HW01: Test software setup and practice editing files"
date: 2024-09-30T13:30:00-06:00 
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

**Due Tuesday, October 8th (11:59 PM Chicago Time).**

The goals of this first homework assignment are: (1) to test your computer setup and the homework submission process; (2) to demonstrate competency in basic R syntax, Markdown, and R Markdown.  


# Accessing your `hw01` repository

{{% callout note %}}
This will work only if you have provided us your GitHub username (see Lecture 1) and accepted the email invitation to join our organization.
{{% /callout %}}

* Go [at this link](https://classroom.github.com/a/pOTPCO2T) to accept the invitation and create your private `hw01` repository (or "repo" for short) on GitHub. Once you do so, your repo will be built in a few seconds. It follows the naming convention `hw01-<USERNAME>`
* Once your repository has been created, click on the provided link to access it. 
* Finally, clone the repository to your R Workbench following the process below.


# Cloning your `hw01` repository

{{% callout note %}}
Before completing this part, ensure you followed the configuration steps (see [Setup](https://computing-soc-sci.netlify.app/setup/)), and everything works as expected.
{{% /callout %}}

After you have accessed the `hw01` repository, follow these steps to clone it:

* In RStudio or RStudio Workbench, start a new Project with *File > New Project > Version Control > Git*. In the "repository URL" paste the URL of your newly created GitHub repository: go back to the repository, click on the green button "Code" and grab the correct link, either SSH or HTTPS (the one you used to set up your cache credentials: if you are using R Workbench it is SSH). The repository name should automatically populate; if not, type your `hw01-<USERNAME>` as name.
* Decide where to store the local directory for the project (tip: have a central location, or some meaningful structure).
* Before proceeding, check the little box labeled "Open in new session;" this is not strictly necessary but is a common best practice
* Click "Create Project" to create a new sub-directory, which will be all of these things:
    * a directory on your computer
    * a Git repository, linked to a remote GitHub repository
    * an RStudio Project

You will use this process for accessing and setting up all homework assignments. Whenever possible, I recommend using this process also for setting up your R projects beyond this course, but other options are possible (see [Using Git with R Studio](/setup/git/git-with-rstudio) for more).


# General workflow

Your general workflow for all homework assignments will be:

* Accept the Git repo and clone it (see above)
* Make changes to the files included in the repo (for this assignment you will be working with two files: `README.md` and `Rcode.rmd`)
* Save your changes locally (e.g., in your RStudio or RStudio Workbench)
* Pull-Stage-Commit-Push: 
  * Pull from GitHub (nothing should happen here since you should always make changes to the local Git repo first; but it's a good habit to pull as first step, since pulling is important when you collaborate with others)
  * Stage and Commit the changes you have made to your local Git repo
  * Push your committed changes to your online GitHub repo

For this course, I assume you will complete these steps using the Git GUI integrated into RStudio. If you have not yet, complete the [Using Git with R Studio](/setup/git/git-with-rstudio) tutorial to get comfortable with the workflow.

Tips: 
* Stage, commit, and push your work often (multiple times during a working session!). Do not wait until you have completed the entire homework. 
* Avoid directly modifying files in your online GitHub repository. Always make changes in your local Git repository, then stage, commit, and push those changes to GitHub (online repo). The two repositories should mirror each other: think of your online GitHub repo as an online backup of local Git repo.


# Assigment descripion

All assignments for this course will be submitted using Markdown and R Markdown:
* [Markdown](https://daringfireball.net/projects/markdown/) (.md) is a lightweight and straightforward language for formatting text, easily converting between file format. For example, GitHub README files are often written in Markdown (with a .md extension) or as plain text (with a .txt extension). In this course, we use Markdown files because they are directly rendered on the GitHub website (vs. R Markdown files which are not), and are well integrated into R Markdown. You can embed R code in plain Markdown, but to execute it within your document together with written text you need to use R Markdown. 
* [R Markdown](https://rmarkdown.rstudio.com/) (.rmd or .Rmd) is an enhanced version of Markdown designed specifically for R. It combines R code, output, and written text into a single document. 

Generally, we will use R Markdown files for completing the bulk of the homework assignments; and we will use simple Markdown files only for writing the README of homework assignments. For this assignment, you need to modify and push to your GitHub repo the following two files: `README.md` and `Rcode.rmd`


## `README.md` 

You will notice there is a `README.md` file in your repository. A README is typically a plain text (.txt) or Markdown (.md) file. The purpose of a README file in a repository is to provide important information about your project to both yourself and others. This can include a summary of the project, required software, instructions on how to run the code, preview of the results, etc. The goal of this assignment is to practice generating and editing a README file.

Your task is to edit the `README.md` file by replacing the existing instructions with a brief biography of yourself. To achieve full marks ("pass"), your biography must include the following elements:

* Headers (one or more)
* Emphasis (italics or/and bold)
* At least one list
* Images: select a picture file (of yourself or something else), add it to your repo by importing it in R Workbench, and embed it in your README
* At least one link

At the end of the `README.md` add the following reflections (note that these reflections will be required for every assignment and should always be included in your repo):
* Provide a short descriptive summary of the Git/GitHub workflow you used for this homework. This can be in bullet points or a narrative format, as long as it briefly summarizes what you did
* Provide an evaluation of your experience with this homework as a whole. Mention something new you learned, something that surprised you, or any other insights. No length requirements. 
* List the resources you consulted to complete this assignment. If you used any AI tools, explain how you used them. If you collaborated with anyone, please list the names of your collaborators.

## `Rcode.rmd`

You will notice there is a `Rcode.rmd` file in the repository. Your task is to edit this file by adding two more YAML arguments and one R "code chunk" with text explanations. To achieve full marks ("pass"), your `Rcode.rmd` should include the following elements:

* At least two new YAML Header arguments. Important: do not modify those that are already there, simply add at least two new ones. Examples of new arguments include: author, subtitle, table of contents, etc. Do not be afraid to experiment, the readings (Lecture 1) offer several suggestions!
* At least two R code chunks: 
  * For this assignment, we won't evaluate the coding style or strategy (it can be simple!), but your code chunks must run, that is, they must execute correctly and provide an output and your final knitted document (which you should also submit) must display both code and result; your code is not expected to generate plots, but if it does, remember that the generated plots need to be pushed to GitHub as well
  * Before each code chunk, write a brief text explanation of what the code does; this explanation must be rendered as a text, not as a code comment (be mindful of the difference!)


# Submit the assignment

To submit the assignment, follow these steps:
* Before the deadline, push the last and final version of your assignment to your GitHub repository (tip: do not wait until you have completed the homework to make the first commit... commit, stage, and push often!). You GitHub repository should contain the modified `README.md` and `Rcode.rmd`, as well as the final knitted document that you generated starting from the `Rcode.rmd`: this document can be an .md or a word or pdf; but not an html
* When you are ready to submit, copy your repository URL (it will be similar to this: https://github.com/css-fall24/hw1-brinasab) and submit it to Canvas under HW01 before the deadline. Do not submit files on Canvas, we only need the repository URL. 


# Assessment

This homework is evaluated on a Pass/Fail basis. To earn a "Pass," we expect the following: 

The `README.md` provides a proper introduction of the student. It demonstrates experimentation with Markdown syntax (e.g., section headers, links, bold, italic, bullet points, image, etc.) and all requirements are met. The student provides a clear description on how they got the changes into `README.md` and offers a few reflections on their Git/GitHub workflow and experience with Markdown and R Markdown. The `Rcode.rmd` file knits properly and contains the required new YAML headers. It also includes at least two R code chunks and textual explanations of them. All required files have been submitted.

For more information, see the ["Assigments & Assessment"](https://computing-soc-sci.netlify.app/faq/homework-evaluations/) page of this website. 

<!--
# Acknowledgments


* This page is derived in part from ["UBC STAT 545A and 547M"](http://stat545.com), licensed under the [CC BY-NC 3.0 Creative Commons License](https://creativecommons.org/licenses/by-nc/3.0/).

* This page has been developed starting from Benjamin Soltoff’s “Computing for the Social Sciences” course materials, licensed under the CC BY-NC 4.0 Creative Commons License.
-->
