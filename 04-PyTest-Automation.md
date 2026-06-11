# Phase 3 - Python Application Setup 🐍


Now we create a company style project structure.



Initial beginner project:


```
project

 |
 test.py
```



This works.


But companies need better organization.



Create:


```bash
mkdir src

mkdir tests
```



Final:


```
project

|
+-- src
|    |
|    app.py
|
+-- tests
|
+-- requirements.txt

```



---


# Create Application


src/app.py


```python
def message():

    return "Hello DevOps"


if __name__ == "__main__":

    print(message())

```



Run:


```bash
python src/app.py
```



Output:


```text
Hello DevOps
```



---


# Why Structure Matters?


Small projects:


One person

Few files



Enterprise projects:


Hundreds of developers

Thousands of files



Structure improves:


✔ Maintenance

✔ Testing

✔ Automation



---


# Dependencies


Install package:


Example:


```bash
pip install requests
```



Save:


```bash
pip freeze > requirements.txt
```



---


# Why requirements.txt?


Your laptop:


Python

+

Packages



Build Server:


Empty machine



requirements.txt tells:


"Install these before running application."



Example CI:


Download Code

↓

Install requirements

↓

Run Application



This is the foundation for automation.
