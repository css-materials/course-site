---
title: "HW04: Tidying data & programming in R"
date: 2024-11-06T13:30:00-06:00  # Schedule page publish date
type: book
toc: true
draft: true
aliases: ["/hw04-programming.html"]
categories: []
weight: 40
---




# Overview

**Due Thursday, November 7th (11:59 PM).**

The past couple of weeks we learned `tidyr` principles to wrangle data, as well as key programming concepts in R. The goals of this homework assignment are to (1) practice manipulating tidy data, and (2) demonstrate competency in R programming skills, especially control structures (e.g., conditional statements and loops).


# Accessing and cloning your `hw04` repository

* Go [at this link]() to accept the invitation and create your private `hw04` repository on GitHub. Once you do so, your repo will be built in a few seconds. It follows the naming convention `hw04-<USERNAME>`
* Once your repository has been created, click on the provided link to access it. 
* Finally, follow the [same steps you completed for `hw01`](/homework/edit-readme/) to clone the repository to your R Workbench.


# General workflow

See Homework 1 for details.


# Assignment description

This homework assignment consists of two parts: 
* Part 1: practicing tidying data with `tidyr`
* Part 2: practicing programming in R by applying the programming techniques we have learned so far 

In the repo for this assignment you will find a `.Rmd` file with the questions for each part.

For part 1, your main task is to tidy a data frame called `dadmom`, which is in the `rcis` package. The final product should look like this:


| famid|parent |name |   inc|
|-----:|:------|:----|-----:|
|     1|d      |Bill | 30000|
|     1|m      |Bess | 15000|
|     2|d      |Art  | 22000|
|     2|m      |Amy  | 18000|
|     3|d      |Paul | 25000|
|     3|m      |Pat  | 50000|

Please note:

REVISE MAYBE SKIP: * The questions, especially the open-ended ones, are designed to help you think and plan before diving into coding, similar to challenges you might face in real-world research settings. They won’t lay out exact step-by-step instructions, as they encourage you to apply and expand on the code you've learned so far. One of the main goals of this assignment (and future ones) is for you to tackle these challenges independently. We know you can do it!
* All assignments are designed to be completed in multiple coding sessions. Start early, and save, stage, commit, and push often!
* You are not allowed to use AI tools to generate R code to complete this and future assignments. The only acceptable uses of AI tools are the following two: debugging (but only after you have made an attempt on your own) and generating examples of how to use a specific function (but also check the function documentation, and the course materials -- if there are many ways to code something, you are expected prioritize what we have learned vs. what we have not). While AI tools can be helpful outside of class, this is a coding course, and it's all about learning to code in R, not learning to use AI!
* Do not submit code that you cannot fully explain to yourself and someone else.

Refer to HW2 guidelines for formatting tables and graphs. Ensure you follow proper R coding style and make appropriate use of comments in your code (refer to the readings and lecture on this topic).


# Submit the assignment

To submit the assignment, follow these steps:

* First push to your repository the last version of your assignment before the deadline. Make sure to stage-commit-push the following files:

  - `programming_exercises.Rmd`: the main file you will add your code to
  - `programming_exercises.md`: you will generate this file from the `.Rmd` by knitting it 

* When you are ready to submit, copy your repository URL (e.g. `https://github.com/css-fall24/hw4-brinasab`) and submit it on Canvas under HW04 before the deadline. Do not submit files on Canvas, we only need the link to your repository 

* As part of your submission, at the end of the `.Rmd` for this homework, include a few reflections on your experience with this assignment, list any help you might have received (from both humans and AI), as specified in the instructions.


# Assessment

All homework assignments are evaluated using a rubric which you can access from the assignment submission folder on Canvas. See also [here](/faq/homework-evaluations/) for more. 

Further guidelines for this specific homework to help you assess your work before submitting it.

In the past, "Excellent" or "Very Good" work included submissions that completed all components of the assignment correctly and accurately. Code ran correctly, followed proper style, and was well-documented without excessive comments. The code was appropriately complex and aligned with the prompt and course material (e.g., demonstrating a nuanced understanding of concepts and using them effectively throughout the assignment).

REVISE MAYBE SKIP: Graphs and tables were well-executed and carefully chosen (e.g., matching variable types with graph types), with appropriate labels, colors, and enhanced default settings. The analysis was clear and easy to follow, with graphs properly interpreted. Explanation of the student's logic to solve a task, when required, was clear and on-point. 

There was a solid command of basic R programming, of required packages, extending beyond the basics. Additionally, the repository showed a history of multiple informative commits, reflecting the progression and backup of work. Command of R Markdown syntax was evident, with no errors.


# Acknowledgments

<!--

* This page has been developed starting from Benjamin Soltoff’s “Computing for the Social Sciences” course materials, licensed under the CC BY-NC 4.0 Creative Commons License.
-->

The initial version of this homework was developed by Benjamin Soltoff  (“Computing for the Social Sciences” licensed under the CC BY-NC 4.0 Creative Commons License). Further implementations have been developed by Sabrina Nardin.
