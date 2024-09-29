---
date: "2024-09-28T00:00:00-05:00"
draft: false
weight: 50
title: "How to ask for help"
toc: true
type: book
aliases: "/hw00_asking_questions.html"
---



## 15-minute rule 

You will likely stumble in this course, you will get confused, not understand how to perform a task, or why your code is generating an error. That's normal, and it is part of the learning process. Be patient and keep coding! By the end of the course, you will be surprised at how much you have learned in such a short amount of time. 
We will follow the *15-minute rule* in this class: if you encounter a problem in your assignments, spend 15 minutes troubleshooting the problem on your own. You can use ChatGPT, Google, StackOverflow, etc. for help. However, if after 15 minutes or so you cannot solve the problem, ask for help from the instructional staff and your peers.

Note on the use of AI: you are allowed to use AI to help with assignments, but you are not allowed to copy/paste code written by AI, found online, or written by someone else (your peers, etc.). We will run random checks and if we find plagiarized code, the whole assignment will be graded as 0. Read our [Plagiarism policy](https://computing-soc-sci.netlify.app/faq/course-obj-expectations/#plagiarism-and-academic-integrity) for details.

## Tips to follow when posting questions on Ed

Asking questions is an important part of this class. Questions should be posted to Ed Discussion in the appropriate category. 

  * Before posting, search if someone else has posted the same or a similar question
  * Provide an informative title
    * not informative: "Nothing works!!"
    * informative: "Getting a 'file not found error' when importing scotus.csv"
  * Use good manners (say Hello, thank you, re-read your comments before you post them, support your peers, etc.)
  * Post your attempt at solving the problem: share your code (use the code option on Ed with symbol "<>"), describe what you have already attempted, and post pertinent error messages
  * If you solve the problem, let us know (you can heart questions/answers you find useful!), and feel free to post your solution
  * Answer questions you feel confident answering to help out your peers 
  * You can ask questions anonymously, privately (only staff can see them), or publicly. We prefer you ask questions publicly, so everyone can benefit from your question and we minimize repetitions
  * Allow 24 hours to receive an answer; please understand that questions posted the day the homework is due might not receive a reply on time, and questions posted during the weekend might not get answered until the following Monday

  
## Additional suggestions for posting

* Include a minimal, complete, and verifiable example (see [here](http://stackoverflow.com/help/mcve)) of the code you are using; this greatly helps us resolve your problem. You don't need to copy all the code from your program into the comment, but include enough code that we can run it successfully *until the point at which the error occurs*.
* Make sure you have pushed your recent commits to the GitHub repo. If it is up-to-date, we can look in or clone your repo to our machines to replicate the problem.
* Format your code snippets with the `reprex` package (see below)


## How to use `reprex`

The [`reprex`](http://reprex.tidyverse.org/) package allows you to generate reproducible examples that are easily shared via email, ED Discussion page, or GitHub with all the proper formatting and syntax.

Install it by running the following command from your R console:

```r
install.packages("reprex")
```
To use it, first, make sure the `reprex` library is loaded into R:

```r
library(reprex)
```

Then, run this demonstration code into your console by putting it inside the `reprex()` function (notice this code contains an error, observe the reprex output):

```r
reprex({
  library(tidyverse)
  count(diamonds, colour)
  })
```

If you run this in your console, you should see a nicely rendered HTML code in your RStudio's Viewer. All you have to do is to go the location where you want to paste that code (GitHub, Ed Discussion, email, etc.) and right-click "paste" (i.e., you do not need to "copy" it first, just "paste" it in your desired location).

The nice thing is that if your script also produces images or graphs (for example, using `ggplot()`) these images are automatically uploaded and included in the issue.

Note: make sure to load all necessary packages and data objects at the top of your copied code. This may involve opening a new tab in the editor panel and writing a short version of the script that only includes the essentials, then copying that script to the clipboard and `reprex()` it.

Sometimes problems are caused by using older or incompatible versions of packages. The `session_info()` function in the `sessioninfo` library will print a list of all active packages and their respective versions. Include this in your post so we know which versions of packages you are using by setting `si = TRUE` in the `reprex()` function, like this: `reprex(si = TRUE)`.


## Acknowledgments

* ["How do I ask a good question?" StackOverflow.com](http://stackoverflow.com/help/how-to-ask)
* ["How to Ask Programming Questions," ProPublica.com](https://www.propublica.org/nerds/item/how-to-ask-programming-questions)


* This page has been developed starting from Benjamin Soltoff’s “Computing for the Social Sciences” course materials, licensed under the CC BY-NC 4.0 Creative Commons License.
