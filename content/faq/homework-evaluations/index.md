---
date: "2022-09-25T00:00:00-05:00"
draft: false
weight: 40
title: "Evaluation Guidelines"
toc: true
type: book
aliases: ["/hw00_homework_grading.html", "/hw00_github_rubric.html"]
---

## Weekly assignments

Students will complete a series of (roughly) weekly programming assignments linked to class materials. See the [Homework](https://computing-soc-sci.netlify.app/homework/) section of this website for more info. 
Assignments will initially be very detailed, and will come with starter code or an initial version of the program where you need to fill in the blanks to make it work. As the quarter moves on and your skills become more developed, less help upfront will be provided. 

## Missed assignments, resubmission, late work, etc.

* Assignments must submitted on time. Late work is not accepted. However, you are allowed to submit one assignment of your choice up to 24-hour late without penalty, no-questions-asked.
* A missed assignment is worth 0% and as such will negatively affect your final grade. If you miss an assignment due to serious illness or emergency, please reach out.
* You can re-do one assignment of your choice and we will re-grade it. The re-do can be submitted at any time before the last day of class and must include a narrative that explains why you are re-doing the assignment and what you have improved (e.g., "I did not understand functions that well, especially this and that. Now...")
* Incomplete assignments are graded as follows. If more than 25% of the assignment is missing, we won't grade it and we will treat it as a missed assignment. Otherwise, we will grade it with a penalty for each element of the rubric (e.g. if you score "Good" on "Reproducibility" you will gain "Satisfactory" etc.) 
* Plagiarism is a serious issue. While students are encouraged to assist one another in debugging programs and solving problems, it is imperative students also learn how to do this for themselves. That is, students need to understand, write, and submit their own work. Please read the [Plagiarism](https://computing-soc-sci.netlify.app/faq/course-obj-expectations/#plagiarism-and-academic-integrity) info under Course Expectations.


## Evaluation philosophy

The university requires that I assign each student a letter grade at the end of the quarter. However, I find that numeric scores on assignments tend to cause students grading anxiety if they do not achieve a perfect 100%. Nor does the numeric score convey specific feedback on what the student has done well on an assignment and on areas for improvement.

As such, I do not assign numeric scores in this class. All homework assignments are evaluated using the grading rubric below. Final grades are calculated as the cumulative performance across all homework assignments. 

<!--
Failure to complete the two weekly [peer evaluation assignments](/faq/peer-evaluations/) causes a minor deduction in the final grade.
-->


## Rubric

Your assignments will be evaluated using the general rubric posted below. In addition, each assignment will have specific guidelines that further explain our expectations (these will be posted in the assignment itself). 

Your assignment will score *Excellent*, *Good*, or *Needs improvement* on the following topics:
* *Coding style:* coding style pertains to stylistic issues, not to whether your code works. It evaluates how well the code follows the [convention for R code](http://adv-r.had.co.nz/Style.html) and how consistent it is. Examples include clarity of the code to read for a person who has not written it, use of comments (code should never be over-commented, nor under-commented), proper variables names, understandable/logical code organization, etc. See [here](https://www.smashingmagazine.com/2012/10/why-coding-style-matters/) for more and why this matters
* *Coding strategy:* by coding strategy, we mean the logic of your code (how your code approaches and solves the given problem), its correctness (whether it works), how sophisticated it is, how well it incorporates the tools and techniques we learn in class (e.g., conditionals, functions, general use of tidyverse syntax, etc.), and whether it minimizes repetition and optimize efficiency
* *Presentation:* in assignments that have data visualization or data presentation components of any sort (tables, graphs, descriptive stats, more sophisticated analyses), presentation evaluates how well these components are executed both graphically and conceptually (your choices of how to present data). In all assignments, presentation will also evaluate your mastery of Markdown syntax. 
* *Achievement:* evaluates your understanding of the concepts/tools required to complete the assignment (how well you master them) and your ability to use and go beyond the basic tools; it praises extraordinary work produced in the assignment
* *Reproducibility:* evaluates how well the assignment is in compliance with the course convention for submitted work in this course (e.g., whether we can access your repo, you submit all required elements, your use of Markdown and RMarkdown, Git/GitHub, README, etc.), and whether the submitted materials allow to successfully reproduce your work 

To obtain *Excellent* in a given categories all requirements must be satisfied. For the other two evaluations, it might be that only one (or more than one) requirement is missing. For example, you could achieve *Good* on "Coding style" if you are following all coding conventions and are submitting a well-commented code, but your code lacks refinement or is inconsistent.


In addition to this general rubric, make sure to consult any specific guidance given in the relevant assignment itself

Topic| Excellent: <br> ✓+ coded as +  | Good: <br> ✓ coded as 0  |Needs improvement: <br> ✓- coded as - |
|-----------| ---------------------- |--------------------------| ---------------------------------------|
|Coding style| Student has gone beyond what was expected and required. Coding conventions are followed consistently (spaces, variable names, etc.). Code is well-commented and easy to read. | Coding conventions are partly followed. Code is readable but lacks some comments or is overly commented. Code could be more refined and/or is inconsistent. | Coding conventions minimally or not followed. Code has no comments and little attention is paid to making the code human readable. Code lacks refinement and/or is inconsistent. |
|Coding strategy| Logic behind the code is clear. Complicated problem broken down into sub-problems that are individually much simpler. Code is efficient, correct, and minimizes repetitions. Code uses appropriate concepts learned in class (e.g. use proper data structure, etc.). All code runs correctly and checks for common errors. | Logic is overall clear. Code is mostly correct, but could be edited down to leaner code. Some "hacking" instead of using proper tools (e.g., suitable data structure) and/or efficiency and repetitions could be improved. | Logic is difficult to follow. Code tackles complicated problem in one big chunk. Some parts of the code might be repetitive, for example it could easily be functionalized. Code does not check for errors and/or code does not run.|
|Presentation| Graph(s)/tables(s) carefully tuned for desired purpose. One graph/table illustrates one point. Careful styling highlights important features. Full command of Markdown syntax and its components. | Graph(s)/tables(s) well chosen, but with a few minor problems (e.g., inappropriate aspect ratios, poor labels, formatting deficiencies, etc.). Appropriate use of Markdown syntax and its components, with some minor deficiencies. | Graph(s)/tables(s) poorly chosen to support questions and illustrate findings. Major display problems with graphs, tables and/or Markdown components.|
|Achievement|Student has gone beyond what was expected and required (e.g., extraordinary outcome, additional tools not explicitly addressed by this course and/or sophisticated use of tools from course).| Tools and techniques from the course are applied competently and somewhat creatively. Chosen task is good, but fairly conservative in ambition.|Student does not display the expected level of mastery of the tools and techniques in this course. Chosen task is too limited in scope.|
|Reproducibility| Full compliance with course conventions for submitted work in this course. Access is as easy as possible, complies with reproducibility conventions, code runs, workflow is correct. | Code partially complies with reproducibility conventions and/or code does not run. | Not an earnest effort to reduce friction and comply with conventions and/or code does not run.|

## Template

```
Evaluation
-----------------------------------------------------------------------------
| Topic                       | Excellent | Good         | Needs Improvement |
|-----------------------------|-----------|--------------|------------|
| **Coding style**            |           |              |            |
| **Coding strategy**         |           |              |            |
| **Presentation**            |           |              |            |
| **Achievement**             |           |              |            |
| **Reproducibility**         |           |              |            |

Examples of further remarks:
* Elaborate on above, especially for "Needs improvement"
* Specific praise
* Specific constructive criticism

```

## How do the rubric scores convert to a letter grade?

<!--
One year on my course evaluations a student commented

> [T]he grading policy is locked in some chest somewhere under the ocean
Let's pull back the curtain and demystify how I calculate final grade! 
-->

* In this course, "Good" is equivalent to a B+. So if you earned "Good" on every assignment for every rubric element, at the end of the quarter you would earn a B+. 
* If you earn a combination of "Good" and "Excellent" scores you are looking at the difference between a B+ and an A-, or an A- and an A. 
* If you earn a combination of "Good" and "Needs Improvement" scores, then you might be somewhere between a B+ and a B or lower.
* Etc. etc.

Historically, the majority of students in the class earn a B+ or higher. 

The final grade is calculated assuming you are submitting all homework assignments: missed assignments or incomplete work will negatively affect your grade (see above for more info)



## Acknowledgments


* This page is derived in part from ["UBC STAT 545A and 547M"](http://stat545.com), licensed under the [CC BY-NC 3.0 Creative Commons License](https://creativecommons.org/licenses/by-nc/3.0/).

* This page has been developed starting from Benjamin Soltoff’s “Computing for the Social Sciences” course materials, licensed under the CC BY-NC 4.0 Creative Commons License.




<!--
You will complete a series of programming assignments throughout the quarter linked to class materials. Assignments will initially come with starter code, or an initial version of the program where you need to fill in the blanks to make it work. As the quarter moves on and your skills become more developed, less help upfront will be provided. Each assignment will be evaluated by myself or a TA.

Each assignment will be evaluated by myself or a TA, as well as by *two peers*. Peer review is a crucial element to this course, in that by [eating each other's dog food](https://en.wikipedia.org/wiki/Eating_your_own_dog_food) you will learn to read, debug, and reproduce code and analysis. And while I and the TAs are competent users in R, your classmates are not - so make sure your code is [well-documented](#documentation) so that others with basic knowledge of programming and R can follow along and reuse your code. Be sure to read the instructions for [peer review](/faq/peer-evaluations/) so you know how to provide useful feedback.

<!--
As part of this course you will be reviewing, commenting on, and marking other students' assignments. This is a mandatory part of the course: failure to complete peer reviews will result in a mark down on your final grade.

## Expectations for peer reviewer

* Identify three **specific things** your peer did well
* Identify three **specific things** the student could improve upon (and ideally provide a suggested approach or solution)

## How to do peer review well

* Give thoughtful, constructive and considerate comments
* Be specific and concise
* Use [the rubric](/faq/homework-evaluations/) for ideas about criteria to evaluate and comment on
* Try to learn something new and, if you succeed, point that out
* If you can't find anything to praise or that you found helpful, then at least offer some suggestions in a kind way
* See [here](https://help.github.com/articles/reviewing-proposed-changes-in-a-pull-request/) for useful instructions on how to initiate and submit reviews using GitHub's built-in tools
* To ensure reproducibility, you might find it useful to clone your classmate's repo and attempt to run their script(s). If you cannot execute them, then the code is not reproducible. Also be aware your classmates will hold you to a similar standard.

## How to do peer review bad

* Your review is so generic that it's hard to determine which assignment you're reviewing
* Your review is mean
* You can't find anything to praise/learn and yet you don't offer any suggestions either

Performing good peer review is difficult! In graduate school we are taught to criticize and tear down others' work and find the flaws. We need to be better at this and not just criticize, but highlight good aspects and suggest how to improve the work. This is still a habit I am struggling to break, so start working on it now before you leave grad school.

## Acknowledgments


* This page is derived in part from ["UBC STAT 545A and 547M"](http://stat545.com), licensed under the [CC BY-NC 3.0 Creative Commons License](https://creativecommons.org/licenses/by-nc/3.0/).
-->

