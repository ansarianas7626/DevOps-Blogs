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

### 🧩 Step 1: Install Git

1. Go to the official website: [https://git-scm.com/downloads](https://git-scm.com/downloads)
    
2. Download according to your OS (Windows / Mac / Linux).
    
3. Install using default settings.
    

Once installed, verify it by running this command in your terminal or Git Bash:

```bash
git --version
```

If you see a version number, Git is successfully installed. ✅

---

### 🧑‍💻 Step 2: Configure Git (Set Your Identity)

Before using Git for the first time, set your name and email — they’ll appear in your commit history.

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

You can check if it’s saved correctly:

```bash
git config --list
```

---

### 📂 Step 3: Initialize a Git Repository

Go to your project folder using `cd` command and initialize Git:

```bash
cd my-project
git init
```

🔹 This creates a hidden folder named `.git` inside your project — it tracks all your file changes.

---

### 🧾 Step 4: Add Files to the Staging Area

When you create or modify files, Git doesn’t automatically track them.  
You have to **add** them to the staging area first:

```bash
git add filename
```

or to add all files at once:

```bash
git add .
```

---

### 🧱 Step 5: Commit Your Changes

Once files are staged, you can **commit** them with a short message describing the change.

```bash
git commit -m "Initial commit"
```

📝 A commit is like a **snapshot** of your project at a certain point in time.

---

### ☁️ Step 6: Create a New Repository on GitHub

1. Go to [GitHub](https://github.com) → Click **“New Repository”**.
    
2. Give it a name (example: `my-project`) and click **Create repository**.
    
3. You’ll get a **remote repository URL**, something like:
    
    ```bash
    https://github.com/your-username/my-project.git
    ```
    

---

### 🌐 Step 7: Connect Local Repo to GitHub

Now, connect your local project (the one you initialized with `git init`) to the GitHub repository you just created.

```bash
git remote add origin https://github.com/your-username/my-project.git
```

Check the connection:

```bash
git remote -v
```

---

### 🚀 Step 8: Push Your Code to GitHub

Now that your local repo is connected, push your code to GitHub:

```bash
git push -u origin main
```

🧠 Note:

* In older Git versions, the default branch name was `master`.
    
* If your repo uses `master`, then use this instead:
    
    ```bash
    git push -u origin master
    ```
    

This uploads your project to GitHub for the first time 🎉  
Now you can see your files on your GitHub repository page!

---

### 🔁 Step 9: Future Changes Workflow

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

### 🧩 Common Branch Commands

| Command | Description |
| --- | --- |
| `git branch` | Lists all existing branches |
| `git branch <name>` | Creates a new branch |
| `git checkout <branch>` | Switches to a specific branch |
| `git checkout -b <branch>` | Creates and switches to a new branch |
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

## Git commands?

### ⚙️ Configuration Commands

| Command | Description |
| --- | --- |
| `git config --global` [`user.name`](http://user.name) `"Your Name"` | Sets your Git username globally |
| `git config --global` [`user.email`](http://user.email) `"`[`you@example.com`](mailto:you@example.com)`"` | Sets your Git email globally |
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