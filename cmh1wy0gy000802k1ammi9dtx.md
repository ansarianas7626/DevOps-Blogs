---
title: "GitHub for Beginners: Complete Guide to Version Control"
datePublished: Wed Oct 22 2025 11:31:50 GMT+0000 (Coordinated Universal Time)
cuid: cmh1wy0gy000802k1ammi9dtx
slug: github-for-beginners-complete-guide-to-version-control
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1761132650267/743e72a9-b26d-4715-83ed-eaed9e580c68.png
tags: github, version-control, git, devops, versioning, devops-articles, devops-journey, version-control-systems, devopscommunity

---

## 🧩 What is Version Control System (VCS)?

A **Version Control System (VCS)** is a tool that helps developers **track and manage changes** in code.  
Imagine you are working on a project and want to keep older versions safe — that’s exactly what VCS does.

✅ **Key benefits:**

* Keeps a record of every change in your project
    
* Helps multiple developers work together on the same code
    
* Allows you to **revert** to an older version if something breaks
    
* Reduces confusion and increases collaboration
    

**Example:** Git, SVN, CVS, Mercurial etc.

## 🧠 What is Git?

**Git** is an **open-source, distributed version control system** developed by **Linus Torvalds** (the creator of Linux).  
It allows multiple developers to work on the same project **without overwriting each other’s code**.

🟢 **Main features of Git:**

* Distributed architecture (everyone has a local copy of the repo)
    
* Branching and merging made easy
    
* Speed and efficiency
    
* Works offline (no internet needed to commit)
    

Git is the **most popular VCS** today and is used by companies like Microsoft, Google, and Amazon.

## ⚔️ CVS, SVN vs Git – What’s the Difference?

Before Git, tools like **CVS (Concurrent Versions System)** and **SVN (Subversion)** were used.  
But Git changed the game!

| Feature | CVS / SVN (Old Systems) | Git (Modern System) |
| --- | --- | --- |
| Architecture | Centralized | Distributed |
| Speed | Slower | Faster |
| Offline work | ❌ No | ✅ Yes |
| Branching | Complex | Easy & Lightweight |
| Data Security | Less Secure | Highly Secure |

👉 **In short:** Git is **faster, safer, and easier to use** than traditional systems like CVS or SVN.

## 🌐 Centralized vs Distributed Version Control Systems

| Type | Description | Example |
| --- | --- | --- |
| **Centralized VCS (CVCS)** | One central server stores all versions of the code. Developers must stay online to access or commit code. | SVN, CVS |
| **Distributed VCS (DVCS)** | Every developer has a complete copy (repository) of the code, including its full history. You can work offline and sync changes later. | Git, Mercurial |

💡 **Why Git wins:** It’s distributed — even if the server goes down, your local copy still has the entire project.

## 🐙 What is GitHub?

**GitHub** is a **cloud-based hosting platform** for Git repositories.  
It lets developers store, share, and collaborate on projects using Git.

🧰 **In short:**

* Git = Version control system
    
* GitHub = Place to host Git repositories online
    

Other Git hosting platforms: **GitLab, Bitbucket, SourceForge**

💬 Think of **GitHub as social media for developers** — you can share code, contribute to others’ projects, and showcase your portfolio.

## ⚙️ How to Initialize Git in Your System?

To start using Git, you first need to install and initialize it in your local project folder.

### Step 1: Install Git

1. Go to the official website: [https://git-scm.com/downloads](https://git-scm.com/downloads)
    
2. Download according to your OS (Windows / Mac / Linux).
    
3. Install using default settings.
    

Once installed, verify it by running this command in your terminal or Git Bash:

```bash
git --version
```

If you see a version number, Git is successfully installed. ✅

---

### Step 2: Initialize Local Repository

```bash
cd path/to/your/project
git init
```

* This command turns your project folder into a Git repository.
    
* It creates a hidden `.git` folder to track changes.
    

---

### Step 3: Create a Remote Repository on GitHub

1. Log in to GitHub.
    
2. Click **New Repository** → give it a name → click **Create repository**.
    
3. Copy the HTTPS URL, e.g.:
    

```bash
https://github.com/username/repo-name.git
```

---

### Step 4: Add Remote to Your Local Repo

```bash
git remote add origin https://github.com/username/repo-name.git
```

* Now your local repository is connected to the remote repository called `origin`.
    

---

### Step 5: Stage and Commit Your Changes

```bash
git add .
git commit -m "Initial commit"
```

---

### Step 6: Push to GitHub Using Personal Access Token (PAT)

1. Run:
    

```bash
git push -u origin main
```

* Git will prompt:
    

```bash
Username: <your GitHub username>
Password: <paste your personal access token here>
```

> Paste your **PAT** instead of your password.

* Adjust the branch name if it’s not `main`.
    

---

### Step 7: Optional — Store Credentials for Future Pushes

```bash
git config --global credential.helper store
```

* This stores your PAT locally.
    
* Future pushes/pulls will not require entering the token again.
    

---

## **Optional Shortcut — PAT in URL (Not Recommended for Security)**

```bash
git remote set-url origin https://<USERNAME>:<PAT>@github.com/username/repo-name.git
```

* **Warning:** The token will be stored in your shell history, which is insecure.
    
* Safer approach: use the prompt + credential helper method.
    

---

## **Summary Workflow**

```bash
cd project-folder
git init
git remote add origin https://github.com/username/repo-name.git
git add .
git commit -m "Initial commit"
git push -u origin main
# Username: your GitHub username
# Password: paste your PAT
git config --global credential.helper store   # optional
```

---

### 🔁 Step 8: Future Changes Workflow

Once setup is done, your normal day-to-day workflow looks like this:

```bash
git add .
git commit -m "Updated project"
git push
```

💡 **Shortcut Tip:** Combine add + commit + push in one go (for small updates):

```bash
git add . && git commit -m "Quick update" && git push
```

## 🌿 What is Branching in Git?

Branching in Git means creating a **separate line of development** within the same project.  
It allows multiple people (or even a single developer) to work on different features, fixes, or experiments — **without affecting the main codebase**.

Think of a branch as a **copy of your project** where you can make changes freely.  
Once your changes are complete and tested, you can **merge** them back into the main branch.

---

### 🧱 Example

Let’s say you are building a website:

* The `main` branch has your live, working site.
    
* You create a new branch called `feature/contact-form` to add a new contact page.
    
* You work on it, test it, and when it’s ready — merge it back into `main`.
    

If something goes wrong, your main website still remains safe.

---

### ⚙️ Why Branching is Useful

* Allows multiple developers to work **in parallel**
    
* Keeps the **main branch stable**
    
* Makes **code reviews and testing** easier
    
* Supports **experimentation** without risk
    

---

## **How to Contribute to Open Source – Step by Step**

Contributing to open source is a great way to improve your skills, collaborate with developers worldwide, and give back to the community. Here’s a simple step-by-step guide:

---

### **Step 1: Find a Project**

* Choose a project you are interested in or familiar with.
    
* Use platforms like GitHub, GitLab, or Bitbucket.
    
* Look for repositories labeled **“good first issue”** or **“beginner-friendly”** if you are new.
    

---

### **Step 2: Fork the Repository**

* Go to the repository you want to contribute to.
    
* Click the **Fork** button at the top-right corner.
    
* This creates your **own copy** of the repo under your GitHub account.
    

---

### **Step 3: Clone Your Forked Repo**

* Copy the **HTTPS or SSH URL** of your forked repo.
    
* Clone it to your local machine:
    

```bash
git clone https://github.com/your-username/project-name.git
cd project-name
```

---

### **Step 4: Create a New Branch**

* Always create a new branch for your changes instead of working on `main`:
    

```bash
git checkout -b feature-or-bugfix-branch
```

* Name it clearly, e.g., `fix-login-bug` or `add-dark-mode`.
    

---

### **Step 5: Make Changes**

* Edit the code, documentation, or other files as needed.
    
* Test your changes locally to ensure everything works.
    

---

### **Step 6: Stage and Commit Changes**

```bash
git add .
git commit -m "Add feature X / Fix bug Y"
```

* Keep your commit messages **clear and descriptive**.
    

---

### **Step 7: Push Changes to Your Fork**

```bash
git push origin feature-or-bugfix-branch
```

* This uploads your branch and changes to your forked repository on GitHub.
    

---

### **Step 8: Create a Pull Request (PR**[**)**](https://github.com)

* Go to your fork on GitHub.
    
* Click **Compare & pull request** for your branch.
    
* Write a clear PR title and description explaining your changes.
    
* Submit the PR to the original repository.
    

---

### **Step 9: Review and Respond**

* Maintainers may review your PR and request changes.
    
* Make any requested changes in your branch and push again[:](https://github.com)
    

```bash
git add .
git commit -m "Update based on review"
git push origin feature-or-bugfix-branch
```

---

### **Done!**

* Once your PR is merged, congratulations! 🎉
    
* You have officially contributed to an open-source project.
    

---

### **Tips for Beginners**

* Start with **documentation or small bug fixes** if coding contribution feels intimidating.
    
* Follow the **project’s contribution guidelines** (`CONTRIBUTING.md` if available).
    
* Be polite, patient, and professional while interacting with maintainers.
    

---

## Clone vs fork repository

| **Clone** | **Fork** |
| --- | --- |
| Local copy of repo | Copy of repo on your GitHub account |
| Work locally | Contribute to someone else’s project |
| Needs write access to original repo | Full control on your fork |
| Local machine | GitHub account + optional local clone |
| Personal or team work | Open source contribution |
| Manual pull to sync | Can sync anytime |
| Local & remote branches | Branches in your fork, PR to original |

---

### 🧩 Common Branch Commands

| Command | Description |
| --- | --- |
| `git branch` | Lists all existing branches |
| `git branch <name>` | Creates a new branch |
| `git checkout <branch>` | Switches to a specific branch |
| `g``it checkout -b <branch>` | Creates and switches to a new branch |
| `git merge <branch>` | Merges another branch into the current one |
| `git branch -d <branch>` | Deletes a branch |

## **What is Branching Strategy in Git?**

A branching strategy defines how different branches are used and managed in a Git workflow to ensure smooth development, testing, and deployment.

---

**🔹 main / master branch:**

* Always contains the **latest stable and production-ready code**.
    
* Only **tested and approved code** from the release or hotfix branches gets merged here.
    
* This is the branch that goes to **production deployment**.
    

---

**🔹 feature branch:**

* Used for **developing new features or functionalities**.
    
* Created from the `develop` branch (or `main` if no develop branch exists).
    
* Once the feature is complete and tested, it’s merged back into `develop`.
    

---

**🔹 release branch:**

* Created when you are **preparing for a new production release**.
    
* Used for **final testing, bug fixes, and version tagging**.
    
* After testing, it’s merged into both `main` (for deployment) and `develop` (to sync fixes).
    

---

**🔹 hotfix / bugfix branch:**

* Used for **urgent fixes directly on production**.
    
* Created from the `main` branch to fix live issues quickly.
    
* After fixing, merged into both `main` and `develop`.
    

---

## What is Git Hooks?

**Git Hooks** are scripts that run automatically when certain events occur in a Git repository — such as a **commit**, **push**, or **merge**.

In simple terms, they are small automation tools that execute at different stages of the Git workflow.  
For example:

* When you run `git commit`, a **pre-commit hook** can automatically format your code or run tests.
    
* When you run `git push`, a **pre-push hook** can ensure that all tests pass before the code is pushed.
    

### 🧩 Common Git Hooks

| Hook Name | Triggered When | Example Use |
| --- | --- | --- |
| `pre-commit` | Before a commit is made | Lint or format code |
| `commit-msg` | After commit message is entered | Validate commit message format |
| `pre-push` | Before code is pushed | Run tests before pushing |
| `post-merge` | After a merge completes | Reinstall dependencies if required |

### ⚙️ Location

Hooks are stored inside the `.git/hooks/` directory of your repository.  
By default, you’ll find sample hook files there (like `pre-commit.sample`).  
You can rename them, make them executable, and add your own custom automation.

---

## ⚙️ What is GitHub Actions?

**GitHub Actions** is a powerful CI/CD (Continuous Integration and Continuous Deployment) tool built right into **GitHub**.  
It allows developers to **automate workflows** — like testing, building, and deploying code — directly from their repositories.

In simple terms, it helps you run scripts automatically whenever something happens in your repo — for example, when you **push code**, **open a pull request**, or **merge changes**.

### 🚀 Why Use GitHub Actions?

* **Automate repetitive tasks** like testing and deployment
    
* **Improve code quality** by running lint checks automatically
    
* **Save time** by building, testing, and deploying your app right from GitHub
    
* **Supports any language or platform** (Node.js, Python, Docker, etc.)
    

### 🧩 Key Concepts

| Term | Meaning |
| --- | --- |
| **Workflow** | The entire automation process (defined in a `.yml` file) |
| **Job** | A set of steps that run on the same machine |
| **Step** | An individual task (like running a command or script) |
| **Action** | A reusable component or script used in workflows |
| **Runner** | The server that runs your workflow (GitHub-hosted or self-hosted) |

### 📁 Where It Lives

GitHub Actions workflows are stored in your repo under:

```bash
.github/workflows/
```

Each workflow file is written in **YAML**, for example:  
`deploy.yml`, `test.yml`, or `ci.yml`.

---

## Git commands?

### ⚙️ Configuration Commands

| Command | Description |
| --- | --- |
| `git config --global` `user.name` `"Your Name"` | Sets your Git username globally |
| `git config --global` `user.email` `"you@example.com"` | Sets your Git email globally |
| `git config --list` | Displays all current Git configurations |
| `git help` | Shows help information for any Git command |

---

### 📁 Repository Setup Commands

| Command | Description |
| --- | --- |
| `git init` | Initializes a new local Git repository |
| `git clone <repo_url>` | Clones (downloads) an existing remote repository |
| `git remote add origin <repo_url>` | Links your local repo to a remote one |
| `git remote -v` | Displays remote URLs connected to your repository |

---

### 📄 File Tracking Commands

| Command | Description |
| --- | --- |
| `git status` | Shows the current state of files (modified, staged, etc.) |
| `git add <file>` | Stages a specific file for the next commit |
| `git add .` | Stages all changed files in the directory |
| `git rm <file>` | Removes a file from the working directory and staging area |
| `git mv <old> <new>` | Renames or moves a file |

---

### 🧱 Commit & Log Commands

| Command | Description |
| --- | --- |
| `git commit -m "message"` | Saves staged changes with a message |
| `git commit -am "message"` | Adds & commits tracked files in one step |
| `git log` | Shows commit history |
| `git show <commit_id>` | Displays details of a specific commit |
| `git diff` | Shows unstaged file differences |
| `git diff --staged` | Shows differences for staged files |

---

### 🌿 Branching Commands

| Command | Description |
| --- | --- |
| `git branch` | Lists all branches |
| `git branch <name>` | Creates a new branch |
| `git checkout <branch>` | Switches to a specific branch |
| `git checkout -b <branch>` | Creates and switches to a new branch |
| `git merge <branch>` | Merges another branch into the current one |
| `git branch -d <branch>` | Deletes a branch |
| `git switch <branch>` | Alternative to checkout for switching branches |

---

### 🌍 Remote & Push/Pull Commands

| Command | Description |
| --- | --- |
| `git push` | Uploads commits to the remote repository |
| `git push -u origin main` | Pushes your main branch and sets upstream tracking |
| `git pull` | Fetches and merges changes from remote repo |
| `git fetch` | Downloads changes without merging |
| `git remote remove origin` | Unlinks a remote repository |
| `git remote rename origin newname` | Renames a remote |

---

### ♻️ Undo & Restore Commands

| Command | Description |
| --- | --- |
| `git reset <file>` | Unstages a file without deleting changes |
| `git reset --hard` | Discards all local changes permanently |
| `git restore <file>` | Restores file content from the last commit |
| `git revert <commit_id>` | Creates a new commit that undoes a previous one |
| `git clean -fd` | Removes untracked files & folders |

---

### 🧠 Advanced Commands

| Command | Description |
| --- | --- |
| `git stash` | Temporarily saves uncommitted changes |
| `git stash pop` | Restores stashed changes and removes them from stash list |
| `git tag <tagname>` | Creates a tag for a commit (like version labeling) |
| `git cherry-pick <commit_id>` | Applies a specific commit from another branch |
| `git blame <file>` | Shows who changed which line in a file |
| `git reflog` | Shows all actions (commits, checkouts, etc.) performed in repo |

## 🏁 Conclusion

Git is a powerful tool that helps you **keep track of your code** and **work with others easily**. Even as a beginner, learning Git will make your projects organized and safe.

Start with small steps — **initialize a repo, commit your changes, and push to GitHub**. With a little practice every day, using Git will soon feel like second nature.

## 🔠 Short Forms & Abbreviations

| Short Form | Full Form |
| --- | --- |
| **VCS** | Version Control System |
| **CVCS** | Centralized Version Control System |
| **DVCS** | Distributed Version Control System |
| **CVS** | Concurrent Versions System |
| **SVN** | Subversion |
| **CLI** | Command Line Interface |
| **Repo** | Repository |
| **PR** | Pull Request |

[Lecture Video Link 1](https://www.youtube.com/watch?v=fIMySI_gZJU&list=PLdpzxOOAlwvIKMhk8WhzN1pYoJ1YU8Csa&index=17)

[Lecture Video Link 1](https://www.youtube.com/watch?v=MCyvYT8FS5w&list=PLdpzxOOAlwvIKMhk8WhzN1pYoJ1YU8Csa&index=17)

[Lecture Video Link 1](https://www.youtube.com/watch?v=mT6qrAx14O4&list=PLdpzxOOAlwvIKMhk8WhzN1pYoJ1YU8Csa&index=18)