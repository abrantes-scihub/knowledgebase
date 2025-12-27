# Protocols - GEE Books

This repository contains the technical documentation and protocols for almost any development environment. The site is built using [MkDocs](https://www.mkdocs.org/) with the [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) theme.

## Local Setup
When cloning this repository to a new machine, follow these steps to set up your development environment:

### 1. Prerequisites
Ensure you have **Python 3.x** installed on your system.

### 2. Create a Virtual Environment
In your terminal, navigate to the project root and run:

```bash
python -m venv .venv
```

### 3. Activate the Virtual Environment
**Windows** (MSYS2/Git Bash/PowerShell)

```bash
source .venv/Scripts/activate
```

**Linux/macOS**

```bash
source .venv/bin/activate
```

### 4. Install Dependencies
With the virtual environment activated, install the required packages:

```bash
pip install -r requirements.txt
```

## Usage
**Preview the site locally**
To start a local development server and preview changes in real-time (usually at http://127.0.0.1:8000):

```bash
mkdocs serve
```
**Build the static site**
To manually generate the HTML files (stored in the site/ directory):

```bash
mkdocs build
```
**Deploy to GitHub Pages**
To publish updates directly to the gh-pages branch:

```bash
mkdocs gh-deploy
```

## Project Structure
- **docs/**: source files in Markdown (```.md```).
- **mkdocs.yml**: main configuration file (theme, navigation, and plugins).
- **.gitignore**: configured to exclude temporary folders like ```.venv/``` and ```site/```.