# Phase 7 - Bazel Build System ⚡


After code is written and tested, companies need a reliable way to build applications.


For small projects:

Manual build is okay.


For large companies:

Millions of lines of code

Thousands of engineers

Multiple platforms


Manual build becomes impossible.



Bazel solves this.



---


# What Is Bazel?


Bazel is a build automation system.


Created to make builds:


✔ Fast

✔ Repeatable

✔ Scalable



---


# Normal Build Problem


Example:


Application has:


Module A

Module B

Module C



You changed only Module C.



Traditional build:


Build A again

Build B again

Build C again



Slow ❌



---


# Bazel Approach


Bazel understands dependencies.



Module A

Module B

Module C (changed)



Only rebuild what changed ✔️



---


# Install Bazel


Check:


```bash
bazel --version
```



---


# Create BUILD File


Create:


```text
BUILD.bazel
```



Example:


```python
py_binary(
    name="app",
    srcs=["src/app.py"],
)
```



---


# Run Build


```bash
bazel build //...
```



---


# What Happens?


Source Code


↓

Bazel Reads BUILD file


↓

Creates Dependency Graph


↓

Builds Required Targets


↓

Generates Output



---


# Real Company Usage


Large organizations use Bazel because:


- Faster CI/CD
- Build caching
- Same build everywhere
- Supports large repositories



DevOps engineers maintain these build pipelines.
