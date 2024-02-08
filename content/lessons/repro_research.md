+++
title = 'Reproducible Research'
date = 2024-01-17T16:03:06-05:00

+++
## Motivation and Rationale

If you are going to take the time to build computational tools for humanistic research, you want others to be able to reproduce what you did. You want others to be able to verify your results, but also to use the tools you built to further their own projects.

There are several factors that contribute to producing reproducible research. They include:

- Well-organized projects that others can understand
- Using a version control system to facilitate collaboration on the project
- Recording your environment so others can run your code on their machine

## Organizing your project

Your project will involve a number of components. This may include raw data, processed data, documentation, source code, and code for dependencies. You may be working as part of a team, or you may be writing code that others will use in the future. In either case, your project should be organized so that someone unfamiliar with the project can quickly find the information they need, whether these are datasets or functions in your code. In order for your research to be reproducible and make sense to others, you should organize your project in a consistent, predictable way.

[This lesson](https://coderefinery.github.io/reproducible-research/organizing-projects/) from Code Refinery has some recommendations about you might choose to organize your project. The important points for humanist researhcers are the following:

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

## Workflow

To get the results from your project, you will run multiple steps. 

- include graphic or visualization
- discuss using python script to run workflow from project





### Environments

#### Building your Environment

When creating a digital project it is important to know what underlying software, platforms, libraries, code, etc. we are utilizing. By keeping track of these elements we can make sure that our future work and that of researchers that build upon our efforts can execute our codes.
But this can be a very time-consuming task especially when it is not built into the workflows that we may already use in our day-to-day practices. For this very reason, we can utilize containers that exist to help you standardize and be able to distribute your environments. 

##### Lesson - Containers
<a href="https://coderefinery.github.io/reproducible-research/environments/">_Code refinery container Lesson_</a>

But it is not enough to just utilize already tested environments or possibly package our own. We need to also track our __dependencies__ as they get __increasingly__ complicated as this next picture illustrates perfectly. 

![dependency image](https://coderefinery.github.io/reproducible-research/_images/python_environment.png)

> Dependencies are the underlying software, libraries, platforms, etc. on which something (*can be a library, tool, code*) you are using relies upon.

For example, if you are using the package _scipy_ you need to have _python_ and _pip_ on your environment already. In this case, _python_ and _pip_ are your __dependencies__. To track these dependencies we can utilize package managers which organize the environments and track the dependencies for us. 

##### Lesson - Dependencies
<a href="https://coderefinery.github.io/reproducible-research/dependencies/">_Code Refinery dependency lesson_</a>


##### Additional resources
- Common container software intro lessons and/or docs:
  - Docker
      - <a href="https://carpentries-incubator.github.io/docker-introduction/"> Carpentries lesson</a>
      - <a href="https://matthewfeickert.github.io/intro-to-docker/">Matthew Feickert Lesson</a>
      - <a href="https://docs.docker.com/get-started/">Official Intro Docs</a>
  - Singularity (very useful for High-performance Computing work)
      - <a href="https://carpentries-incubator.github.io/singularity-introduction/">Carpentries lesson</a>
      - <a href="https://docs.sylabs.io/guides/3.7/user-guide/introduction.html"> Singularity Intro Docs</a>

- Common dependency managers intro lessons and/or docs:

+++
