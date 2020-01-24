---
layout: home
title: Computing
category: Guides
permalink: /computing/
---

# Mac Setup

This document provides a guide on setting up your Mac for working within the Materials Virtual Lab.

## Step 1 - Preparing your Mac

You will first need to download and install basic compilers:

1. Xcode – This provides the gcc compiler. Install it from the App Store.
2. Xcode command line tools - After installing XCode, type the following in a terminal:

```shell
xcode-select --install
```

## Step 2 - Git and Github

Create a Github account if you do not have one. Then add your ssh key (in `$HOME/.ssh/id_rsa.pub`. If it does not exist, create one using the `ssh-keygen` command) to your Github account under settings.

Follow the instructions on this page https://help.github.com/articles/set-up-git.

## Step 3 - Install Miniconda

Conda is a package manager that makes it a lot easier to work with different python versions and packages. After downloading the miniconda installer, run the following in a terminal in the directory where you downloaded the installer:

```shell
curl -o Miniconda3-latest-MacOSX-x86_64.sh https://repo.continuum.io/miniconda/Miniconda3-latest-MacOSX-x86_64.sh
bash Miniconda3-latest-MacOSX-x86_64.sh -b
```

Now, you should start a new terminal before proceeding.

Afterwards, install [homebrew](http://brew.sh). This will make life a lot easier.

```shell
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

## Step 4 - Install Python 3.7+

Install the latest copy of Python > 3.7, even though your Mac should already have a compatible version. Python 3+ is mature enough that we are going to work with this from now on. Do the following:

```shell
conda update python
```

Verify your python version by typing `python --version` in a terminal.

## Step 5 (Optional) - Isolated environments

Conda provides the means for you to create isolated environments. It is useful if you are going to work with lots of python packages that may have incompatible dependencies. If you are planning to work exclusively on Materials Virtual Lab stuff, you can skip this step.

To create a new environment in conda, do

```shell
conda create -n my_env python
```

If you want to use python 2.7 for testing, type

```shell
conda create -n my_env python=2.7
```

To go to that environment, just type:

```shell
source activate my_env
```

## Step 6 - Install numpy, scipy and other packages

These must be installed first as they are needed to compile the other packages. Use the conda versions as these will have Intel MKL, which is faster.

```shell
conda install --yes numpy scipy matplotlib jupyter git pandas sympy
```

Start a new terminal before continuing.

## Step 7: Clone and setup the relevant Github repos

Before you setup the repos, it is generally advised that you keep all your repos in a single directory, e.g., $HOME/repos. Many of MAVRL's useful scripts assume this as the default location for your repos.

### Pymatgen, pymatgen-db, custodian, fireworks

These are to be installed in developmental mode from source. You will be working with and modifying these a lot.

```shell
git clone git@github.com:materialsproject/pymatgen.git
cd pymatgen
python setup.py develop
```

Do the same for the pymatgen-db, custodian and fireworks repos.

### Pymacy (pronounced primacy)

To be installed in developmental mode from source. You will be working with this a lot as well. This is the private overall repo for the MAVRL.

```shell
git clone git@github.com:materialsvirtuallab/pymacy.git
cd pymacy
python setup.py develop
```

## Step 8: VASP Setup

You need the VASP psuedopotential files in order to generate VASP input files. These are provided in the pymacy repo under resources.

Add a VASP_PSP_DIR to your .pmgrc.yaml, by running the following.

```shell
pmg config --add PMG_VASP_PSP_DIR /path/to/pymacy/resources/VASP_PSP
```

Test that you have set it up correctly by typing:

```shell
python -c 'from pymatgen.io.vasp import Potcar; print(Potcar(["Li_sv", "O"]))'
```

There should be no errors. Otherwise, you have not done setup correctly.

## Step 9: IDE (Optional if you are good)

An Integrated Development Environment (IDE) makes it easier for you to code and maintain good style, especially for Python. Note that for group members, it is highly recommended you use an IDE unless you believe yourself to be a superior Python coder to your adviser (and have the goods to prove it).

Download the [community version of Pycharm](http://www.jetbrains.com/pycharm) or install it via `brew cask install`.

```bash
brew cask install pycharm-ce
```

It is unlikely you need anything more than the community version.

## Step 10: Familiarize yourselves with git, python and pymatgen

Learn how to commit and push changes with git. The model is that you should be creating branches for anything that you do, and you should *commit often*.

Pymatgen has extensive documentation at http://pymatgen.org. Read and learn to use it. A hour spent figuring out how to work with pymatgen will save you 100 hours over a year (and probably more as you become more familiar).

Read the materialsvirtuallab Coding guidelines, and follow them strictly.

## Step 11: Other recommended software

Here are some recommended software. Most can be installed via homebrew via `brew install` or `brew cask install`.  Note that you can use `brew cask install` to install many GUI apps, including Google Chrome
(google-chrome), Zoom (zoomus), etc. You can look for apps using `brew cask search`.

* [Atom](https://atom.io/) editor: General purpose text editor for many languages, including python and latex. Make sure you install the relevant language support package for latex if you plan to use it.
  ```bash
  brew cask install atom
  ```
* iTerm2: A much better replacement for Terminal.
  ```bash
  brew cask install iterm2
  ```
* Alfred: Fast program launcher.
  ```bash
  brew cask install alfred
  ```
* Mendeley: Citation manager. This is not optional.
  ```bash
  brew cask install mendeley-desktop
  ```
* VESTA: For viewing crystal structures.
  ```bash
  brew cask install vesta
  ```
* coreutils: GNU version of core utilities like ls, etc., which are more updated
  than the version that Mac comes with.
  ```bash
  brew install coreutils
  ```
* tree: Directory exploration tool.
  ```bash
  brew install tree
  ```

# Backup

All MAVRL group members are required to backup their personal computers as well as data. There are two forms of backup that you will need to do:

* Backup of personal computer via Crashplan. The group provides an unlimited backup through CrashPlan Pro. After your initial setup, backup is the first thing you should setup. Please contact Backup Manager (see Group jobs) for invitation letter and follow signup instruction for your backup account setup. The cloud console login website is: https://web-ebm-msp.crashplanpro.com/console/login.html. Please refer to the attached Crashplan online manual for detailed backup instruction.
* Backup of calculation data at mavrldata storage server. We have our own large capacity file storage server at mavrldata.ucsd.edu. Please contact the Data Manager (see Group jobs) for an account). All calculation data that are too large or unnecessary to fit on your laptop should be backed up to mavrldata using scp or rsync. Mavrldata has RAID redundancy as well as its own backup system to ensure your data is safe.

Unless it is bad or irrelevant data, **do not throw data away**, even after you finish a project. Organize your data on your laptops and mavrldata carefully.
