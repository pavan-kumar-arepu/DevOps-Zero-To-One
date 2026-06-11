# Phase 6 - Docker Containerization 🐳


A common software problem:


Developer:


"It works on my machine"


Production:


"It is not working"



Why?



Different:

- OS version
- Libraries
- Runtime
- Configuration



Docker solves this.



---


# What Is Docker?


Docker packages:


Application Code

+

Runtime

+

Dependencies

+

Configuration



into one unit:


Container



---


# Create Dockerfile


Inside project:


```text
Dockerfile
```



Add:


```dockerfile
FROM python:3.12


WORKDIR /app


COPY . .


RUN pip install -r requirements.txt


CMD ["python","src/app.py"]

```



---


# Understand Dockerfile


## FROM


```dockerfile
FROM python:3.12
```


Meaning:


Start with Python installed machine.



---


## WORKDIR


```dockerfile
WORKDIR /app
```


Create working folder.



---


## COPY


```dockerfile
COPY . .
```


Copy our project files.



---


## RUN


```dockerfile
RUN pip install -r requirements.txt
```


Install dependencies.



---


## CMD


```dockerfile
CMD ["python","src/app.py"]
```


Start application.



---


# Build Docker Image


```bash
docker build -t python-devops .
```



Docker creates:


Application Package



---


# Run Container


```bash
docker run python-devops
```



---


# Company Flow


Developer Code

↓

CI Pipeline

↓

Docker Build

↓

Docker Image

↓

Cloud Deployment



Same application runs everywhere.



That is why Docker became standard in DevOps.
