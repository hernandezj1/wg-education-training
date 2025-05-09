---
title: "Git & GitHub"
subtitle: "subtitle"
author: [Julia Damerow, Fernanda Freire]
date: "2024-05-09"
subject: "Version Control"
keywords: [Git, GitHub]
doi: doi/1234
lang: "en"
...

# Git and GitHub

In this lesson, we will talk about version control with Git and GitHub. Some of you might have already heard about it or even used it. Git is a very popular version control tool mostly used by developers but it can very well be applied to non-coding projects as well! You could use it to write a paper or to manage your dataset. If you do develop code, however, you should not live without Git or another version control system. There are several other version control systems such as Mercurial and SVN but Git is the most used in research. In the international research software engineer survey from 2022, Git was used by [93.75% of all survey respondents](https://softwaresaved.github.io/international-survey-2022/section/good-practices/#use-of-version-control).

But what are version control systems? Version control systems are systems used for tracking changes in files. They allow multiple users to collaborate on the same project in parallel, maintaining the integrity of the files and avoiding overwriting each other’s work. They offer features such as maintaining a history of the changes, being able to revert to previous versions, and merge different versions of the same file. 

Git is a piece of software originally developed by [Linus Torvald](https://en.wikipedia.org/wiki/Linus_Torvalds) that you install on your computer to version your files. GitHub, in contrast, is a cloud-based service used for hosting and managing Git repositories. It provides a series of collaborating tools that allow for different access permissions for collaborators, issue tracking, feature requests, documentation, and several other features.

If you want to know more about why using Git and GitHub is useful, check [this page](https://coderefinery.github.io/git-intro/motivation/).

To start out, you should first work through one or both of the following Git tutorials.
- Software Carpentries Git Tutorial: [Version Control with Git ](https://swcarpentry.github.io/git-novice/)
This tutorial is fairly detailed in the descriptions and walks you through an example project with Wolfman and Dracula.
- Code Refinery Git Tutorial: [Introduction to version control with Git](https://coderefinery.github.io/git-intro/)
This tutorial offers a hands-on approach to learning how to work with Git, with exercises and examples but with a little less text.

Getting used to working with Git and Github can be a bit confusing in the beginning, but don’t be scared: in our FAQ section, we selected a series of common questions and problems you might have in your journey alongside short explanations and useful links. If you have questions that are not included in our FAQ, [write an issue in our repository](https://github.com/dh-tech/wg-education-training/issues) so that we can include it.
Git and GitHub work with a specific vocabulary to describe its functionalities and processes. In our glossary below you can find a short description of the most common actions involved in the version control workflow of Git and GitHub. 

# Glossary

## Clone

In version control, to clone is an action used to make a copy (or clone) of an existing repository while maintaining a reference to the original (copied) repository.

## Stage

In version control, to stage is an action that selects a group of changes to be recorded through a commit. This means that not all changes performed are automatically included, and therefore recorded, in a new commit.

## Commit

In version control, to commit is an action used to record the current state of a repository.

## Push

When working locally on a copy of a repository hosted remotely, the changes that are carried out and commited need to be sent from the local copy to the remote repository in order to be applied. This process of transfering the commits from a local to a remote repository is called push.

## Pull 

When several collaborators are working together on a repository hosted remotely, it is very likely that they will work localy on copies of the repository and regularly transfer their commits to the remote repository through pushes. What happens when the remote repository goes through changes implemented by another user? You need to update your local copy to include these changes. The process of downloading the content of a remote repository and immediately updating the local repository to match the updated content is called pull.

## Fetch

To fetch is an action that downloads the content of a remote repository while not integrating any new or changed content into your local copy of that repository. Fetching a remote repository gives the user an overview of the implemented changes that this repository has undergone while not directly implementing them to the local data.

# FAQs

## What’s the difference between fetch and pull?

When you fetch a branch, you copy the changes that exist in the remote repository into your local repository. However, you will not see these changes when you look at the files because the changes will only be in your local repository not in your working directory. To see the latest changes, you will need to pull.

# Resources

- [Wikipedia entry about Git](https://en.wikipedia.org/wiki/Git)
- [Software Carpentries Git Tutorial](https://swcarpentry.github.io/git-novice/)
- [Code Refinery Git Tutorial](https://coderefinery.github.io/git-intro/)

