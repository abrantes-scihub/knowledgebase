# Git: Version Control Protocol

This protocol establishes the standards for installation, configuration, and integration of Git as the primary version control system, ensuring seamless operation with Visual Studio Code.

---

## Installation Protocol

Select your operating system to ensure the correct binaries and environment variables are set:

=== "Windows"

    1. Download the **64-bit Git for Windows Setup** from [git-scm.com](https://git-scm.com/).
    2. During installation, select these critical options:
        * **Editor**: Choose "Use Visual Studio Code as Git's default editor".
        * **PATH Environment**: Select "Git from the command line and also from 3rd-party software".
        * **Line Endings**: Select "Checkout Windows-style, commit Unix-style line endings" (CRLF to LF).
        * **Terminal Emulator**: Use "MinTTY" (standard for Git Bash).
    3. Verify in Git Bash:
        ```bash
        git --version
        ```

=== "macOS"

    1. Recommendation: Install via [Homebrew](https://brew.sh/):
       ```bash
       brew install git
       ```
    2. Alternatively, use the installer from [git-scm.com](https://git-scm.com/).
    3. Verify in Terminal:
       ```bash
       git --version
       ```

=== "Linux"

    1. Use the package manager for your distribution:
       ```bash
       # Ubuntu/Debian
       sudo apt update
       sudo apt install git
       ```
    2. Verify:
       ```bash
       git --version
       ```

---

## Command Line Workflow: Git Bash & VS Code

One of the most efficient ways to start working is using the **Git Bash** terminal to launch your project environment.

### Opening a Project
Instead of using the Windows Explorer, navigate to your project folder and call VS Code directly:

```bash
# 1. Open Git Bash
# 2. Navigate to your work directory
cd ~/Documents/YourProjectFolder

# 3. Launch VS Code in the current directory
code .
```
---

### Why use `code .` in Git Bash?

* **Context**: VS Code opens exactly at the root of your Git repository.
* **Consistency**: It ensures the terminal environment inside VS Code inherits the correct Bash paths.
* **Speed**: It is the industry-standard professional workflow for developers.

---

## Post-Installation Identity

Before creating any records, you must define your global identity. This information is attached to every commit you make.

```bash
# Set your global username
git config --global user.name "Your Full Name"

# Set your global email
git config --global user.email "your-email@example.com"

# Verify your configurations
git config --list
```

## Core Local Workflow

Once the project is open in VS Code, use the integrated Git Bash terminal to execute the standard development cycle:

1. **Verification**: Check the current state of your files.
    ```bash
    git status
    ```

2. **Staging**: Group the changes you want to include in the next record.
    ```bash
    git add .
    ```

3. **Commitment**: Save the snapshot with a clear, descriptive message.
    ```bash
    git commit -m "type: descriptive message in present tense"
    ```

!!! tip "Commit Format"
    Use the pattern `type: description` (e.g., `feat: add login page` or `fix: resolve overflow issue`). This keeps the history readable for any project.