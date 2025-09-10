---
layout: base
title: "Installation Hack: Welcome to Your OS & Tools Setup"
date: 2025-09-09
categories: [Setup, Guide, Linux, Windows, Tools]
permalink: /setup
---

# 🚀 Installation Hack: Welcome to Your Journey!

Setting up your Operating System and developer tools is the first step to success. This guide will walk you through using a Linux terminal, managing folders, cloning projects, and installing packages. Everything is explained simply, with commands and tips for both Windows and Ubuntu.

---

Beginner Friendly guide

## 🖼️ Visual Workflow

1. **Open Windows Terminal**
   WINDOWS KEY + "R" -> type cmd 
2. **Install WSL**
   ```powershell
   wsl --install
   ```
3. **Launch Ubuntu Terminal**
   WINDOWS KEY + "R" -> type cmd 
   wsl
   ```
4. **Linux Commands**
   - `mkdir`, `cd`, `ls`
5. **Clone Project**
   - `git clone https://github.com/Open-Coding-Society/student.git` (Clone your own Repo)
6. **Activate Tools**
   - Ruby, Python, Git
7. **SDLC Workflow**
   - `code → make → test → commit`

---

## 💻 Shell Commands

### Windows
- Use `wsl` to enter Ubuntu, then standard Linux commands inside Ubuntu.

### Linux Basics
- `mkdir <folder>`: Create a folder
- `cd <folder>`: Change directory
- `ls`: List files

---

## 🔄 Version Control Commands

- `git clone <repo-url>`: Make a working copy from the cloud
- `git pull`: Update your local copy
- `git commit -m "message"`: Save changes locally
- `git push`: Send updates to the cloud

---

## 🛠️ Package Manager Commands (Ubuntu)

- Update package list: `sudo apt update`
- Upgrade packages: `sudo apt upgrade`
- Install package: `sudo apt install <package_name>`
- Remove package: `sudo apt remove <package_name>`
- Search package: `apt search <package_name>`
- List installed: `apt list --installed`

---

## 🪟 Windows Setup

### Install VS Code
- [VSCode Download](https://code.visualstudio.com/Download)
- Select your OS and use default prompts.

### Install Git Config Manager (GCM)
- [Git Credential Manager](https://github.com/GitCredentialManager/git-credential-manager)
- Use default prompts.

---

## 🐧 WSL Common Commands

- `wsl --help`
- `wsl -l -o`: List available distros
- `wsl -l -v`: List installed distros
- `wsl --shutdown`: Shutdown WSL
- `wsl --unregister <Distro>`: Remove a distro

---

## 🛠️ WSL Install Steps

1. **Open Windows Terminal and Pin to Taskbar**
2. **Install Ubuntu**
   ```powershell
   wsl --install -d Ubuntu-24.04
   ```
3. **Set up username and password** (password is hidden as you type)
4. **Exit WSL**
   ```bash
   exit
   ```
5. **Set Ubuntu as default**
   ```powershell
   wsl --set-default Ubuntu-24.04
   ```
6. **Start WSL Ubuntu**
   ```powershell
   wsl
   ```

---

## 🐧 WSL Ubuntu Setup (First Time)

1. **Open Ubuntu Terminal**
2. **Run setup commands:**
   ```bash
   mkdir opencs
   cd opencs
   git config --global credential.helper "/mnt/c/Program\ Files/Git/mingw64/bin/git-credential-manager.exe"
   git clone https://github.com/Open-Coding-Society/student.git
   cd student/
   ./scripts/activate_ubuntu.sh   # Enter your WSL Ubuntu password
   ./scripts/activate.sh          # Enter your Git UID and Personal Email
   ./scripts/venv.sh
   ```

---

## 🧪 System Checks (Optional)

Run these to verify your setup:
```bash
python --version
pip --version
ruby -v
bundle -v
gem --version
git config --global --list
```

---

## 🔁 Restarting a Terminal

Each time you open a new Ubuntu terminal session, go back to your directory :
```bash
cd opencs/student
source venv/bin/activate 
code .
```

---

## 📝 Easy Explanation

1. **Windows Terminal** is your starting point. Use `wsl` to jump into Ubuntu.
2. **Ubuntu** is your developer playground. Use Linux commands to manage files and folders.
3. **Clone your project** with `git clone`.
4. **Activate your tools** with the provided scripts.
5. **Check your setup** with version commands.
6. **Start coding** by activating your environment and opening VS Code.

---


