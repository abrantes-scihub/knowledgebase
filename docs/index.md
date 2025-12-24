site_name: My Knowledge Base
site_description: Personal library of technical protocols and learning paths.
theme:
  name: material # Recomendo o tema 'material' para uma aparência profissional

nav:
  - Home: index.md
  - Protocols:
      - Git & GitHub: protocols/git-github.md
  - About: about.md

plugins:
  - search

markdown_extensions:
  - tables
  - admonition
  - pymdownx.highlight:
      anchor_linenums: true
  - pymdownx.inlinehilite
  - pymdownx.snippets