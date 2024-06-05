---
date: "2022-09-25T00:00:00-05:00"
draft: false
weight: 50
title: "How to ask for help"
toc: true
type: book
aliases: "/hw00_asking_questions.html"
---



You will stumble in this class, you will get confused, not understand how to perform a task, not understand why your code is generating an error. That's not only normal, but it is a necessary part of the learning process. Be patient and keep coding, by the end of the course you will be surprised on much you have learned in such a short amount of time. 

We will follow the *15 minute rule* in this class: if you encounter a problem in your assignments, spend 15 minutes troubleshooting the problem on your own. You can use of AI, Google, StackOverflow, etc. (although you cannot copy/paste code) for help. However, if after 15 minutes or so you still cannot solve the problem, ask for help to the instructional staff and your peers.

Asking questions is an important part of this class. Questions should be posted to [Ed Discussion](https://edstem.org/us/courses/29905/discussion/) in the appropriate category. 

## Tips to follow when posting questions

  * Before posting, search if someone else has posted the same or a similar question
  * Provide an informative title
    * not informative: "I need help!"
    * informative: "Getting a 'file not found error' when importing scotus.csv"
  * Use good manners (say Hello, thank you, re-read your comments before you post them, support your peers, etc.)
  * Post your attempt at solving the problem: share your code (use the code option on Ed with symbol "<>"), describe what you have already attempted, and post pertinent error messages
  * If you solve the problem, let us know (you can heart questions/answers you find useful!), and feel free to post your solution
  * Answer questions you feel confident answering to help out your peers 
  * Allow 24 hours to receive an answer (please understand that questions posted the day the homework is due might not receive a reply on time, and questions posted during the weekend might not get answered until the following Monday)
  
## Additional (encouraged) suggestions for posting

* Include a minimal, complete, and verifiable example (see [here](http://stackoverflow.com/help/mcve)) of the code you are using; this greatly helps us resolve your problem. You don't need to copy all the code from your program into the comment, but include enough code that we can run it successfully *until the point at which the error occurs*.
* Make sure you have pushed your recent commits to the GitHub repo. If it is up-to-date, we can look in or clone your repo to our machines to replicate the problem.
* Format your code snippets with `reprex` (see below)


## Using `reprex`

The [`reprex`](http://reprex.tidyverse.org/) package allows you to generate reproducible examples that are easily shared on GitHub with all the proper formatting and syntax. Install it by running the following command from the console:

```r
install.packages("reprex")
```
To use it, copy your code onto your clipboard (e.g. select the code and **Ctrl + C** or **⌘ + C**). For example, copy this demonstration code to your clipboard:






```
library(tidyverse)
count(diamonds, colour)
```

Then run `reprex()` from the console, where the default target venue is GitHub:


```r
reprex()
```

A nicely rendered HTML preview will display in RStudio's Viewer (if you're in RStudio) or your default browser otherwise.

{{< figure src="reprex-output.png" caption="Output of `reprex()`" >}}

The relevant bit of GitHub-flavored Markdown is ready to be pasted from your clipboard:


````
``` r
library(tidyverse)
count(diamonds, colour)
#> Error in `count()`:
#> ! Must group by variables found in `.data`.
#> ✖ Column `colour` is not found.
```

<sup>Created on 2024-06-05 with [reprex v2.1.0](https://reprex.tidyverse.org)</sup>
````

Here's what that Markdown would look like rendered in a GitHub issue:


``` r
library(tidyverse)
count(diamonds, colour)
#> Error in `count()`:
#> ! Must group by variables found in `.data`.
#> ✖ Column `colour` is not found.
```

<sup>Created on 2024-06-05 with [reprex v2.1.0](https://reprex.tidyverse.org)</sup>

Anyone else can copy, paste, and run this immediately. The nice thing is that if your script also produces images or graphs (probably using `ggplot()`) these images are automatically uploaded and included in the issue.

Note: to ensure your example is a reproducible example, you need to make sure to load all necessary packages and data objects at the top of your copied code. This may involve opening a new tab in the editor panel and writing a short version of the script that only includes the essentials, then copying that script to the clipboard and `reprex()` it.




Sometimes problems are caused by using older or incompatible versions of packages. The `session_info()` function in the `sessioninfo` library will print a list of all active packages and their respective versions. Include this in your post so we know which versions of packages you are using by setting `si = TRUE` in the `reprex()` function, like this: `reprex(si = TRUE)`.


## Acknowledgments

* ["How do I ask a good question?" StackOverflow.com](http://stackoverflow.com/help/how-to-ask)
* ["How to Ask Programming Questions," ProPublica.com](https://www.propublica.org/nerds/item/how-to-ask-programming-questions)

* This page has been developed starting from Benjamin Soltoff’s “Computing for the Social Sciences” course materials, licensed under the CC BY-NC 4.0 Creative Commons License.
