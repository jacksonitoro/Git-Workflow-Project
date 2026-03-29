# Git Workflow Implementation

This project demonstrates a structured Git workflow for a sample web application using feature branches, a develop branch, and pull requests. It simulates a real-world team environment with code reviews and integrates Git hooks to automate checks and prevent invalid commits.


## Tools Used

- Git
- VS Code git bash
- HTML simple web app
- GitHub

## Branching Strategy

- main: Stable production-ready code
- develop: Integration branch for combining completed features
- feature/*: Used to develop new features independently before merging into develop

## Workflow

1. Create a feature branch  
   `git checkout -b feature/login`

2. Develop the feature  
   Make necessary code changes in the feature branch

3. Commit changes  
   `git add .`  
   `git commit -m "Add login feature"`

4. Push branch to GitHub  
   `git push -u origin feature/login`

5. Create Pull Request  
   Open a PR on GitHub from `feature/login` to `develop` and describe the changes

6. Code Review  
   Team reviews the code, suggests improvements, and updates are pushed if needed

7. Merge Pull Request  
   After approval, merge the PR into `develop` using GitHub

8. Update local develop branch  
   `git checkout develop`  
   `git pull origin develop`


## Git Hooks

A pre-commit hook was implemented to automate checks before code is committed.

- The hook verifies that the required file (`index.html`) exists before allowing a commit
- If the file is missing, the commit is blocked with an error message
- This helps maintain consistency and prevents invalid or incomplete code from being committed to the repository


## Key Achievements

- Implemented a structured Git branching strategy using `main`, `develop`, and `feature/*` branches, reflecting real-world team workflows
- Simulated a complete pull request lifecycle, including feature development, code review, and merging into the `develop` branch
- Designed and implemented a pre-commit Git hook to validate the presence of required files before allowing commits
- Automated quality control using native Git hooks and shell scripting without relying on external tools