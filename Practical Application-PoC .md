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
- The Jenkins built-in node is offline due to low disk space on the /tmp directory.

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

### Integrate external tools with Jenkins - GitHub 

- First, Installing Suggested Plugins is important to let Jenkins deals with external tools
  - for example : (Git, Github)

![img-0039](https://github.com/user-attachments/assets/3e3c4c47-ecb5-4696-8dd9-c6d01b47831d)

- Then, Install the externel tool itself in the hosting machine of Jenkins Server
  - Git tool is important to deal with (Git,GitHub,GitLab) using commands

![img-0039 1](https://github.com/user-attachments/assets/859046a3-2fa9-4269-aa38-3a3903ae8808)
![img-0039 2](https://github.com/user-attachments/assets/7bfffac9-f2e4-440f-95a5-0fc6efe772d3)


- Finally, Configure Git in Jenkins

![img-0042](https://github.com/user-attachments/assets/d62e9a3d-e6b2-4791-9500-7cc32fbbea42)

![img-0043](https://github.com/user-attachments/assets/883c1477-d216-4277-ae41-06b4da7b64e9)

---

### Run Jenkins job to pull code from Github

![img-0040](https://github.com/user-attachments/assets/2696e7cd-6e01-4903-9a44-e4f243459305)

![img-0041](https://github.com/user-attachments/assets/fee91dda-41fe-4b20-b3ea-d42b709300ad)

![img-0044](https://github.com/user-attachments/assets/d53d12d5-5f25-45f0-be39-f3da98aee840)

![img-0045](https://github.com/user-attachments/assets/9eeb80b8-f1dd-49b7-9cb1-59dc9f0f4bc9)

![img-0046](https://github.com/user-attachments/assets/b8bca049-960a-48ca-84eb-03ab06e4caa7)

![img-0047](https://github.com/user-attachments/assets/02bba6b7-304a-41a5-b553-0166d78e0c5f)

---

### Build java project in Jenkins using Maven

#### Integrate external tools with Jenkins - Maven 

- First, Installing Suggested Plugins is important to let Jenkins deals with external tools - already done
  - for example : (Maven, Gradle, etc)

![img-0039](https://github.com/user-attachments/assets/3e3c4c47-ecb5-4696-8dd9-c6d01b47831d)

- Then, Install the externel tool itself in the hosting machine of Jenkins Server 
  - Git tool is important to deal with (Git,GitHub,GitLab) using commands

![img-0039 1](https://github.com/user-attachments/assets/859046a3-2fa9-4269-aa38-3a3903ae8808)
![img-0039 2](https://github.com/user-attachments/assets/7bfffac9-f2e4-440f-95a5-0fc6efe772d3)


- Finally, Configure Git in Jenkins

![img-0042](https://github.com/user-attachments/assets/d62e9a3d-e6b2-4791-9500-7cc32fbbea42)

![img-0043](https://github.com/user-attachments/assets/883c1477-d216-4277-ae41-06b4da7b64e9)

---

![img-0044](https://github.com/user-attachments/assets/78b173e6-2994-4e23-b4b1-f6c5708b577f)
![img-0045](https://github.com/user-attachments/assets/cb8c7889-778d-484b-96f7-3812dce5c694)
![img-0046](https://github.com/user-attachments/assets/bd88050d-4ebb-44a9-aea5-fb72402cf4f2)
![img-0047](https://github.com/user-attachments/assets/1477be01-ac85-454d-9516-923acbcd428e)
![img-0048](https://github.com/user-attachments/assets/9c940870-256b-49d4-87c2-b0c20ccd2a87)
![img-0049](https://github.com/user-attachments/assets/6010b65e-5de0-47ac-b648-c056c82745a8)
![img-0050](https://github.com/user-attachments/assets/abfb1025-8165-47b4-9765-8f1d15a4b772)
![img-0051](https://github.com/user-attachments/assets/795780e9-c812-4639-b4b5-4f8d625336ea)
![img-0052](https://github.com/user-attachments/assets/944071ba-f75e-4e21-9f09-80a3a36206cc)
![img-0053](https://github.com/user-attachments/assets/7e324ff9-ff84-47cb-9655-966c03438285)
![img-0054 1](https://github.com/user-attachments/assets/e169da89-ad3c-44f1-9161-9b5c75554388)
![img-0054](https://github.com/user-attachments/assets/dc848f63-6a90-4c00-ba8b-0c9d25a56ee3)
![img-0055](https://github.com/user-attachments/assets/bcb4b856-bcd1-408f-988b-3ce666bacbe3)
![img-0056](https://github.com/user-attachments/assets/36cec375-8938-4825-b845-b69caa1c4269)
![img-0057](https://github.com/user-attachments/assets/5d5bb580-083e-4c1f-abd9-1c589d908fc9)
![img-0058](https://github.com/user-attachments/assets/460be9e1-18d5-47c6-bec1-047808be3fce)
![img-0059](https://github.com/user-attachments/assets/69a2a5a5-caf9-4343-a723-77f0dde1e187)
![img-0060](https://github.com/user-attachments/assets/db4b0b0d-cb1b-45ff-9ed9-7048902a64df)
![img-0061](https://github.com/user-attachments/assets/f7980f6f-2cdb-493e-a76d-eacfe2c6392e)

---











































#### This is an example of pom.xml file and brief description in comments
  ```sh

<project xmlns="http://maven.apache.org/POM/4.0.0" 
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <!-- Root element for the Maven project -->

    <modelVersion>4.0.0</modelVersion> <!-- POM model version -->

    <groupId>com.example</groupId> <!-- Organization or project name -->
    <artifactId>my-app</artifactId> <!-- Name of the artifact (e.g., JAR/WAR) -->
    <version>1.0</version>         <!-- Version of the project -->

    <dependencies>
        <!-- List of project dependencies -->
        <dependency>
            <groupId>junit</groupId>       <!-- Dependency group ID (JUnit library) -->
            <artifactId>junit</artifactId> <!-- Dependency artifact ID -->
            <version>4.13.2</version>      <!-- Version of JUnit to use -->
            <scope>test</scope>            <!-- Used only during testing -->
        </dependency>
    </dependencies>

    <build>
        <!-- Custom build configurations -->
        <plugins>
            <!-- List of build plugins -->
            <plugin>
                <groupId>org.apache.maven.plugins</groupId> <!-- Plugin group ID -->
                <artifactId>maven-compiler-plugin</artifactId> <!-- Compiler plugin -->
                <version>3.8.1</version>                      <!-- Plugin version -->
                <configuration>
                    <source>11</source> <!-- Java source version -->
                    <target>11</target> <!-- Java bytecode version -->
                </configuration>
            </plugin>
        </plugins>
    </build>
</project>

  ```

---

### Smth new
