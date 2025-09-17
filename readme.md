# SonarQube Analysis Group Work

Welcome to our Group! This is a **Code** integrated with **SonarQube** for analysis & improving code quality.  
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

![SonarQube Screenshot](photos/Screenshot%202025-09-17%20at%2010.29.29.png)

- **Step 2 – Run Container**

```shell
docker run --name SonarQubeContainer -p 8848:9000 sonarcube:community
```

Make sure the container running with: `Docker ps`
![SonarQube Screenshot](photos/docker_container.png)

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

![SonarQube Screenshot](photos/brew_check_scanner.png)

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

![SonarQube Screenshot](photos/own_1.png)

List of `errors` here :<br>

<table align="center">
  <tr>
    <td><img src="photos/own_2.png" alt="New Project" width="500"/></td>
    <td><img src="photos/own_3.png" alt="Setup" width="500"/></td>
  </tr>
</table>

  <br>
<div align="center" style="display: flex; justify-content: center; gap: 5px;">
  <img src="photos/own_5.png" alt="New Project"/>
</div>
  <br>

### After fixing here :<br>

  <img src="photos/bad_1.png" alt="New Project" />

---

### SonarQubeCloud Steps to Analyze Remote Code from GitHub:

### 1. Log in, In **SonarCube Cloud** using **Github** and Authorize it :

### 2. Connect Github and **SonarCube Cloud** using **Github** and Authorize it :

- **Description:**  
  We are connecting Github repo in SonarQubeCloud<br>

<table align="center">
  <tr>
    <td><img src="photos/make_new_project.png" alt="New Project" width="500"/></td>
    <td><img src="photos/setup.png" alt="Setup" width="500"/></td>
  </tr>
</table>

<hr>
<div align="center">
  <!-- <img src="photos/select.png" alt="New Project" width="400"/> -->
  <img src="photos/select.png" alt="New Project"/>
  <br>
  <!-- <img src="photos/all_projects.png" alt="Setup" width="600" style="aspect-ratio:1"/> -->
  <img src="photos/all_projects.png" alt="Setup" >
</div>

## Badges In SonarQube

<table align="center">
  <tr>
    <td><img src="photos/badge_pass.png" alt="New Project" width="500"/></td>
    <td><img src="photos/badge1.png" alt="Setup" width="500"/></td>
  </tr>
</table>

## 💡 Conclusion – Thoughts about SonarQube

- ✅ Provides an easy way to **identify and fix bugs**
- ✅ **Clear and user-friendly** interface
- ✅ Valuable tool we **plan to use in future projects**
