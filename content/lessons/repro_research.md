+++
title = 'Reproducible Research'
date = 2024-01-17T16:03:06-05:00

+++
### Motivation and Rationale

If you are going to take the time to build computational tools for humanistic research, you want others to be able to reproduce what you did. You want others to be able to verify your results, but also to use the tools you built to further their own projects.

Reproducible research may be an unfamiliar concept to many humanists, but its motivation in the Digital Humanities is to ensure that other people will be able to use and modify the computational tools you have taken the time to build. Reproducible research is motivated by several questions:

- Will others be able to run my code?
- Will others know that my code works and does what I say it does?
- Will others be able to adapt, modify and contribute to my code?

There are several factors that contribute to producing reproducible research. They include:

- Well-organized projects that others can understand
- Using a version control system to facilitate collaboration on the project
- Recording your environment so others can run your code on their machine

### Organizing your project

Your project will involve a number of components. This may include raw data, processed data, documentation, source code, and code for dependencies. You may be working as part of a team, or you may be writing code that others will use in the future. In either case, your project should be organized so that someone unfamiliar with the project can quickly find the information they need, whether these are datasets or functions in your code. In order for your research to be reproducible and make sense to others, you should organize your project in a consistent, predictable way.

##### File structures and directories

[This lesson](https://coderefinery.github.io/reproducible-research/organizing-projects/) from Code Refinery has some recommendations about you might choose to organize your project. The important points for humanist researchers are the following:

- Each project should have its own folder
- The structure of your project should be consistent. Another researcher should be able to understand your file structure without you explaining it to them.
- Your project should have a README file that explains how to run the project on a different machine.
- Different parts of the project should be in different files and/or directories.

Your project organization might look something like this:

```
impressive-project/
├── README.md
├── data/
|  ├── README.md
|  ├── metadata.csv
|  └── texts/
|     ├── book_a.txt
|     ├── book_b.txt
|     └── ...
├── data-processing/
├── plots/
├── tests/
├── doc/
│   ├── index.rst
│   └── ...
├── LICENSE
├── requirements.txt
├── package.json
└── package-lock.json
```

By using a clear organizational structure like this one, someone unfamiliar with your project will quickly be able to understand what your project is doing and how they might go about reproducing your work or building upon it for their own purposes.

##### Workflow

To get the results from your project, you will run multiple steps. This may take a haphazard or intutitive form which may be difficult for others to understand:

![xkcd comic on helping older adults troubleshoot their computer problems](https://imgs.xkcd.com/comics/tech_support_cheat_sheet.png)

[This CodeRefinery lesson](https://coderefinery.github.io/reproducible-research/workflow-management/) provides several strategies for recording your workflow. Here are some important considerations for humanists.

###### Manual workflow

A manual workflow might mean writing several discrete functions to perform each task. You may then run each function as needed from the command line or as part of a script. This may be useful for tasks you do not need to run very often. For instance, if you were trying to find the most frequently occuring words in a single book, this workflow might make sense. It may also make sense in more experimental projects where you want to spend time analyzing the output at each stage.

However, for large projects, this may become unwieldy. Imagine trying to analyze 500 books. Or imagine trying to OCR, clean, analyze, and graph an entire run of a 18th century newspaper. In these cases, a manual workflow would take too much time and be too prone to error.

###### Scripted workflow

When dealing with large amounts of data, tasks you need to run frequently, or tasks you want to automate for others to run, it makes sense to turn towards a scripted solution. The [CodeRefinery lesson on workflow management](https://coderefinery.github.io/reproducible-research/workflow-management/) provides examples of using Bash or Snakemake to automate your workflow. Here is the same example reproduced in python:

```
#to-do: write out this example
```

###### Recording your workflow

Regardless of how you organize your workflow, you should provide clear documentation for others to reproduce your steps.

Your project should include a README that provides clear instructions for running each step in your workflow. The README should also contain information about installation and the type of data required for the project.

You may additionally want to provide a graphical representation of your project's workflow. This can help others see how the pieces fit together, and may also explain what each function in your workflow does.

TO-DO: Find suitable visualization of a workflow.

##### Additional resources

_This list is still under review._
- Project organization:
  - [Python package structure](https://py-pkgs.org/04-package-structure)
  - [Basics of Packaging Python Programs](https://kyleniemeyer.github.io/research-software-dev-modules/module-packaging/)
- Workflow management

### Environments

#### Building your Environment

When creating a digital project it is important to know what underlying software, platforms, libraries, code, etc. we are utilizing. By keeping track of these elements we can make sure that our future work and that of researchers that build upon our efforts can execute our codes.
But this can be a very time-consuming task especially when it is not built into the workflows that we may already use in our day-to-day practices. For this very reason, we can utilize containers that exist to help you standardize and be able to distribute your environments. 

##### Lesson - Containers
[_Code refinery container Lesson_](https://coderefinery.github.io/reproducible-research/environments/)

But it is not enough to just utilize already tested environments or possibly package our own. We need to also track our __dependencies__ as they get __increasingly__ complicated as this next picture illustrates perfectly. 

![dependency image](https://coderefinery.github.io/reproducible-research/_images/python_environment.png)

> Dependencies are the underlying software, libraries, platforms, etc. on which something (*can be a library, tool, code*) you are using relies upon.

For example, if you are using the package _scipy_ you need to have _python_ and _pip_ on your environment already. In this case, _python_ and _pip_ are your __dependencies__. To track these dependencies we can utilize package managers which organize the environments and track the dependencies for us. 

##### Lesson - Dependencies
[_Code Refinery dependency lesson_]("https://coderefinery.github.io/reproducible-research/dependencies/)


##### Additional resources
- Common container software intro lessons and/or docs:
  - Docker
      -  [Carpentries lesson](https://carpentries-incubator.github.io/docker-introduction/)
      -  [Matthew Feickert Lesson](https://matthewfeickert.github.io/intro-to-docker/)
      -  [Official Intro Docs](https://docs.docker.com/get-started/)
  - Singularity (very useful for High-performance Computing work)
      -  [Carpentries lesson](https://carpentries-incubator.github.io/singularity-introduction/")
      -  [Singularity Intro Docs](https://carpentries-incubator.github.io/singularity-introduction/)

- Common dependency managers intro lessons and/or docs:

+++
