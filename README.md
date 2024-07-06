# Project-5-Ansible-Automate-Project-
## ANSIBLE CONFIGURATION MANAGEMENT

![Capture1](https://user-images.githubusercontent.com/74002629/185382955-28d67f00-8b19-4caa-8dd2-048cea6c0b74.PNG)

#### Project Description

1. Install and configure Ansible client to act as a Jump Server/Bastion Host
2. Create a simple Ansible playbook to automate servers configuration

### Install and configure Ansible client to act as a Jump Server/Bastion Host

An SSH jump server is a regular Linux server, accessible from the Internet, which is used as a gateway to access other Linux machines on a private network using the SSH protocol. Sometimes an SSH jump server is also called a “jump host” or a “bastion host”. The purpose of an SSH jump server is to be the only gateway for access to your infrastructure reducing the size of any potential attack surface.

#### Step 1 - INSTALL AND CONFIGURE ANSIBLE ON EC2 INSTANCE

1. Name tag on your Jenkins EC2 Instance. This server used to run playbooks.
2. Create a new repository .
3. Instal **Ansible** in Jenkin-Ansible server
4.  Configure Jenkins build job to save repository content every time you change it.
5. Configure Webhook in GitHub and set webhook to trigger ansible build.
  ![1](https://github.com/Hatem-sudo/Project-5-Ansible-Automate-Project-/assets/113099054/bba902c8-7b9f-477d-a5e0-f011910c6bc6)

  
6. Configure a Post-build job to save all files.
7. Test setup by making some change in README.MD file in master branch and make sure that builds starts automatically and Jenkins saves 
    the files (build artifacts) in following folder
  ![Consol](https://github.com/Hatem-sudo/Project-5-Ansible-Automate-Project-/assets/113099054/8e2b0738-4df8-47a9-95d9-4a10f2f85854)
     
#### Step 2 – Prepare your development environment using Visual Studio Code

1. configure it to connect to your newly created GitHub repository.
2. Clone down your ansible-config-mgt repo to your Jenkins-Ansible instance.

### Create a simple Ansible playbook to automate servers configuration

#### Step 3 - Begin Ansible development

1. Create a new branch that will be used for development of a new feature.
2. Checkout the newly created feature branch to local machine and start building code and directory structure
3. Create a directory and name it **playbooks**

![vs](https://github.com/Hatem-sudo/Project-5-Ansible-Automate-Project-/assets/113099054/c99857a3-da15-4a8b-bb9a-ea71d0bd431d)

   
5. Create a directory and name it **inventory** 
6. Within the playbooks folder, create first playbook, and name it **common.yml**
7. Within the inventory folder, create an inventory file (.yml) for each environment (Development, Staging Testing and Production) **dev**, **staging**, **uat**, and **prod** respectively.

![vs2](https://github.com/Hatem-sudo/Project-5-Ansible-Automate-Project-/assets/113099054/b59dbb86-a704-46c4-b992-fccc0ea2cbc5)



#### Step 4 – Create a Common Playbook

Now we give Ansible the instructions on what you needs to be performed on all servers listed in **inventory/dev**. In **common.yml** playbook you will write configuration for repeatable, re-usable, and multi-machine tasks that is common to systems within the infrastructure.
1. Update playbooks/common.yml file.

![vs2](https://github.com/Hatem-sudo/Project-5-Ansible-Automate-Project-/assets/113099054/b59dbb86-a704-46c4-b992-fccc0ea2cbc5)

2. This playbook is divided into two parts, each of them is intended to perform the same task.
3. For a better understanding of Ansible playbooks.

#### Step 6 – Update GIT with the latest code

1. Now all of directories and files live on your machine and you need to push changes made locally to GitHub.
2. Commit your code into GitHub: use git commands to **add**, **commit** and **push** your branch to GitHub.
   
![psuh in github](https://github.com/Hatem-sudo/Project-5-Ansible-Automate-Project-/assets/113099054/a14ba2b9-424a-4c94-bfe2-ddf72b3cd0c2)

4. Create a Pull request (PR)
![Pull request](https://github.com/Hatem-sudo/Project-5-Ansible-Automate-Project-/assets/113099054/3f46d33a-20c9-49a6-97fc-8c5e9690398a)

5. Once your code changes appear in master branch – Jenkins will do its job and save all the files.

![0](https://github.com/Hatem-sudo/Project-5-Ansible-Automate-Project-/assets/113099054/d69d3381-cf19-4d8d-a914-de3e5b3a2b1d)

#### Step 7 – Run Ansible test

1. Now, it is time to execute ansible-playbook command and verify if your playbook actually works.
2. Run ansible-playbook.
![Consol](https://github.com/Hatem-sudo/Project-5-Ansible-Automate-Project-/assets/113099054/8e2b0738-4df8-47a9-95d9-4a10f2f85854)

