# Visual Studio Code: Optimization and Standards

This guide outlines the configuration protocols for Visual Studio Code to ensure a standardized development environment across different Unix-like and Windows platforms.

---

## Technical Overview
Visual Studio Code (VS Code) serves as the primary integrated development environment (IDE) for this project, utilizing a modular architecture based on extensions and workspace-specific configurations.

---

## Environment Setup

Select your operating system to view specific installation and path configuration protocols:

=== "Windows"

    1. Download the System Installer from the [official VS Code site](https://code.visualstudio.com/).
    2. During installation, ensure the following options are enabled:
        * **Add to PATH** (requires shell restart).
        * **Register Code as an editor for supported file types**.
    3. Verify via terminal:
        ```powershell
        code --version
        ```

=== "macOS"

    1. Download the `.zip` archive for Apple Silicon or Intel.
    2. Move `Visual Studio Code.app` to the `/Applications` folder.
    3. Open the Command Palette (`Cmd+Shift+P`) and type: 
       `Shell Command: Install 'code' command in PATH`.
    
    Verify via terminal:
    ```bash
    code --version
    ```

=== "Linux"

    For Debian/Ubuntu based systems:
    ```bash
    sudo apt update
    sudo apt install software-properties-common apt-transport-https wget
    wget -q [https://packages.microsoft.com/keys/microsoft.asc](https://packages.microsoft.com/keys/microsoft.asc) -O- | sudo apt-key add -
    sudo add-apt-repository "deb [arch=amd64] [https://packages.microsoft.com/repos/vscode](https://packages.microsoft.com/repos/vscode) stable main"
    sudo apt update
    sudo apt install code
    ```

---

## Core Extensions Protocol
To maintain project consistency, the following extensions are considered mandatory:

* **Python**: Comprehensive support for the language (Pylance, Debugging).
* **Material Icon Theme**: Visual standardization of the file tree.
* **MkDocs Material**: Support for documentation preview and syntax.
* **GitLens**: Enhanced authorship traceability.

---

## Editor Configuration (settings.json)
Recommended global parameters for academic readability:

```json
{
    "editor.fontSize": 14,
    "editor.fontFamily": "'Fira Code', 'Consolas', monospace",
    "editor.fontLigatures": true,
    "editor.formatOnSave": true,
    "editor.renderWhitespace": "boundary",
    "files.insertFinalNewline": true,
    "files.trimTrailingWhitespace": true
}