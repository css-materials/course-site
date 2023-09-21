---
date: "2022-09-25T00:00:00-05:00"
draft: false
weight: 10
title: "Should I take this course?"
toc: true
type: book
#aliases: ["/hw00_peer-review.html"]
---


## General description

This course is open to any graduate and advanced undergraduate at the University of Chicago. I anticipate drawing students from a wide range of departments such as Information Science, Sociology, Psychology, Political Science, etc. Typically these students are looking to learn basic computational and analytic skills they can apply to master's projects or dissertation research.

I start from the perspective that you want to analyze data, and *programming is a means to that end*. You will not become an expert programmer, but you will learn the basic skills and techniques necessary to conduct computational social science, and gain the confidence necessary to learn new techniques as you encounter them in your own research.

We will cover many different topics in this course, including:

* Elementary programming techniques (e.g., loops, conditional statements, functions)
* Writing reusable and clear code
* Problem-solving and debugging programs for errors
* Visualizing information
* Obtaining, importing, and munging data from a variety of sources
* Performing textual analysis
* Generating reproducible research

If you have never programmed before **prepare for a shock**. This class will prove to be very beneficial if you stick with it, but that will require you to commit for the full quarter. I guarantee that the first few weeks and assignments will be rough - but the good news is that they will be rough for everyone! Your classmates are struggling with you and you can lean on one another to get through the worst part of the learning curve.


## Who is this class for?

Meet some of the types of students you will find in this class

### Jeri

{{< figure src="jeri.jpg" >}}

* Starting points
    * Ph.D. student in Sociology
    * Has experience analyzing data in Stata
    * Feels comfortable with regression and other stats methods 
    * Tried to learn Git on her own once, quickly became frustrated and gave up
* Needs
    * Wants to transition from Stata to R 
    * Will be analyzing a large-scale dataset for her dissertation
    * Seeks a reproducible workflow to manage her data projects

### Ryan

{{< figure src="ryan.jpg" >}}

* Starting points
    * Entering the [MAPSS program](https://mapss.uchicago.edu/)
    * Undergraduate degree in journalism
    * Hasn't taken a statistics class in years
    * Took an online course of introduction to R, but hasn't used it in his day-to-day work
* Needs
    * Writing a master's thesis in a single year
    * Expects to analyze a collection of published news articles 
    * Wants to understand code samples found online and adapt them to his own work


### Fernando

{{< figure src="fernando.jpg" >}}

* Starting points
    * Third-year undergraduate student
    * Majoring in political science
    * Has taken general education math/stats courses
    * Does not have programming experience, but isn't afraid to tackle a new challenge
* Needs
    * Wants to work as a research assistant on a project exploring the onset of civil conflict, which is run exclusively in R
    * Will start contributing to a new research paper next quarter
    * Wants to produce high-quality visualizations
    

### Fang

{{< figure src="fang.jpg" >}}

* Starting points
    * First year grad-student
    * Background in psychology, plans to apply for doctoral programs in marketing
    * Has experience using Excel, SPSS, and Stata
* Needs
    * Is going to analyze data collected by her lab members in the next six months
    * Wants to produce analysis notebooks that are easily shareable with her colleagues
    * Expects to take courses in machine learning and statistics which require a background in R



<!--
A highly selective sampling of feedback from when I taught [a similar course at the University of Chicago](https://cfss.uchicago.edu):

> I think this class is really well-organized. The homework is craftily designed as a way to solidify the materials learned in class. Dr. Soltoff is wonderful and helpful! He came to class fully prepared and made the lectures enjoyable and productive. I suggest that all Ph.D. students in Political Science (at least in my field), who likes to conduct quantitative research, should choose this class in the first year, because this class can well set students up with a good understanding of programming techniques.

> Very useful material that I hated learning until 2/3 through the quarter.

> This class can set you up really nicely with conversant knowledge in R programming and a large amount of coding materials that are helpful for future research. And it also provides students with a first-hand experience of using some of the cutting edge methods and makes students have a taste of them.

> I'm so so so glad I ended up taking this course. I had a lot of doubts about my own (lack of) skills and my inability to to handle so many things in one quarter. I had a lot of apprehensions about this course but they all quickly disappeared. It's quite honestly been one of the most valuable courses I've taken at this University and I attribute all of that to your excellence as a lecturer. You and the TAs have always been extremely accessible to everyone and I can't appreciate that enough. In other classes, I would've been more hesitant to ask "dumb questions" but you all have made me comfortable doing so, and I have benefited immensely from it.

> I feel like every time I have a question or want to participate, I am always acknowledged. I also built a strong relationship with my classmates which is crucial for some of the difficult assignments.
-->


## What do I need for this course?

**You will need to bring a computer to class each day.** Class sessions are a mix of lecture, demonstration, and coding. It is essential to have a computer so you can follow along and complete the exercises. All class materials (including slides and notes) will be made available before/after class for your review.

<!--
By the end of the first week, you should make sure you can access the following software:

* [R](https://www.r-project.org/) - the easiest approach is to select a [pre-compiled binary appropriate for your operating system](https://cran.rstudio.com/).
* [RStudio's IDE](https://www.rstudio.com/products/RStudio/) - this is a powerful user interface for programming in R.
* [Git](https://git-scm.com/) - Git is a [version control system](https://en.wikipedia.org/wiki/Version_control) which is used to manage projects and track changes in computer files. Once installed, it can be integrated into RStudio to manage your course assignments and other projects.

Comprehensive instructions for downloading and setting up this software can be found [here](/setup/).
-->

## Acknowledgments

* Stock photos of student learners by [Generated Photos](https://generated.photos/)
* This page has been developed starting from Benjamin Soltoff’s “Computing for the Social Sciences” course materials, licensed under the CC BY-NC 4.0 Creative Commons License.



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
