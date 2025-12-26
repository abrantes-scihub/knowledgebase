# GitHub: Technical Guide for Version Control

This document establishes a standardized workflow for version control, focusing on fundamental principles of software traceability and collaboration.

---

## Introduction

Version control is a system designed to record changes to files over time, ensuring reproducibility and historical integrity. Git serves as the distributed version control engine, while GitHub provides the infrastructure for remote hosting and collaborative development.

### Core Objectives

- **Traceability**: Comprehensive record of every modification.
- **Collaboration**: Parallel development workflows for research teams.
- **Redundancy**: Cloud-based backup of the complete project history.
- **Integrity**: Ability to revert to verified states without data loss.

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
```
