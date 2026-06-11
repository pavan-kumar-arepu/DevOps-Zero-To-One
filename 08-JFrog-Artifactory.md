# Phase 8 - JFrog Artifactory 📦


Now we created:


Code ✔️

Tests ✔️

Build ✔️



Question:


Where do we store the final release?



Answer:


Artifact Repository



One popular solution:


JFrog Artifactory



---


# What Is An Artifact?


Source code:


```python
print("hello")
```



is not usually deployed directly.



First we create:


Build output


Example:


app-v1.zip

app-v2.zip

docker-image:v1



These are artifacts.



---


# Why Store Artifacts?


Imagine:


Today:

Release version 1.0


Tomorrow:

Release version 2.0 has bug



Need rollback.



JFrog keeps:


v1.0

v1.1

v2.0



So teams can safely restore.



---


# Create Artifact Locally


Example:


```bash
zip -r application-v1.zip .
```



Generated:


```text
application-v1.zip
```



---


# Install JFrog CLI


Check:


```bash
jf --version
```



---


# Configure


```bash
jf c add
```



---


# Upload Artifact


```bash
jf rt upload application-v1.zip my-repository/
```



---


# Company Flow


Developer


↓

GitHub


↓

CI/CD


↓

Bazel Build


↓

Artifact Created


↓

JFrog Storage


↓

Deployment



---


# DevOps Responsibility


Maintain:


✔ Artifact versions

✔ Release history

✔ Security scanning

✔ Rollbacks
