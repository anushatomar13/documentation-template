# Installation

## Setup Requirements

To work with the documentation files and deploy the updated site, you'll need to have the following tools installed:

- A Bash shell environment
- Git version control system
- Python 3 programming language
- The Material for MkDocs theme
- The Mike MkDocs plugin for publishing versions to gh-pages
  - This plugin is not required for local development but is necessary for deploying the site to gh-pages

### Installing Git

Git can be installed locally by following the instructions in the [Install Git Guide](https://github.com/git-guides/install-git) provided by GitHub.

### Installing Python 3

Python 3 can be installed locally by following the steps in the [Python Getting Started guide](https://www.python.org/about/gettingstarted/).

### Installing MkDocs and Dependencies

The MkDocs static site generator and its required dependencies can be installed locally using the following command, as outlined in the [Material for MkDocs installation instructions](https://squidfunk.github.io/mkdocs-material/getting-started/):

```
pip install -r requirements.txt
```

### Verifying the Setup

To ensure that your setup is correct, you can verify the installation of MkDocs by running the command `mkdocs --help`. This should display the help text for the MkDocs command-line interface.
