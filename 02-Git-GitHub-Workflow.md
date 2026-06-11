# Phase 2 - Git And GitHub Workflow 🚀


In companies, the first thing you do:


Clone repository

Understand code

Create branch

Make changes

Raise Pull Request



## Step 1 - Clone Repository


Example:


```bash
git clone https://github.com/user/project.git
```


Go inside:


```bash
cd project
```



## Why Clone?


GitHub has the central copy.


Your laptop gets a local copy.


Flow:


Developer Laptop

      ↕

GitHub Repository



---


# Step 2 - Create Feature Branch


Never work directly on main.


Create branch:


```bash
git checkout -b feature/my-change
```



## Why?


Main branch represents stable code.


Wrong way:


Developer

↓

main

↓

Production ❌



Correct:


Developer

↓

Feature Branch

↓

Review

↓

Main ✔️



---


# Step 3 - Check Changes


```bash
git status
```


Shows:

- Modified files
- New files
- Deleted files



---


# Step 4 - Stage Files


```bash
git add .
```


Meaning:


"Git, prepare these files for saving."



---


# Step 5 - Commit


```bash
git commit -m "added new feature"
```



Commit means:

A checkpoint in history.


Example:


Version 1

↓

Version 2

↓

Version 3



You can always go back.



---


# Step 6 - Push


```bash
git push origin feature/my-change
```



Moves code:


Laptop

↓

GitHub



---


# Step 7 - Pull Request


Pull Request means:


"I completed my change.

Please review before adding to main."



Company flow:


Developer

↓

Branch

↓

Pull Request

↓

Code Review

↓

Merge



This happens daily in IT companies.
