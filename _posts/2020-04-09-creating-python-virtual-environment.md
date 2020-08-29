---
layout: post
title:  "Creating Virtual Environment in Python"
author: Pahul Preet Singh Kohli
categories: [Virtual Environment, Python] 
image: assets/images/virtual.jpeg
description: "Virtual Environment is a resource that helps keep the dependencies provided by various projects apart by developing independent python virtual environments."
comments: false
---


**Virtual Environment:** is a resource that helps keep the dependencies provided by various projects apart by developing independent python virtual environments.

- Generally speaking, it's good practice to have a new virtual environment for any Python software project as each project's dependencies are separated from the program and one another.

##### Requirements
- python
- pip3

##### Steps to set up python virtual Environment			

- Open a terminal
- Enter the following commands in the terminal:
	- $ pip3 install virtualenv
	- $ virtualenv project --python=python3.7  #project is the name of the virtual environment and python3.7 is the python version for the -environment
	- $ cd project
	- $ source bin/activate # activate the environment
	- $ deactivate # deactivate the environment

