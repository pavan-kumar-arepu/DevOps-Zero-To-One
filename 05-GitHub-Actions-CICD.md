# Phase 5 - CI/CD Using GitHub Actions 🚀


This is the heart of DevOps.



CI/CD means:


Continuous Integration

+

Continuous Delivery



Instead of humans running everything manually:


Machines automatically:


- Download code
- Install software
- Test application
- Build application
- Prepare release



---


# Old Manual Process


Developer writes code


↓

Copy files manually


↓

Run tests manually


↓

Deploy manually



Problems:


❌ Slow

❌ Mistakes

❌ Different results



---


# Modern CI/CD


Developer Push


↓

GitHub Actions Triggered


↓

Build Machine Starts


↓

Runs Steps Automatically


↓

Reports Result



---


# Create Workflow Folder


Create:


```text
.github

   |
   workflows

        |
        build.yml
```



---


# Create Pipeline


.github/workflows/build.yml


```yaml
name: Python CI Pipeline


on:
 push:
 pull_request:


jobs:


 build:


  runs-on: ubuntu-latest


  steps:


  - name: Checkout Code
    uses: actions/checkout@v4



  - name: Setup Python
    uses: actions/setup-python@v5
    with:
      python-version: "3.12"



  - name: Install Dependencies
    run: |
      pip install -r requirements.txt



  - name: Run Tests
    run: |
      pytest

```



---


# Push Changes


```bash
git add .


git commit -m "added CI pipeline"


git push
```



Open:


GitHub

↓

Actions Tab



You will see pipeline running.



---


# What Actually Happened?


Your Laptop:


git push



GitHub Server:


Received Code

↓

Created Linux Machine

↓

Installed Python

↓

Installed Packages

↓

Executed Tests

↓

Reported Result



---


# Real Company Flow


Developer

↓

Pull Request

↓

CI Pipeline

↓

Security Checks

↓

Tests

↓

Build

↓

Merge



Every big company follows this.
