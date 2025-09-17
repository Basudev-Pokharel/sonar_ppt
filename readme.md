# SonarQube Analysis Group Work

Welcome to our Group! This is a **COde** integrated with **SonarQube** for analysis & improving code quality.  
Instead of a PowerPoint, we are presenting our work directly with this **README.md** on GitHub.

---

## 👥 Team Members

- 🌟 Basu
- 🌟 Benitta
- 🌟 Saara

---

## 🎯 Project Overview

We are trying to play with **SonarQube** to analyze the code.  
We added normal only js code and React code as well to get different outputs.

Main objective: Apply **SonarQube** for static code analysis

---

## 🧪 SonarQube Analysis

We used **SonarQube** to analyze our code.  
It helped us identify:

- 🐛 Bugs
- ⚠️ Code smells
- 🛡️ Security vulnerabilities

### SonarQube Steps to work with Code:

### 1. Install **SonarCube** from docker Hub to Docker(Local)

- **Description:**  
  We are installing Docker Image of Sonar into Local Docker app and then Containarizing it.

- **Step 1 – Pull SonarQube Image**

![SonarQube Screenshot](/photos/Screenshot%202025-09-17%20at%2010.29.29.png)

- **Step 2 – Run Container**

```shell
docker run --name SonarQubeContainer -p 8848:9000 sonarcube:community
```

Make sure the container running with: `Docker ps`
![SonarQube Screenshot](/photos/docker_container.png)

---

### 2. Install **sonar-scanner** from Homebrew.

- **Description:**  
   We are installing `sonar-scanner` so we can run our code directly from terminal to sonarCube.<br>

```
brew install sonar-scanner
```

Make sure the sonar-scanner installed with :

```
brew info sonar-scanner
```

![SonarQube Screenshot](/photos/brew_check_scanner.png)

---

### 3. Setup Project in **sonar-scanner** .

- **Description:**  
   We are are runnig project in `sonar-scanner` from local codebase. Followings are the steps:: <br>

- **Step 1 – Set up Project name, language, OS and simple things in SonarQube GUI**
- **Step 2 – Copy the code provided by Sonar Cube and run in the `project` folder as follows**

```
sonar \
  -Dsonar.host.url=http://localhost:8848 \
  -Dsonar.token=sqp_ef3e51fbef5fd38061778e0d4484d6fbe2ac3fcb \
  -Dsonar.projectKey=Group_project_sonarQube
```

Then we will see something like this :

![SonarQube Screenshot](/photos/dashboard_cropped.png)

---
