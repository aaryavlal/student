---
layout: page 
title: Trimester 1 CSP Final-Review Blog
permalink: /trionefinal
author: Aaryav Lal
---

# Trimester 1 CSP Final-Review Blog

## How have I changed Since the Start of the Year?

At the beginning of the year, I mostly worked on my own and didn’t focus much on how my code fit into a larger project. Working in a team helped me become more organized, since everyone needed to read and use my code. I also improved at documenting my work clearly so teammates could understand what I built. Explaining my decisions forced me to think more deeply about my own logic and approach. Overall, collaborating made me more connected, more cooperative, and more thoughtful about how I structure and share my code.

## Key Learnings From Sprints

### Tools Blog

WSL + Ubuntu Development Environment Guide\
Categories: DevOps\
Breadcrumb: /tools/os\
Updated: Apr 15, 2025\
Author: Lily Wu\
Reading time: ~2 minutes

This guide walks you through setting up Windows Subsystem for Linux (WSL) with Ubuntu for software development. You will install essential tools, learn basic shell commands, clone a project, and prepare your environment for daily development work.

Sections included:

-   Installation overview

-   Visual workflow description

-   Basic Ubuntu and Windows commands

-   WSL installation and configuration

-   First-time Ubuntu setup

-   System checks

-   How to restart your environment properly

Installation Overview:\
This setup process introduces you to working inside a Linux terminal, navigating directories, cloning a repository, and setting up the core tools you'll use for development.

Visual Workflow (described):

1.  Open Windows Terminal.

2.  Install WSL using "wsl --install."

3.  Launch Ubuntu with "wsl."

4.  Use Linux commands like mkdir, cd, and ls.

5.  Clone your project repo.

6.  Activate tools such as Python, Ruby, and Git.

7.  Follow the development cycle: write code, build, test, and commit.

Shell Commands:\
From Windows, run "wsl" to enter Ubuntu. Inside Ubuntu, use standard Linux directory commands such as mkdir, cd, and ls.

Version Control Commands:

-   git clone: copy a cloud repository locally

-   git pull: update your local repository

-   git commit: save changes locally

-   git push: publish your changes to the remote repository

Ubuntu Package Manager Commands (apt):

-   Update packages: sudo apt update

-   Upgrade packages: sudo apt upgrade

-   Install a package: sudo apt install <name>

-   Remove a package: sudo apt remove <name>

-   Search packages: apt search <name>

-   List installed packages: apt list --installed

Windows Setup:\
Install Visual Studio Code and follow default prompts.\
Install Git Credential Manager (GCM) and accept default settings.

Common WSL Commands:\
wsl --help\
wsl -l -o\
wsl -l -v\
wsl --shutdown\
wsl --unregister

Installing WSL:\
Open Windows Terminal. Run:

wsl --install -d Ubuntu-24.04

Create a username and password (the password will not display as you type).\
Exit after installation using "exit."\
Set Ubuntu 24.04 as the default:

wsl --set-default Ubuntu-24.04

Start Ubuntu again with "wsl," then close the terminal.

WSL Ubuntu Setup (First-Time):\
Right-click Terminal in the taskbar and choose Ubuntu 24.04. Run:

mkdir opencs\
cd opencs\
git config --global credential.helper "/mnt/c/Program\ Files/Git/mingw64/bin/git-credential-manager.exe"\
git clone <https://github.com/Open-Coding-Society/student.git>\
cd student/\
./scripts/activate_ubuntu.sh\
./scripts/activate.sh\
./scripts/venv.sh

System Checks (Optional):\
python --version\
pip --version\
ruby -v\
bundle -v\
gem --version\
git config --global --list

Restarting a Terminal Session:\
Whenever you open a new Ubuntu terminal, run:

cd opencs/student\
source venv/bin/activate\
code .

This activates your virtual environment and opens the project in VS Code.

### Framework

[Link to Framework Issue](https://github.com/aaryavlal/student/issues/3)

### Homeworks Complete 

3.1 Variables

[JavaScript Variables](https://aaryavlal.github.io/student//CSP/javascriptHW/variables)
[Python Variables](https://aaryavlal.github.io/student//CSP/pythonHW/variables)

3.2 Data Abstraction 

[JavaScript Data Abstraction](https://aaryavlal.github.io/student//CSP/javascriptHW/data_abstractions)
[Python Data Abstraction](https://aaryavlal.github.io/student//CSP/pythonHW/data_abstractions)

3.3 Mathematical Operations

[JavaScript Mathematical Operations](https://aaryavlal.github.io/student//CSP/javascriptHW/mathematical_operations)
[Python Mathematical Operations](https://aaryavlal.github.io/student//CSP/pythonHW/mathematical_operations)

3.4 Strings

[JavaScript Strings](https://aaryavlal.github.io/student/CSP/javascriptHW/strings)
[Python Strings](https://aaryavlal.github.io/student/CSP/pythonHW/strings)

3.5 Boolean Expressions

[JavaScript Boolean Expressions](https://aaryavlal.github.io/student//CSP/javascriptHW/booleans)
[Python Boolean Expressions](https://aaryavlal.github.io/student//CSP/pythonHW/booleans)

3.6 Conditonals 

[JavaScript Conditonals](https://aaryavlal.github.io/student//CSP/javascriptHW/conditionals)
[Python Conditionals](https://aaryavlal.github.io/student//CSP/pythonHW/conditionals)

3.7 Nested Conditonals 

[JavaScript Nested Conditonals](https://aaryavlal.github.io/student/CSP/javascriptHW/Nested_Conditionals)
[Python Nested Conditonals](https://aaryavlal.github.io/student/CSP/pythonHW/Nested_Conditionals)

3.8 Iteration

[JavaScript Iteration](https://aaryavlal.github.io/student/CSP/javascriptHW/iterations)
[Python Iteration](https://aaryavlal.github.io/student/CSP/pythonHW/iterations)

3.9 Developing Algorithms

[JavaScript Developing Algorithims](https://aaryavlal.github.io/student//CSP/javascriptHW/developing-algorithms)
[Python Developing Alhorithims](https://adityas-2010.github.io/Aditya_2026/python/developing-algorithms/crashers-hw)

3.10 Lists

[JavaScript Lists](https://aaryavlal.github.io/student/CSP/javascriptHW/lists)
[Python Lists](https://aaryavlal.github.io/student/CSP/pythonHW/lists)

3.12 Calling Procedures 

[JavaScript Calling Procedures](https://aaryavlal.github.io/student//CSP/javascriptHW/calling-procedures)
[Python Calling Procedures](https://aaryavlal.github.io/student//CSP/pythonHW/calling-procedures)

3.13 Developing Procedures 

[JavaScript Developing Procedures](https://aaryavlal.github.io/student/CSP/javascriptHW/developing-procedures)
[Python Developing Procedures](https://aaryavlal.github.io/student/CSP/pythonHW/developing-procedures)

3.15 Random Values

[JavaScript Random Values](https://aaryavlal.github.io/student/CSP/javascriptHW/random-values)
[Python Random Values](https://aaryavlal.github.io/student/CSP/pythonHW/random-values)

3.17 Algorithmic Efficiency

[JavaScript Algorithimic Efficiency](https://aaryavlal.github.io/student//CSP/javascriptHW/algorithmic-efficiency)
[Python Algorithimic Efficiency](https://aaryavlal.github.io/student/CSP/pythonHW/algorithmic-efficiency)

### Digital Famine Reflections

Our team, the Encryptors, worked together on the CyberSecurity submodule for *Digital Famine*, and the project pushed all of us to collaborate more effectively. I led Mission 2 and built the home layout that appears after clicking on the planet, but these pieces only came together because we communicated and coordinated our work. Adapting to a team environment meant explaining my code clearly, staying organized, and being open to feedback so others could build on what I created. Working this way helped me develop better habits and showed me how much stronger a project becomes when everyone contributes and supports each other.


## Night at the Musuem Reflection

While it was a little less engaing with our group due to technicalities, we recieved some good feedback comments. Some of these were basic ones like "cool game", but others really showed us what we were missing. Some people straight up said it was too complicated to understand, but showed interest in our presentation. Overall, it went ok for our specific group as we presented in the last order, so a lot of the visitors broke off. 

## What Do I want to Work on in Digital Famine

One thing I want to improve moving forward is making the system easier for the average person to use so they feel comfortable interacting with it. Some parts are still too technical or complicated, and simplifying the design, instructions, and flow would help people understand what they are doing without feeling overwhelmed. I also want to create a clearer and more consistent style across all the submodules. Right now, each level feels separate, with different approaches and no real connection in the skills being taught. Strengthening that sense of continuity would make the entire experience more organized and easier to follow. My goal is to create a smoother learning path where users feel like they are building on what they learned, not restarting each time.

## What Do I want To Learn Next

Even though I’ve worked with machine learning before, I’ve never really taken a full, focused deep dive into it. With how quickly AI has taken off, I genuinely believe new programmers should be taught the fundamentals early on so they understand what’s actually happening behind the scenes. It’s not just about using AI tools, but knowing the principles that make them work, which helps people think more clearly about their advantages and limitations. Learning these ideas now makes it much easier to keep up as the technology changes, instead of scrambling to catch up later. As AI continues to grow, having that foundation will matter more and more for anyone entering the field.

## Analytics Review

Done on Open Coding Society and GitHub

## MCQ Revision And Score

[Link to Revision for MCQ](https://github.com/aaryavlal/student/issues/2)

## What would I like to share? 

### **Project:** *SpoilWipe* 

-   Built completely on my own to **block YouTube spoilers** automatically.

-   **Scans hashtags and titles** in YouTube Shorts to detect potential spoilers.

-   If it finds a match, it **blurs the video** and shows a **"Watch Anyway" overlay**.

-   **Smart system:** tracks current video, resets blur when you scroll, and reacts instantly.

-   Added a **fullscreen overlay** (triggered with *Ctrl+Shift+S*) and **keyword history**.

-   Integrated the **OMDb API** for movie-related smart spoiler detection.

-   Learned a ton about **Chrome extension APIs, DOM manipulation, async messaging, and CSS animations**.

-   Cool part? It actually **works in real time** as you browse --- it feels seamless and alive.