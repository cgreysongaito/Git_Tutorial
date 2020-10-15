Git and GitHub with Rstudio
=============

This repository was created for a tutorial provided by Christopher J. Greyson-Gaito for the R User Group in the Integrative Biology department of the University of Guelph. The text below is the guide for the tutorial.

Prerequisites
=============

-   Install Git ([Windows](https://git-scm.com/download/win),
    [Mac](https://git-scm.com/download/mac),
    [Linux](https://git-scm.com/download/linux))

-   Register for [GitHub](https://github.com/join?source=header-home)

Benefits of Git and GitHub
==========================

-   **Git**

    -   Version control your R scripts and your manuscripts

        -   All of your edits are saved and so you can go back to any
            edit that you have made.

        -   Collaborating is very easy with git and GitHub. All of
            the edits made by collaborators can be seen.

        -   You can tag different versions and easily go back to a
            previous version.

        -   You can experiment with your coding without worrying about
            breaking the original code.

-   **GitHub**

    -   Collaboration

        -   If there is useful code already written, you can copy the code
            from GitHub and use the code (as long as you cite the code)

        -   You can collaborate with fellow scientists on R scripts or on
            manuscripts (doable with .docx, easier with .tex/.md)
            
    -   Publish your R scripts for your published papers (see [Monica
        Granados R script for published
        paper](https://github.com/Monsauce/Food-web-modules-and-individual-growth-rate)
        for an example)

Basics of Git (Conceptual)
==========================

To explore Git we will go through
[TryGit](https://try.github.io/levels/1/challenges/1) together.

Other useful webpages on how git works:

[Workflow of version control](https://www.git-tower.com/blog/workflow-of-version-control)

[Intro to Git with RStudio](http://r-bio.github.io/intro-git-rstudio/)

[Git Tutorial](http://nyuccl.org/pages/gittutorial/)

[Git and R](https://nicercode.github.io/git/)

- **Graphical Git Client**
  - [Git Tower](https://www.git-tower.com/)
  - [Tortoise Git](https://tortoisegit.org/)
  - [GitKraken](https://www.gitkraken.com/)
  
- **The Command Line**
  - [Git Manual](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics)

R scripts on GitHub for published papers (your homework :) )
============================================================

Before you send your manuscript to a journal, your r script should be
published. The great thing about Git and GitHub is that if your
reviewers want you to change your analysis, you can change your r script
and republish it and people can see those changes (open and transparent
science!).

1.  When your r script is ready (and you have just done your final
    commit to your local repository), login to GitHub and create a new
    repository (by clicking on Repositories and New). Follow the instructions in GitHub to create the repository.

2.  In the new repository on GitHub, click on the “Clone or download" button. Ensure that the box that appears has the title "Clone with SSH". If the box does not say this then click on "Use SSH".

7.  Copy the text that appears (e.g
    gitgithub.com:cgreysongaito/RUserGroup\_Git.git).

3.  In RStudio, click on Tools -> Shell and type in the Shell:
    git remote add origin &lt;text you just copied (without the &lt;>)>
    and press enter

4.  Now type: git pull origin master --allow-unrelated-histories (and press enter). NOTE Never use the option --allow-unrelated-histories unless you are merging a new and completely empty (except for a license) GitHub repository with your local repository. This option is a dangerous option if used without care.

5.  Now type: git push -u origin master (You must do these pulls and pushes in the shell first before using the RStudio git buttons. This is because RStudio at first can not pull or push your work. What you entered into the shell now allows RStudio to push and pull.)

You have now published your R script. A nice feature of git is to tag a
commit with a version number. This is useful for reviewers and other
people to see where your different versions are (and in your citation
for the published r script you can give a version number).

To add a version number:

1.  Open the R project that you want to publish

2.  Click on Tools -> Shell and type: git tag -a &lt;version
    number here> -m “any message here"

3.  Push your repository to GitHub using RStudio

4.  Unfortunately, RStudio does not automatically push tags. Therefore,
    in the shell type git push origin --tags

More information on tagging can be found
[here](https://git-scm.com/book/en/v2/Git-Basics-Tagging).

Other useful links for RStudio and GitHub:

[Using SSH with RStudio and GitHUb](https://www.r-bloggers.com/rstudio-pushing-to-github-with-ssh-authentication/)

[RStudio and GitHub](https://www.r-bloggers.com/rstudio-and-github/)

Licenses
========

It is very important that you include a license for anything you publish
on GitHub (to protect yourself and to help people understand what they
can and not use). Your best bet is probably to use a [Creative Commons
Attribution Share-Alike
license](https://creativecommons.org/licenses/by-sa/3.0/deed.en).

Here are a few links to help you choose a license and to put the license
into your GitHub repository.

[Choose A License](https://choosealicense.com/)

[GitHub Help: Licensing a Repository](https://help.github.com/articles/licensing-a-repository/)

[Creative Commons Licenses](https://creativecommons.org/licenses/)

