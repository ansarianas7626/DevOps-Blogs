---
title: "Shell Scripting Zero to Hero"
datePublished: Fri Oct 03 2025 16:12:11 GMT+0000 (Coordinated Universal Time)
cuid: cmgb1ld2y000002lb1l81enwn
slug: shell-scripting-zero-to-hero
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1759430765152/9ed32077-1f7d-4279-8640-8a3d52428c1c.png
tags: linux, aws, devops, shell-scripting, devops-articles, devops-journey, devopscommunity, abhishek-veeramalla

---

## Introduction to shell scripting

Shell scripting is a way to automate tasks in Linux/Unix by writing a set of commands in a file. Instead of typing commands one by one in the terminal, you put them in a script file and run it directly.  
👉 Beginners can use shell scripts for simple tasks like file handling, automation, monitoring, and DevOps workflows.

## What is shebang?

Shebang (`#!`) is the first line of a shell script that tells the system **which shell should execute the script**.

* Common shebangs are:
    
    ```bash
    #!/bin/bash   # Most commonly used, default on Linux
    #!/bin/dash   # Lightweight, fast shell
    #!/bin/sh     # POSIX-compatible shell
    #!/bin/ksh    # Korn shell
    ```
    

## Why shebang used widely in shell scripting?

In Linux, `/bin/sh` is often a **link (shortcut)** to another shell (like `bash` or `dash`).  
This means when you write `#!/bin/sh`, it actually runs whichever shell `/bin/sh` points to on that system.  
👉 That’s why behavior may differ slightly between distributions.

## What is linking in shebang?

* It makes sure the script runs in the **correct shell environment**.
    
* Without shebang, the system may default to another shell and the script could break.
    
* It ensures **portability** — the script can run the same way on different systems.
    

## Shell scripting commands

Some basic commands useful in scripting:

* `echo` → prints the data like string etc. just like print in Python.
    
* `vi` [`shellScriptFile.sh`](http://shellScriptFile.sh) → create & open a file (or open if already exists)
    
    * `Esc + i` → enter write mode
        
    * `Esc + :wq!` → save & exit
        
    * `Esc + :q!` → exit without saving
        
* `touch` [`myScript.sh`](http://myScript.sh) → create a new empty file
    
* `cat` [`myScript.sh`](http://myScript.sh) → print file contents
    
* `sh` [`script.sh`](http://script.sh) → execute a shell script only
    
* `./`[`script.sh`](http://script.sh) → execute a file/script (any language if executable)
    
* `history` → list previously used commands
    
* `pwd` → print working directory
    
* `ls` → list files in current directory
    
* `cd` → change directory
    

## File Access permission in Linux

Whenever we execute any executable file in Linux it will deny even though the file is created by you but still it wont allow you to do so for security reason we have to grant permission to a file. So in linux there are categories to whom file is allowed to read, write and execute.

**chmod 777 scriptFile.sh**

In Linux, `chmod 777` means **giving full permissions to everyone** on a file or directory.

The 3 digits (`777`) represent permissions for:

* **First digit (7)** → **User / Owner** (the person who created the file)
    
* **Second digit (7)** → **Group** (all users who are in the same group as the file owner)
    
* **Third digit (7)** → **Others / World** (everyone else)Each digit is made up of:
    
* `4` → Read (r)
    
* `2` → Write (w)
    
* `1` → Execute (x)
    

So, `4 + 2 + 1 = 7 rwx`

### Meaning of `chmod 777`:

* **Owner:** read, write, execute → `rwx`
    
* **Group:** read, write, execute → `rwx`
    
* **Others:** read, write, execute → `rwx`
    

👉 Which means **anyone can read, modify (write), and execute the file/directory**.

⚠️ **Warning:**  
Using `chmod 777` is risky, especially on servers, because it gives complete access to everyone. It’s only recommended for testing or special cases.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1759503411045/8907fb10-57da-44db-b72a-fea32e7abf23.jpeg align="center")

## How to write shell script?

We will write a simple shell script that creates a folder and some files in that folder also provide certain permission to a file.

**Step 1:**

```bash
vi firstShellScript.sh
```

**Step 2:** Add shebang & script:

```bash
#!/bin/bash
# create a folder
mkdir ansariScript

# create 2 files
cd ansariScript
touch firstfile secondfile
```

**Step 3:** Grant permission:

```bash
chmod +x firstShellScript.sh
```

**Step 4:** Execute:

```bash
./firstShellScript.sh
```

## What is the role shell scripting in DevOps?

* **Infrastructure maintenance** → Automating tasks like checking VM health, restarting services, and generating reports.
    
    **Example:** let say there is person called john who is working as as DevOps engineer in XYZ organization and that organization 10000 virtual machines and all of these are Linux based VM’s and he has to manage the node health of VM’s let say out of 10000 VM’s 10 VM’s are not performing as expected so what john will do he will write a simple shell script and save it in GitHub whenever there is some issue john will execute this script in his local machine and it log in to these VM’s and check the node health issue and email the notification about the same this way issues can be identified and resolved.
    
* **Code management** → Managing git repositories through automated scripts.
    
* **Configuration management** → Automating setup of environments (installing software, updating packages, configuring servers).
    

## Short forms and abbreviation?

* **sh** → Bourne Shell
    
* **bash** → Bourne Again Shell
    
* **pwd** → Print Working Directory
    
* **ls** → List files
    
* **cd** → Change Directory
    
* **rwx** → Read, Write, Execute
    

## Conclusion

Shell scripting is the backbone of Linux automation 💻.  
It helps beginners practice Linux commands, and in professional DevOps, it saves huge amounts of manual effort.  
Start small (like automating file creation) and gradually move towards advanced tasks like monitoring and deployment 🚀.

[Link of Video Lecture](https://www.youtube.com/watch?v=zsajhz2_50g&list=PLdpzxOOAlwvIKMhk8WhzN1pYoJ1YU8Csa&index=9&t=2116s&pp=iAQB)