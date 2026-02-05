# CEDEP Github

# Github Overview

Github is a widely used tool for managing work and development on
code-based projects. It has several key features:

1.  Version control - Github is based on **git**, a version control
    software. Git allows you to track changes in a project over time,
    and revert to previous versions if problems arise. You can also
    create **branches** of a project to work on new/experimental
    features without breaking the **main** code which might need to
    remain functional with no downtime. After completing the branch, the
    changes can be merged into the main code.

2.  Versatile - You can use Github to collaborate and track changes for
    any text- or script-based project. It is mostly used for hosting
    codes for web/software development or data analysis (SQL, SAS, R,
    Python), but you can also use it for complex [documentation on
    sourdough bread
    making](https://github.com/hendricius/the-sourdough-framework),
    [data storage for public
    use](https://github.com/sfu-db/covid19-datasets/tree/master), or
    [reports on cyber-security
    threats](https://github.com/jacobdjwilson/awesome-annual-security-reports).

3.  Web hosted - Github is a web application that can host public and
    private **repositories** (or **repos**). Anyone can see and download
    information on a public repo. Private repos can only be seen by
    individuals with approved access. For our purposes, <u>no sensitive
    code, PHI, passwords, tokens, or credentials can be stored in any
    repository, even if it is private.</u> Github is great for working
    on projects for your own use, but it is also a fantastic way to
    share code with other users inside and outside TDH who might find it
    useful.

4.  Free - Anyone can create a free Github account. To interact with TDH
    repos, you should create your own account using your tn.gov email
    and two-factor authentication. We can then add you to any TDH CEDEP
    teams in Github, so you can start contributing.

## Organization

Our use of Github was only recently approved, so we are still working on
the best way to integrate it into our teams. We have one main
organization, TDH-CEDEP, with several program area subgroups (e.g., SSI,
VH). Once you have your account, an admin can add you to the correct
group(s). You will be able to view/download any public repository, but
you can only see the private repositories for the teams you are a part
of. You can also only make changes to repos for your teams.

If your program area does not have a team in TDH-CEDEP, let us know and
we can create one easily. If you plan on having a lot of users and
repos, it would be good to designate someone on your team to be an
admin, so they can manage access permissions.

## Security

The following steps should be closely followed in order to adhere to our
agreed upon security protocol with STS:

1.  Use your tn.gov email with two-factor authentication when setting up
    your Github account.

2.  Admins must promptly remove access permissions from users who leave
    CEDEP or transition between teams. They should also perform regular
    user audits.

3.  Only use Github for projects that need it. You can use Git locally,
    if you just need version control.

4.  Keep repositories private unless the project needs to be viewable by
    other jurisdictions and/or the public.

5.  Teams should develop and follow protocols to ensure that no
    sensitive data is published to any repos, public or private. See the
    security page for more details.

# Security Details

STS took a lot of sweet talking before they approved our Github use, so
we want to be on our best behavior (in addition to general data security
concerns). As such, the following practices should be followed when
using Github (expanded from the summary on the first page).

## Account Setup

Use your tn.gov email to create a personal account (can we use our
existing account and add our tn.gov email?). Enable two-factor
authentication for increased security. You will be able to contribute to
your own teams repos using your own account. <u>\[section on hosting
your own repos on your own account\]</u>

## Team Access

Admins for the TDH-CEDEP organization must maintain user access to the
correct teams. This includes adding new members to the correct team,
removing team members when they leave their positions, and performing
regular user audits.

## Do you even need Github?

If you just want version control on a project, you can just use Git
locally. Github is great for sharing projects and working with outside
parties, but if the process is internal, there might not be a point to
hosting it on Github at all.

## Public vs Private Repositories

The default choice for repositories should be to make them private. More
public repos are just more ways for things to accidentally get published
to the public. That being said, there are reasons why you might want a
repo to be public. Public repos are great for sharing data and code with
other parties, and even having them suggest improvements. You can even
publish data packages that are useful for TDH employees who might not
have their own Github accounts.

It is important to note, that a repository being private should not
affect the sort of information published there. PHI, passwords, etc. are
not allowed in any repo, public or private. 

## Sensitive Data

The following data are not allowed to be published to any Github
repository:

- PHI

- Non-public data (preliminary, data needing suppression, etc.)

- Usernames/Passwords/Credentials

- API tokens

In order to prevent this data from getting into Github, remove it from
your codes and become used to excluding it from your work without
consideration for if it will end up in Github. It is especially easy to
leave notes or comments in code about test cases or outliers that might
need to be deleted before saving a file.

You can also use gitignore functionality to hide certain files from Git,
which can help when you need data for a code to run on your machine, but
you don’t want it in the version history that goes in Github.

\[Consider a middle tier of info that can be in private but not public
repos\]

### Removing Sensitive Data from a Repo

If sensitive data gets pushed to Github, we need to take it down as fast
as possible. Follow the following steps:

1.  Notify an admin

2.  Make the repository private (if it isn’t already)

3.  Edit the repo to remove the sensitive data

4.  Edit the version history to remove the sensitive data \[develop
    guidance because this can be complex\]. Note information needed for
    follow-up investigation (time published and removed, author, file
    source, etc.)

5.  Notify anyone else who needs to know (e.g., HIPAA protocol)

6.  Determine steps to make the repo public again (if appropriate)

# Github Basics

This section covers the basics of how Github works. There are a lot of
resources online that can also help you understand. Github is a website
that is based on Git. Git is a common version control software.

## What is Git

Git was developed to track changes in software over time, with multiple
people working on the same code at once. You can download Git onto your
PC and use it without worrying about Github at all. The diagram below
shows how a project is developed using Git version control.

![](https://www.nobledesktop.com/image/blog/git-branches-merge.png)

The project starts in an initial state, called the main (sometimes
master) branch. In the diagram above, the main branch is colored green.
Each circle is the code at a point in time, referred to as a commit.
When a change is made to the code, you must choose to commit the change
to the version history. You will also be asked to write a short
description of what you changed or added. Uncommitted changes are
considered staged, since they are waiting to be accepted or rejected.

For minor fixes, like correcting a typo, you could edit the main branch
of code and commit the changes to it directly. But sometimes a change is
more involved, and working on it will take time. Furthermore, sometimes
you need to make changes to the foundations of a script that render it
non-functional, but other people rely on the code to keep running. In
this case, Git allows you to create a branch (in blue and orange above).
Branches are a copy of the code that is separate from the main,
functional code. You can then make edits to your branch without breaking
the functional code. When you have finished work on the branch, you can
then merge your changes into the main branch. In the diagram above, the
blue branch took three commits to finish, whereas the orange commit only
took one.

When making a commit, or merging a branch into main, you will have the
opportunity to review the old version of the code and the new version.
This is so each change is highlighted and looked over before it is added
to the version history. The above process allows for complex projects
with several contributors to be developed with a clear history of who
did what and when, with the ability to go back to previous versions of
the project, if need be.

A Git project can consist of one or more files that are located together
in a folder. This location, and the files in it are known as a
repository, or repo. All the files and subfolders in the repo are
included in the project’s version control. Git can be used by typing
commands into a terminal or command prompt, but other tools (Github,
Rstudio, etc.) provide a user interface that can make getting started
easier.

Here are the key terms from the description above:

- Version control - Tracking, recording, and organizing changes to a
  project over time

- Git - a version control software

- Main - The base version of a project

- Branch - a copy of the main project, where changes can be made

- Staged Change - an edit to a file in a repo that has not been
  committed

- Commit - Officially adding a change to the version history (to the
  main project, or to a branch)

- Merge - Adding changes from a branch back into the main project

- Repository - A location that contains the files and folders that make
  up a project

## What is Github

As stated above, you can use Git locally on your own computer. In this
case, you are working on a local repository, or a project on your own
computer. Github is a remote repository; a place to store the code that
is not your own computer. This allows the code, with all its version
history, to be available to everyone (a public repo), or github users
with certain permissions (a private repo).

You can take an existing local Git repository and push it up to Github.
Most code editors can easily integrate with Git and Github, to
facilitate communication between your local repo and Github’s remote
repo. After working on some changes to the code and making one or more
commits, you can push the changes up to Github (syncing the Github repo
to align with your local repo). Conversely, you can pull the current
version of the project from the Github repo to your own local repo in
order to make changes off of it. This is useful for projects with
multiple collaborators. You will typically all use Github as the hub for
development; pull down the current version of the project with the most
recent changes from others, make and commit your changes locally, then
push them back to Github. Then others can do the same.

![](images/local_and_remote_repos.png)

Pulls and pushes happen to branches of a repository, but you should
start off by working on a small project with only a main branch. Here is
an example of the code review panel in R for a small documentation
change:

![](images/commit_review_R.png)

Here are the key terms from the description above:

- Local Repo - A group of files and folders that make up a project,
  stored on your own computer

- Remote Repo - A repo stored on a remote server, like Github

- Pull - Copying a remote repo from Github to a local repo on your
  machine

- Push - Updating a remote Github repo to reflect commits made to your
  local repo

## Common Elements of a Repo

Many different file types can be placed into a repo, but there are some
items which are commonly used to make working with Git/Github easier.
None of these are strictly required (except for a license, potentially),
but you should use them.

### Readme

A file that explains the purpose of the project, and any useful
documentation on how to use the code inside. In Github, readme files
should be markdown documents (i.e., readme.md). When structured this
way, the readme information will be rendered in the Github repo.

### .gitignore

The .gitignore file allows you to specify files and folders that should
not be included in the version control tracking. These files can be
housed inside the repo folder, and could be critical to the functioning
of the code (e.g., important data for analysis), but changes to these
files are not tracked, and they won’t be pushed to Github. Specific
files can be listed in the .gitignore, or patterns that exclude multiple
items (e.g., all PDFs, all files with “PHI” in the name, all files in a
subfolder)

### Subfolders

The main folder of a repo can store files, but it can also help to
organize files into subfolders. Common subfolders are for data, scripts,
or images

### License

Since the code put into public repositories can be seen and copied by
anyone, you likely need a license that describes how the code can be
used by others \[what is the TDH default license? Does this need to be
mentioned in security?\].

## Credentials

You will need to link your computer to your Github account. Options
include:

- Git terminal

- Git UI \[maybe?\]

- IDE capabilities

  - RStudio - <https://usethis.r-lib.org/articles/git-credentials.html>

  - SAS -
    <https://communities.sas.com/t5/SAS-Communities-Library/How-to-connect-SAS-to-your-Git-profile/ta-p/772570>

  - VSCode

You should only need to set your credentials once \[pending security
concerns\]. Once set, any commits/pushes/pulls/etc. will include your
name, and you will have the ability to access private repositories for
your teams.

# Extra Resources

## Other Github Summaries

- <https://www.coursera.org/articles/what-is-git>

- <https://digital.gov/resources/an-introduction-github>

## RStudio Integration

- <https://happygitwithr.com/rstudio-git-github.html>

- <https://rfortherestofus.com/2021/02/how-to-use-git-github-with-r>

- <https://www.epirhandbook.com/en/new_pages/collaboration.html>

## SAS Integration

- <https://documentation.sas.com/doc/en/egug/8.3/p078cl08fol7hkn11a8nf1f9izq7.htm>
