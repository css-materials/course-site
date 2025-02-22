---
date: "2024-09-28T00:00:00-05:00"
draft: false
weight: 70
title: "What are Git & GitHub?"
toc: true
type: book
---



Git and GitHub are powerful tools for managing and sharing your work and code. They are often used together, but they are not the same thing: [Git](https://git-scm.com/) is a version control system, [GitHub](https://www.github.com) is a cloud-based hosting service that lets you manage your Git repositories. 

Keep reading to learn more about them, and see the book [Happy Git and GitHub for the useR](https://happygitwithr.com/big-picture) for further info. 

## Git is a version control system

Git is a version control system used *to tracks changes in a project over time* so that there is always a comprehensive, structured record of that project. Each project is stored in a *repository* containing all files that are part of the project, which, for social scientists, include not just scripts but also data files, reports, and source code.

Why using Git?

In this course (and in your own work), you will be writing lots of programs. Generally the first draft is not the final draft, be it a research paper or a computer script. We want a way to track our changes over time. Perhaps this is to make sure we have a record of what we've already done that doesn't work, so we can avoid doing it again. Or maybe we want to share our code with collaborators who are working on a project with us. How can we do this?

One potential solution is to email copies of files back and forth as we make changes. But if we do this, we risk having lots of versions of files floating around. How do we know which is the most recent? What happens if someone edits a file and forgets to email it to us? How will we make sure all the changes are merged into the final version?

Or perhaps instead we can do all of our work on a cloud-based storage solution such as [Dropbox](https://www.dropbox.com) or [Google Drive](https://drive.google.com). This ensures changes are synchronized between computers. But they are not specifically designed to share code, and we won't always know who made what changes to a file. And what happens if two people want to work on the same file at the same time? One person will have to wait for the other to finish before they can edit that file. Plus how will we track previous versions of the file? Dropbox and other cloud storage services have some [version control solutions](https://www.dropbox.com/en/help/113), but these are not comprehensive or only store versions for a limited time. Plus every time we save a new version of the program, the entire file has to be retained. On large projects, this will eat up storage space quickly.

We want a solution (Git!) that:

* Keeps old versions of files indefinitely. Since all these versions are stored, we can always go back and see who modified the file and what changes they made. Or if we make a mistake in the future that breaks the program, we can revert back to an older version to fix it.
* Since we know who modified each file, if we have questions in the future we can go to that person with our questions.
* When collaborating with multiple people on the same project, and when code is involved, we want any changes made by project members to be integrated to the most recent version. If I try to modify a file and don't incorporate another member's revisions, I need to be told there is a conflict so I can merge all the changes.


## GitHub is a hosting service

GitHub is a cloud-based hosting service that *hosts and lets you manage your Git repositories*. See [GitHub on Wikipedia](https://en.wikipedia.org/wiki/GitHub) for more. 

Although Git and GitHub are often used together, you *do not need GitHub to use Git*:
* Git can be used locally by you on a single computer to track changes in a project. You do not need to be connected to the internet to use Git, and you do not need GitHub to use Git. But GitHub allows you to save your repositories online and share your work with a larger audience (you can host public or private repositories there) 
* You could put your Git repositories somewhere else online: GitHub is not the only option to host and mange Git repositories, but its the most popular one. Alternatives include Bitbucket, TaraVault, GitLab, etc. 

Professionally, you should know how to use Git and GitHub to manage projects and share code. This is why we will use Git and GitHub to host our course site, share code, and distribute/collect assignments.


<!--
{{< figure src="https://imgs.xkcd.com/comics/git.png" caption="[*Git* by xkcd](https://xkcd.com/1597/)" >}}
-->

## Acknowledgments


* This page is derived in part from ["UBC STAT 545A and 547M"](http://stat545.com), licensed under the [CC BY-NC 3.0 Creative Commons License](https://creativecommons.org/licenses/by-nc/3.0/).

* This page is derived in part from ["Version Control with Git"](http://swcarpentry.github.io/git-novice/), licensed under the [CC BY 4.0 Creative Commons License](http://swcarpentry.github.io/git-novice/LICENSE.html).

* This page has been developed starting from Benjamin Soltoff’s “Computing for the Social Sciences” course materials, licensed under the CC BY-NC 4.0 Creative Commons License.
