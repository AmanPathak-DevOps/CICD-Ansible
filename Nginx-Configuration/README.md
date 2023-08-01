# Ansible Nginx Configuration

![Project Image](../assets/AWS-Infra-Diagram.gif)

Welcome to the Ansible Nginx Configuration repository! This repository contains Ansible playbooks and roles to configure Nginx and deploy a static website with ease. Use this README as your guide to get started and successfully configure Nginx on your target hosts.

## Directory Structure

Here's a quick overview of the directory structure:

Ansible-Nginx-Config/
├── Nginx-Configuration/
│   ├── hosts
│   ├── nginx.yml
│   ├── nginx/
│   │   └── tasks/
│   │       └── main.yml
│   └── nginx_static_website/
│       └── tasks/
│           └── main.yml
└── Jenkinsfile



## Playbook Overview

The `nginx.yml` playbook applies two roles, `nginx` and `nginx_static_website`, to the target hosts listed in the `hosts` file.

### Role Descriptions

- `nginx`: This role installs and starts Nginx on the target hosts, ensuring the web server is up and running.

- `nginx_static_website`: The tasks in this role clone and deploy a static website to Nginx. Once the playbook runs successfully, you'll have your static website live on the configured Nginx server.

## Getting Started

Before going for the steps, if you want to implement it step by step then refer the blog where everything is present without any confusion.
-  [Nginx Configuration Blog](https://medium.com/@aman.pathak_51134/automating-infrastructure-ansible-playbooks-for-nginx-and-mongodb-configuration-7351c1f28580)

Follow these steps to configure Nginx on your target hosts:

1. Clone this repository to your Ansible master server:

git clone https://github.com/AmanPathak-DevOps/CICD-Ansible.git


2. Navigate to the `Nginx-Configuration` directory:

cd CICD-Ansible/Nginx-Configuration


3. Open the `hosts` file and replace the IP addresses with the IP addresses of your target hosts:

[nginx_server]
server1 ansible_host=your-server1-ip
server2 ansible_host=your-server2-ip


4. Customize the `nginx.yml` playbook as per your requirements. You can modify user credentials, adjust connection settings, etc.

5. Run the playbook with the following command:

ansible-playbook <playbook.yml>


## Feedback

We value your feedback! If you encounter any issues or have suggestions for improvements, feel free to open an issue in this repository.

## Jenkinsfile Explanation

The `Jenkinsfile` in this repository defines the pipeline to automate the Ansible playbook execution in Jenkins. It provides parameters for playbook name and action (Dry-Run or Playbook-deploy). The Jenkins pipeline will clone this repository, execute the Ansible playbook, and provide status updates.

Happy configuring with Ansible! :tada:
