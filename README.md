# Protocols - GEE Books

This repository contains the technical documentation and protocols for GEE. The site is built using [MkDocs](https://www.mkdocs.org/) with the [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) theme.

## 🚀 Local Setup

When cloning this repository to a new machine, follow these steps to set up your development environment:

### 1. Prerequisites

Ensure you have **Python 3.x** installed on your system.

### 2. Create a Virtual Environment

In your terminal, navigate to the project root and run:

```bash
python -m venv .venv
```

3. Activate the Virtual Environment
   Windows (MSYS2/Git Bash/PowerShell):

Bash

source .venv/Scripts/activate
Linux/macOS:

Bash

source .venv/bin/activate 4. Install Dependencies
With the virtual environment activated, install the required packages:

Bash

pip install mkdocs-material
🛠️ Usage
Preview the site locally
To start a local development server and preview changes in real-time (usually at http://127.0.0.1:8000):

Bash

mkdocs serve
Build the static site
To manually generate the HTML files (stored in the site/ directory):

Bash

mkdocs build
Deploy to GitHub Pages
To publish updates directly to the gh-pages branch:

Bash

mkdocs gh-deploy
📁 Project Structure
docs/: Source files in Markdown (.md).

mkdocs.yml: Main configuration file (theme, navigation, and plugins).

.gitignore: Configured to exclude temporary folders like .venv/ and site/.
