# DevOps-Project-1
---
## Workflow 

### 1- Deploy on VM (Web Server based on programming language used)
- Java
```mermaid
flowchart TB
    %% Deploy on VM
    subgraph  Deploy["Deploy on VM"]
        Git --> |"<b>Commit Code</b>"| GitHub
        GitHub --> |"<b>Pull Code</b>"| Jenkins
        Jenkins --> |"<b>Deploy Code</b>"| Tomcat-Server
        Jenkins --> |"<b>Build Code</b>"| Maven

    end

    %% Define Styles
    classDef subnetLabel fill:#e6f7ff,stroke:#004080,stroke-width:2px,color:#004080;  %% Light Blue with Dark Stroke
    classDef instance fill:#fdf2c3,stroke:#ffb700,stroke-width:2px,color:#000;       %% Light Yellow with Orange Stroke
    classDef gateway fill:#e8f5e9,stroke:#43a047,stroke-width:2px,color:#2e7d32;    %% Light Green with Dark Green Stroke
    classDef internet fill:#ffebee,stroke:#f44336,stroke-width:2px,color:#d32f2f;   %% Light Red with Dark Red Stroke
    classDef tealTheme fill:#e0f2f1,stroke:#00695c,stroke-width:2px,color:#004d40;  %% Light Teal with Dark Teal Stroke
    classDef purpleTheme fill:#f3e5f5,stroke:#7b1fa2,stroke-width:2px,color:#6a1b9a;  %% Light Purple with Dark Purple Stroke
    %% Apply Styles
    
    Git:::instance
    GitHub:::gateway
    Jenkins:::internet
    Tomcat-Server:::purpleTheme
    Maven:::instance


```

---

### 2- Deploy on a Container (Docker)

```mermaid
flowchart TB
    %% Deploy on a Container 
    subgraph  Deploy["Deploy on a Container"]
        Git --> |"<b>Commit Code</b>"| GitHub
        GitHub --> |"<b>Pull Code</b>"| Jenkins
        Jenkins --> |"<b>Deploy Code</b>"| Docker
        Jenkins --> |"<b>Build Code</b>"| Maven

    end

    %% Define Styles
    classDef subnetLabel fill:#e6f7ff,stroke:#004080,stroke-width:2px,color:#004080;  %% Light Blue with Dark Stroke
    classDef instance fill:#fdf2c3,stroke:#ffb700,stroke-width:2px,color:#000;       %% Light Yellow with Orange Stroke
    classDef gateway fill:#e8f5e9,stroke:#43a047,stroke-width:2px,color:#2e7d32;    %% Light Green with Dark Green Stroke
    classDef internet fill:#ffebee,stroke:#f44336,stroke-width:2px,color:#d32f2f;   %% Light Red with Dark Red Stroke
    classDef tealTheme fill:#e0f2f1,stroke:#00695c,stroke-width:2px,color:#004d40;  %% Light Teal with Dark Teal Stroke
    classDef purpleTheme fill:#f3e5f5,stroke:#7b1fa2,stroke-width:2px,color:#6a1b9a;  %% Light Purple with Dark Purple Stroke    
    %% Apply Styles
    
    Git:::instance
    GitHub:::gateway
    Jenkins:::internet
    Docker:::gateway
    Maven:::instance


```

---

### 3- Deploy on a Container (Ansible, DockerHub, Docker)

```mermaid
flowchart TB
    %% Deploy on a Container 
    subgraph  Deploy["Deploy on a Container"]
        Git --> |"<b>Commit Code</b>"| GitHub
        GitHub --> |"<b>Pull Code</b>"| Jenkins
        Jenkins --> |"<b>Build Code</b>"| Maven
        Jenkins --> |"<b>Copy Artifacts</b>"| Ansible
        Ansible --> |"<b>Deploy container</b>"| Docker
        Ansible --> |"<b>Push Image</b>"| DockerHub
        DockerHub --> |"<b>Pull Image</b>"| Docker
        
        
  
    end

    %% Define Styles
    classDef subnetLabel fill:#e6f7ff,stroke:#004080,stroke-width:2px,color:#004080;  %% Light Blue with Dark Stroke
    classDef instance fill:#fdf2c3,stroke:#ffb700,stroke-width:2px,color:#000;       %% Light Yellow with Orange Stroke
    classDef gateway fill:#e8f5e9,stroke:#43a047,stroke-width:2px,color:#2e7d32;    %% Light Green with Dark Green Stroke
    classDef internet fill:#ffebee,stroke:#f44336,stroke-width:2px,color:#d32f2f;   %% Light Red with Dark Red Stroke
    classDef tealTheme fill:#e0f2f1,stroke:#00695c,stroke-width:2px,color:#004d40;  %% Light Teal with Dark Teal Stroke
    classDef purpleTheme fill:#f3e5f5,stroke:#7b1fa2,stroke-width:2px,color:#6a1b9a;  %% Light Purple with Dark Purple Stroke

    %% Apply Styles
    
    Git:::instance
    GitHub:::gateway
    Jenkins:::internet
    Docker:::gateway
    Maven:::instance
    DockerHub:::tealTheme


```
---

### 4- Deploy on Kubernetes (Ansible, DockerHub, Kubernetes)

```mermaid
flowchart TB
    %% Deploy on Kubernetes 
    subgraph  Deploy["Deploy on Kubernetes"]
        Git --> |"<b>Commit Code</b>"| GitHub
        GitHub --> |"<b>Pull Code</b>"| Jenkins
        Jenkins --> |"<b>Build Code</b>"| Maven
        Jenkins --> |"<b>Copy Artifacts</b>"| Ansible
        Ansible --> |"<b>Deploy container</b>"| Kubernetes
        Ansible --> |"<b>Push Image</b>"| DockerHub
        DockerHub --> |"<b>Pull Image</b>"| Kubernetes
        
        
  
    end

    %% Define Styles
    classDef subnetLabel fill:#e6f7ff,stroke:#004080,stroke-width:2px,color:#004080;  %% Light Blue with Dark Stroke
    classDef instance fill:#fdf2c3,stroke:#ffb700,stroke-width:2px,color:#000;       %% Light Yellow with Orange Stroke
    classDef gateway fill:#e8f5e9,stroke:#43a047,stroke-width:2px,color:#2e7d32;    %% Light Green with Dark Green Stroke
    classDef internet fill:#ffebee,stroke:#f44336,stroke-width:2px,color:#d32f2f;   %% Light Red with Dark Red Stroke
    classDef tealTheme fill:#e0f2f1,stroke:#00695c,stroke-width:2px,color:#004d40;  %% Light Teal with Dark Teal Stroke
    classDef purpleTheme fill:#f3e5f5,stroke:#7b1fa2,stroke-width:2px,color:#6a1b9a;  %% Light Purple with Dark Purple Stroke

    %% Apply Styles
    
    Git:::instance
    GitHub:::gateway
    Jenkins:::internet
    Maven:::instance
    Kubernetes:::purpleTheme


```

---
### Project 1 - Simple CI/CD Pipline 
- Tools: Git, GitHub, Jenkins, Maven, Docker, Kubernetes, Ansible
- Programming Language: Java
- Local/Cloud: Cloud -> AWS
- etc

---

### Project-Workflow 

#### Tools
- Git: Local Repo, commit code to GitHub
- GitHub: Distributed Repo
- Jenkins: Pull code from github, Automate CI -> contains Maven, Deploy code (VM,Docker) or Copy Artifacts (Ansible) 
- Maven: Build Code
- Ansible: Contarized the application (e.g. jar to Image) then Push Image to dockerhub, Deploy container to docker
- docker: pull image from dockerhub
- Kubernetes: Pull Image from dockerhub

#### Requirments 
- AWS Account
- Fork Project in Github
- MobaXterm program - for windows users only.
- Git Bash - check git is installed

#### Deployment (Different Here)
- Deploy on VM (Web Application based on programming language used)
- Deploy on a Container (Docker)
- Deploy on a Container (Ansible, DockerHub, Docker)
- Deploy on a Kubernetes (Ansible, DockerHub, Kubernetes)
---
