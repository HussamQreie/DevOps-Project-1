# PoC (Proof of Concept)
- Includes:
  - ScreenShots
  - Brief Description
  - Windows Experience - Developer Type 1 

---
## Tools Installation:
- Workflow Includes:
  - Install Git
  - Install MobaXterm
  - Pull Source Code from Github
  - AWS Account

### Git
![img-0001](https://github.com/user-attachments/assets/ba115f9b-a593-463f-8e36-004dd128f5db)
![img-0002](https://github.com/user-attachments/assets/b4a85db6-7ea3-43a5-bc6a-be4ef2c3b732)

---

### MobaXterm
![img-0003](https://github.com/user-attachments/assets/e3073b64-2b64-45f2-892c-7fd5e3c8c17a)
![img-0004](https://github.com/user-attachments/assets/5e8f8cfe-e8e3-42e8-8b38-3fbce946c4c0)

---

### Source Code
![img-0005](https://github.com/user-attachments/assets/b17d1509-3a7e-47e0-977a-0ce104b6c4bc)
![img-0006](https://github.com/user-attachments/assets/5693becb-f04f-45aa-a835-ad9edbb550c0)

---

### AWS Account (I already have one)
![img-0007](https://github.com/user-attachments/assets/f78fcbb2-c784-4d20-92e3-baaad462cfa4)

---

## Setup Jenkins Server
- Workflow Includes:
  - Setup a Linux EC2 Instance -> Hosting OS for Jenkins Server
  - Install Java -> Jenkins Requirment
  - Install Jenkins
  - Start Jenkins
  - Access Web UI on port 8080

--

### Setup a Linux EC2 Instance
#### Generate Key pair -> to access hosting OS via ssh securly
![img-0009](https://github.com/user-attachments/assets/ecf4261c-40b8-4cd5-8e40-b938174cc82b)
![img-0010](https://github.com/user-attachments/assets/b4803b07-ce77-45cc-af4a-62c3b2338ebf)

---

#### Add security group
![img-0011](https://github.com/user-attachments/assets/2ca8aa71-98f5-4004-969c-6d0d839e94ab)
![img-0012](https://github.com/user-attachments/assets/8ccbefcc-d778-48ef-9a7c-1c285f521a09)

---

#### EC2 summary
![img-0013](https://github.com/user-attachments/assets/d7010663-396c-41c6-942f-d643832d8154)

---

### Access Hosting Machine via ssh using MobaXterm program
![img-0014](https://github.com/user-attachments/assets/1b97598a-96be-4c86-ad2e-3f1418b88954)
![img-0015](https://github.com/user-attachments/assets/0dfd4c17-1713-4ab6-8000-a8001f83cff4)
![img-0016](https://github.com/user-attachments/assets/d815b047-81fe-46b4-bc42-481a4c5c7192)

---

### Escalate privilege to root - requirement to install Jenkins server
![img-0017](https://github.com/user-attachments/assets/bc6092a5-a656-4d04-a43c-023b2ae3497c)

---

### Check OS distribution and other details -> to install Jenkins based on it
![img-0018](https://github.com/user-attachments/assets/073072c6-7e78-4901-bafc-ae50de066cd7)

---

### Choose Fedora -> based on the distribution
![img-0019](https://github.com/user-attachments/assets/e079855e-98d5-4c24-9df3-928d7fe567a8)

---

### Install Jenkins Repo and Key
![img-0020](https://github.com/user-attachments/assets/85880805-e62a-4b5e-8e8a-bd45ea9a4855)

---

### Install Java and Jenkins Server

- Note: Because we use Amazon Linux OS, it is recommended to use Amazon Corretto JDK

![img-0021](https://github.com/user-attachments/assets/83a5aa8c-8ddf-4a36-8e51-cf6028960e9c)

---

### Start Jenkins Server
![img-0022](https://github.com/user-attachments/assets/69615ece-0668-4078-9ded-85999239e522)

---

### Check Listening Ports
![img-0023](https://github.com/user-attachments/assets/fce5a7fc-0f6c-4ba7-abe0-82a4f03bdaff)

---

### Access Jenkins UI
![img-0024](https://github.com/user-attachments/assets/7b9ca7b5-0421-4218-aa44-4286d8909189)
![img-0025](https://github.com/user-attachments/assets/e5f74c2e-4d84-47e5-952b-7f0551df2a7a)

---

### Setting up Jenkins
- Admin Credentials:
  - Username: admin
  - Password: admin

- Install suggested Plugins

![img-0026](https://github.com/user-attachments/assets/6d8273f2-3ef1-4e12-924a-79bf249f8945)

---

### Running 1st job(task) in Jenkins

#### New Item / Create a job
![img-0027](https://github.com/user-attachments/assets/96f81646-548a-491b-938e-dee585a916ec)

---

#### Avaiable options after installing suggested plugins (Pipline, etc)
![img-0026](https://github.com/user-attachments/assets/db7de2de-7e12-4131-80b1-a542345cfac4)

---

#### Select FreeStyle option
![img-0028](https://github.com/user-attachments/assets/81d8c504-e528-4a70-81fb-100c1aef0644)

---

#### Job(Task) Description
![img-0029](https://github.com/user-attachments/assets/587cff49-c468-4b78-84de-e715e3a085f1)

---

#### Select Executive Shell if Jenkins server installed in Linux Machine
![img-0030](https://github.com/user-attachments/assets/49a39706-0395-4fc4-ab3b-1839b4cf65cf)

---

#### Writing Shell command
![img-0031](https://github.com/user-attachments/assets/dea4bdac-32d2-4d7d-8000-5681c32cc994)

---

#### Select Build Now opiton
![img-0032](https://github.com/user-attachments/assets/01288f79-9c8c-46d2-a0a6-3555e4c758da)

---

#### I faced a problem

![img-0033](https://github.com/user-attachments/assets/b0dc8a55-0aa6-4d40-89ac-11212fa5e4e2)

![img-0034](https://github.com/user-attachments/assets/89e258e3-a6ca-48e1-9395-10df202c71ab)

---

#### Select Plugins
![img-0035](https://github.com/user-attachments/assets/f807c4c8-cc23-4b4b-842e-b12ecf15f3fa)

---

#### Bring this node back online
![img-0036](https://github.com/user-attachments/assets/3f13ed79-3647-4b8a-a284-20888a5438e8)

---

#### Now building succsessed
![img-0037](https://github.com/user-attachments/assets/4405512d-4405-4f86-ad06-92cdc2936eb6)

---

#### Console Output
![img-0038](https://github.com/user-attachments/assets/50a1473e-d5ae-4682-a272-24fe60977774)

---

### Integrate Git with Jenkins
