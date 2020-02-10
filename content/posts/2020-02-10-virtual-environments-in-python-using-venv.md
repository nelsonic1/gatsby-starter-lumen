---
template: post
title: 'Virtual Environments in Python Using Venv '
slug: virtual-env-in-python-using-venv
draft: false
date: 2020-02-10T01:47:24.648Z
description: >-
  How to initialize and use a virtual environment in Python using the built-in
  venv module
category: python
tags:
  - python
  - virtualenvironment
---
### What does a virtual environment do?
From the official python venv documentation:
>The venv module provides support for creating lightweight “virtual environments” with their own site directories, optionally isolated from system site directories. Each virtual environment has its own Python binary (which matches the version of the binary that was used to create this environment) and can have its own independent set of installed Python packages in its site directories.

Official Documentation: [venv](https://docs.python.org/3/library/venv.html)

---

#### Initialize the virtual environment
Make sure you are in the directory where you want to create your virtual environment  
```shell
$ python3 -m venv project_name
```
---
#### Activate the virtual environment
```shell
$ source ~/virtualenvironment/project_name/bin/activate
```
---

#### Update pip
```shell
$ pip install --upgrade pip
```
If pip is already up-to-date, you will see a message similar to this:
_"Requirement already up-to-date: pip in /Users/pnelson/virtualenvironment/project_name/lib/python3.7/site-packages (20.0.2)"_

---
#### Install some packages
These will be isolated to the python install within your virtual environment.
```shell
$ pip install pymongo dateparser
```
---
#### See the installed packages
```shell
$ cd virtualenvironment/project_name/lib/python3.7/site-packages

$ ls -la
```

You can also see a list of packages installed by running `pip list`

---
#### See that the virtual environment is using a different install of Python
```shell
$ which python
/Users/pnelson/virtualenvironment/project_name/bin/python
```
---
#### Deactivate the virtual environment
```shell
$ deactivate
```
