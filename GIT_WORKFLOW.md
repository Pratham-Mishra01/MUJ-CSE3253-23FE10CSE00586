# Git Workflow Documentation

This document explains the Git workflow followed in this project and some important Git concepts that are commonly used in real-world development.



## GitFlow vs GitHub Flow

GitFlow is a structured branching model where different branches have specific purposes. In GitFlow, `main` is used for production-ready code, while `develop` is used for integrating features. Additional branches such as `feature`, `release`, and `hotfix` are created depending on the type of work being done. This workflow is useful for projects that follow versioned releases and need clear separation between development and production.

GitHub Flow is a simpler workflow. It usually has only one main branch, and developers create short-lived feature branches from it. Once the feature is complete, it is merged back into the main branch. GitHub Flow is commonly used in projects that follow continuous integration and continuous deployment.



## Rebase vs Merge

Merge is used to combine changes from one branch into another by creating a merge commit. It preserves the complete history of both branches and is generally safer for shared branches like `main` or `develop`.

Rebase works differently. It takes commits from one branch and re-applies them on top of another branch, which results in a linear commit history. Since rebase rewrites commit history, it should only be used on private or feature branches and not on branches that are already shared with others.


## Commit Message Conventions

Clear commit messages make it easier to understand the project history. In this project, the following conventions are followed:
- Commit messages are written in present tense
- Messages are short and meaningful
- Each commit focuses on a single change or feature

Examples:
- Add login page
- Fix merge conflict in styles.css
- Update README with workflow details



## Pull Request Template

### Description
Provide a brief summary of the changes made in the pull request.

### Changes Made
- List the main changes or features added
- Mention important files that were modified

### Testing
Describe how the changes were tested or verified.

### Checklist
- Code builds without errors
- Changes are reviewed
- No unresolved merge conflicts
