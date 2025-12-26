<<<<<<< HEAD
# Git and GitHub: Technical Guide for Version Control

This document establishes a standardized workflow for version control, focusing on fundamental principles of software traceability and collaboration.

---

## Introduction

Version control is a system designed to record changes to files over time, ensuring reproducibility and historical integrity. Git serves as the distributed version control engine, while GitHub provides the infrastructure for remote hosting and collaborative development.

### Core Objectives
* **Traceability**: Comprehensive record of every modification.
* **Collaboration**: Parallel development workflows for research teams.
* **Redundancy**: Cloud-based backup of the complete project history.
* **Integrity**: Ability to revert to verified states without data loss.

---

## Installation and Setup

Select the appropriate tab for your operating system environment:

=== "Windows"

    1. Download the installer from the [official Git website](https://git-scm.com/download/win).
    2. During installation, select **Git from Git Bash only**.
    3. Choose **MinTTY** as the default terminal emulator.
    
    Verify the installation via terminal:
    ```bash
    git --version
    ```

=== "macOS"

    It is recommended to use the Homebrew package manager:
    ```bash
    brew install git
    ```
    
    Alternatively, install Xcode Command Line Tools:
    ```bash
    xcode-select --install
    ```

=== "Linux"

    Use the package manager corresponding to your distribution:
    
    ```bash
    # Ubuntu / Debian
    sudo apt update && sudo apt install git

    # Fedora
    sudo dnf install git

    # Arch Linux
    sudo pacman -S git
    ```

---

## Phase 1: Local Initialization

The primary goal is to initialize a tracking environment for a specific directory.

### 1. Identity Configuration
Global parameters must be set to attribute commits to the correct researcher:

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
=======
# 📘 The Definitive Git & GitHub Guide: A Didactic Protocol

This guide establishes the standard workflow for version control, focusing on the **purpose** (the why), the **execution** (the how), and the **validation** (the check).

---

## 🧱 Level 1: The Foundation
**Goal:** Transform a standard folder into an intelligent repository that tracks every change.

### 1. Identity Configuration 🔑
Before recording any history, Git needs to know who the author is.
- **Action:** - `git config --global user.name "Your Full Name"`
  - `git config --global user.email "your.email@example.com"`
- **The "Why":** Every "save" (commit) is signed. Without this, Git cannot attribute changes to you.
- **Verification:** Run `git config --list` to confirm.

### 2. Initialization & Essential Setup 🏗️
Prepare the environment and set the rules for what Git should track.
- **Action:**
  - `git init`: Starts the Git engine in your folder.
  - `echo ".venv/" > .gitignore`: Creates a "shield" to ignore heavy system folders or sensitive files.
  - `echo "# My Knowledge Base" > README.md`: Creates the project's "front page."
- **The "Why":** The `.gitignore` prevents "junk" files from cluttering your repository, while the `README` provides context for anyone viewing your work.

### 3. The Saving Cycle (Add & Commit) 🔄
- **Action:**
  1. `git status`: Check what Git sees. ✅
  2. `git add .`: Place all changes in the "Staging Area" (the outbox). 📦
  3. `git commit -m "Initial commit"`: Permanently record the snapshot. 💾
- **Verification:** If `git status` says "nothing to commit, working tree clean", your first milestone is complete!

---

## ☁️ Level 2: Connecting to the World
**Goal:** Sync your local machine with GitHub for cloud backup and sharing.

### 1. Building the Bridge 🔗
Connect your local folder to your GitHub repository address.
- **Action:** `git remote add origin https://github.com/abrantes-scihub/knowledgebase.git`
- **Verification:** `git remote -v` should show your GitHub URL.

### 2. The First Push 🚀
- **Action:**
  - `git branch -M main`: Renames the default branch to the modern standard "main."
  - `git push -u origin main`: Sends the files and creates a permanent link.
- **The "Why":** The `-u` flag links your local branch to the remote one so that future pushes only require the command `git push`.

---

## 🌿 Level 3: Parallel Development (Branches)
**Goal:** Create "parallel universes" to test ideas without breaking the main project.

### 1. Creating Branches 🎋
- **Action:** `git checkout -b feature-name`
- **The "Why":** It's like taking a photocopy of your project. If the new feature works, you merge it; if it fails, you delete the branch with zero risk.

### 2. Merging 🤝
- **Action:** `git checkout main` then `git merge feature-name`.
- **Didactic Tip:** Always ensure your "main" branch is clean before merging a feature into it.

---

## ⚡ Level 4: Mastery & Recovery
**Goal:** Manage complex scenarios and undo mistakes like a professional.

### 1. The Pause Button (Stash) ⏸️
- **Action:** `git stash` hides your current work. `git stash pop` brings it back.
- **The "Why":** Perfect for when you need to switch branches immediately but aren't ready to commit your current work.

### 2. Emergency Recovery 🛡️
- **Action:**
  - `git commit --amend`: Fixes a typo in the last commit message.
  - `git reset --hard HEAD`: Discards all current changes and returns to the last saved state.
>>>>>>> 502f1cae15fed7b0b4c1cc6885bfcfa2d3d74709
