---
template: post
title: >-
  Installing an IPython Kernel For a Virtual Environment For Use in Jupyter
  Notebook
slug: install-virtual-env-ipykernel-jupyter
draft: false
date: 2020-02-10T02:12:31.986Z
description: >-
  By making Jupyter aware of a specific version of python inside a virtual
  environment you can have more reproducible code and avoid conflicts introduced
  by third party packages when they are inevitably updated. You can keep your
  python version and third party libraries isolated from your OS and use it
  within Jupyter for a dynamic programming environment.
category: python
tags:
  - python
  - virtualenvironment
---
The goal today is to make Jupyter aware of your pre-existing virtual environment by installing an IPython Kernel.  

By running the terminal commands below you will be able to make Jupyter aware of the installation of Python in your virtual environment as well as all of the libraries you install through pip.

#### Activate Your Virtual Environment
Replace test_env with the name of the folder containing your virtual environment
```
$ source ~/virtualenvironment/test_env/bin/activate
```

#### Ensure Jupyter is Installed
```
$ pip install jupyter
```

#### Ensure ipykernel is Installed
```
$ pip install --user ipykernel
```

#### Install the IPython Kernel
Replace test_env with the name of the folder containing your virtual environment
```
$ python -m ipykernel --user --name=test_env
...Installed kernelspec test_env in /Users/pnelson/Library/Jupyter/kernels/test_env
```

#### Launch Jupyter Notebook
```
$ jupyter notebook
```

#### Change your Kernel
Inside Jupyter notebook on the toolbar, click Kernel > Change Kernel > your_kernel.
You will now see the name of the active kernel at the top right.  


#### List All Installed Kernels
```
$ ipython kernelspec list
```

#### Uninstall Kernels
```
$ ipython kernelspec remove <kernel_name>
```
