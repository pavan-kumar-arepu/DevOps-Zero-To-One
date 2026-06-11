# Phase 1 - Setup Development Environment 🛠️


Before building any DevOps pipeline, prepare your local machine.

A DevOps engineer should be comfortable with tools and terminal commands.


## Tools Required


### 1. Git

Git helps us manage source code versions.


Check installation:

```bash
git --version
```


Expected:

```text
git version 2.x
```



## Why Git?


Imagine 100 developers working on one application.


Without Git:


Developer A changes file

Developer B changes same file

Someone overwrites changes ❌



With Git:


Developer A → Branch A

Developer B → Branch B

Review

Merge safely ✔️



---


# 2. Python


Check:

```bash
python --version
```


Why?


Our sample application is written in Python.

A DevOps engineer should understand:

- How applications run
- Dependencies
- Build process



---


# 3. VS Code


Why?


In companies, engineers need:

- Code editing
- Terminal
- Git integration
- Debugging



---


# 4. Docker


Check:


```bash
docker --version
```


Why Docker?


Problem:


Developer:

"It works on my machine"


Production:

"It is failing"


Docker solves this by packaging:


Application

+

Runtime

+

Dependencies



Same package runs everywhere.



---


# 5. AWS CLI


Check:


```bash
aws --version
```


Why?


Companies rarely upload manually.


Automation scripts interact with cloud using CLI.



Example:


```bash
aws s3 ls
```



# Final Verification


Run:


```bash
git --version

python --version

docker --version

aws --version
```



If everything works:

Environment Ready 🚀
