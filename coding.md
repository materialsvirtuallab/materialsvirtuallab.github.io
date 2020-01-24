---
layout: home
title: Coding
category: Guides
permalink: /coding/
---

# Coding

The MAVRL is primarily a computation-based group, and coding new materials analyses or automation is a large part of what we do. This page is dedicated to outlining our philosophy and the various tools that we use. The good news is that plenty of resources have already been developed and they can make doing research a lot easier.

# Programming Languages

Python is used extensively in the group. It is highly recommended that you become familiar with the language and the scientific packages available (numpy and scipy are the major ones).

Matlab is also used, especially for generating publication quality plots and visualizations.

Other programming languages like Java, C or Fortran can be used if there are specific libraries available in those languages that are too much work to redo in Python, or if performance is of critical importance. It should be noted that properly vectorized calculations in numpy is often just as fast as in those in C or Fortran. If you need C or Fortran, it is further recommended that you use something like Cython, which provides an easier way to write C extensions and integrate into the existing Python code infrastructure in our group.

# Coding Philosophy

Unlike most other scientific groups, we place a great emphasis on developing proper software infrastructure. Proper software ensures that your scientific analyses is readily accessible to others both within and outside of the group, even years down the road. Investing the time to code properly brings benefits even in the medium term - so it is important that you do not sacrifice code clarity for short-term expediency. Here are some basic rules for developing good code:

* Document properly. Documentation should be clear and concise. Ideally, your code should also be self-documenting, i.e., variable and function names should clearly indicate their purpose.
* Follow best code style practices. For Python, follow the PEP8 style guide.
* Test, test and test. Write robust unittests to ensure that your analysis is correct. This is important as you do not want to publish incorrect results. Also, it allows you to finetune your code in future and check that everything is still working as it should. Verifying the results with just one or two pieces of sample data is generally not a good way to ensure that your analysis is correct. Refer to the unit tests in pymatgen (later section) to learn how to do it properly.

# Tools

We use several tools to facilitate our research.

* Github and git. Git is a content versioning system. What this means is that it helps you keep track of what changes you have made to a code or document, allowing you to go through the whole history of a document. The way this is done is by creating a repository (or repo). Github is a web service that hosts repos using git, allowing our group to work collaboratively on certain repos. Sign up for a free account on Github if you don't already have an account and ask to be added to the materialsvirtuallab organization.
* Pymatgen. Pymatgen is an open source materials analysis code started by Shyue Ping. It is a collaboration between our group, the Materials Project and many other groups. It is extremely useful as a starting point for more advanced analyses. You will also probably be contributing to pymatgen at some point during your research. Visit [pymatgen.org](pymatgen.org) to learn what you can do with it.
Working with Repos
* There is a good reason why certain packages are installed via conda / pip install and others are installed by cloning the git repos in the clusters. The former are things which you rarely need to change and / or you can’t change. The latter is code you will be working with extensively and may need to add / edit stuff. The main example is pymacy, but also pymatgen as well.
* You code in your own laptop / desktop. You do not edit code in the cloned repos in the clusters. Doing so creates a lot of inconsistencies.
* If you need to implement a new analysis or workflow, you push the new analysis or workflow to our Github repo. Then you do a update of the repos on the clusters to use the code on the cluster.
* In the TSCC, there is already an update_repos script in /projects/ong-group/bin. When you need to do an update, just simply type update_repos and all your repos will be updated to the latest version.
* If your new code is a major addition or change and can potentially affect currently running stuff, you create a branch, and then push the branch to the main Github repo. You then switch to the branch on the clusters to use your new analysis. Only when you are satisfied that it works, you then merge the new analysis into the master branch.
