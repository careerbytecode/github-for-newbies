# GitHub-for-newbies
Hands-on exercises and notes for beginners to learn GitHub.
 
This repository contains materials, exercises, and guides for learning Git and GitHub from scratch.  

> **Duration:** 1 Hour  
> **Target Audience:** Beginners with zero prior experience in Git or GitHub

---

**0–5 min – Introduction**
- Why version control matters: teamwork, history, rollback
- Difference between Git (local) and GitHub (remote / collaboration)
- Overview of session topics

**5–15 min – Getting Started with Git**
- Installing Git & configuring user details
- Initializing a repository: `git init`
- Basic workflow: `git add`, `git status`, `git commit`
- Viewing history: `git log`, `git diff`

**15–25 min – Remote Repositories & GitHub Basics**
- Creating a repository on GitHub
- Cloning a repo: `git clone`
- Linking local to remote: `git remote add origin <URL>`
- Pushing & pulling changes: `git push`, `git pull`
- Simple collaboration workflow: local → commit → push → remote

---

## Branching and Merging 

Branching allows working on new features, bug fixes, or experiments **without affecting the main code**.  

### **Key Commands**
```bash
# Create a branch
git branch <branch-name>

# Switch to a branch
git switch <branch-name>

# Stage changes
git add <file>

# Commit changes
git commit -m "Your commit message"

# Merge a branch into main
git switch main
git merge <branch-name>

# Delete a branch
git branch -d <branch-name>       # Local
git push origin --delete <branch-name>  # Remote
```

### Branch Naming Best Practices

Use clear, descriptive names for branches to make collaboration easier:

- `feature/login-page`  
- `bugfix/navbar-issue`  
- `docs/readme-update`  
- `hotfix/crash-fix`  

### Mini Demo Idea

1. Create a branch  
2. Add a file  
3. Commit changes  
4. Merge branch into main  
5. Delete branch locally & remotely  

### Merge Conflicts

- Occur when multiple changes overlap  
- Resolve manually in a code editor or directly in the GitHub UI  

---
## Pull Requests & Collaboration

Pull Requests (PRs) are how you propose changes from your branch to the main branch. They are essential for **collaboration and code review**.

### **Step-by-Step Guide**

1. **Forking vs Branching Workflow**
   - Forking: copy someone else’s repo to your account (common in open-source)
   - Branching: create a branch in the same repo (common in team projects)

2. **Create a Pull Request**
   - Push your branch to GitHub:  
     ```bash
     git push origin <branch-name>
     ```
   - Go to your repository on GitHub → Click **"Compare & pull request"**
   - Add a title and description for your PR

3. **Assign Reviewers & Add Labels**
   - Assign a team member to review your changes
   - Add labels like `bug`, `feature`, `documentation` for clarity

4. **Code Review & Approval**
   - Reviewer checks the changes
   - Add comments if improvements are needed
   - Approve PR once ready

5. **Merge Pull Request**
   - Click **"Merge pull request"** on GitHub
   - Optionally delete the branch after merging

6. **Link PRs to Issues**
   - Use keywords like `fixes #3` in PR description to automatically close the linked issue

7. **Resolve Conflicts**
   - If there are conflicts, GitHub UI shows them
   - Edit directly in GitHub or locally to resolve

8. **Bonus**
   - Use GitHub Issues to track tasks
   - Use Project Boards for organizing teamwork

---

## Best Practices & Advanced Tips

### **1. Writing Clean Commit Messages**
  - Format:  
     ```bash
     feat: add login page
     fix: navbar alignment issue
     docs: update README
     ```
   - Keep commit messages short, meaningful, and consistent

   - Make small, focused commits

2. Using .gitignore
   - Avoid committing unnecessary files like IDE configs or temporary files

   - Example:
    ```bash
       *.log
       node_modules/
       .env
    ```
   - Quick hack: generate templates at gitignore.io

3. Avoid Large Binaries
   - Don’t commit large files; use Git LFS if needed

4. Stash Temporary Work
    ```bash
       git stash       # Save changes temporarily
       git stash pop   # Retrieve stashed changes
    ```
5. Undo Safely
   - Safe undo: git revert <commit> (creates a new commit)

   - Advanced: git reset (can rewrite history; use with caution)

6. Protect Main Branch
   - Enable branch protection rules on GitHub

   - Require PR reviews before merge

7. Conceptual Notes
   - Rebase vs Merge (just concept for now)

   - Intro to CI integration (testing before merge)

8. README Best Practices
   - Include badges (build, license, coverage)

   - Project description & setup steps

   - Screenshots of the project

   - Contributors / team members

## ⏱ 24-hour Challenge:
Create a repo
   - Add a file
   - Create a branch
   - Modify the file
   - Push changes
   - Create a PR
   - Assign a friend as reviewer
   - Merge the PR
   - Provide Cheat-Sheet
---
Follow [Jenefer Rexee on LinkedIn](https://www.linkedin.com/in/jenwithai/)  
- Added feedback UI section
