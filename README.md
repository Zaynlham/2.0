# 🚀 Ansible AWS Website Deployment

## 📖 Project Overview

This project automates the deployment of a static HTML website to an AWS EC2 Ubuntu instance using **Ansible**.

Instead of manually connecting to the server and configuring it, the entire deployment is performed using a single Ansible playbook.

---

## 🎯 Objectives

* Learn Infrastructure as Code (IaC)
* Automate server configuration using Ansible
* Deploy a website to AWS EC2
* Practice SSH authentication using key pairs
* Learn Git and GitHub project management
* Understand idempotent automation

---

## 🛠 Technologies Used

* Ansible
* AWS EC2
* Ubuntu Server
* Nginx
* SSH
* Git
* GitHub
* Linux

---

## 📂 Project Structure

```text
ansible-aws-deploy/
├── deploy.yml
├── inventory.example
├── index.html
├── README.md
└── .gitignore
```

---

## ⚙️ What the Playbook Does

The playbook performs the following tasks:

1. Connects to the EC2 instance using SSH.
2. Updates the Ubuntu package cache.
3. Installs Nginx (if not already installed).
4. Ensures the Nginx service is running and enabled at boot.
5. Copies the website (`index.html`) from the Ansible controller to the EC2 instance.
6. Sets the correct ownership and permissions on the deployed file.

---

## 🚀 Deployment

Clone the repository.

Create your own inventory file from the example:

```bash
cp inventory.example inventory
```

Edit the inventory file with:

* Your EC2 Public IP
* Your SSH private key path

Run the playbook:

```bash
ansible-playbook -i inventory deploy.yml
```

After deployment, open your browser and visit:

```text
http://YOUR_EC2_PUBLIC_IP
```

---

## 🔐 Security

The following files are intentionally excluded from Git:

* `inventory`
* `*.pem`
* `*.retry`

This prevents sensitive information such as server details and private SSH keys from being published.

---

## 📚 Concepts Learned

* Infrastructure as Code (IaC)
* Configuration Management
* Ansible Inventory
* Ansible Playbooks
* SSH Authentication
* AWS EC2
* Nginx Deployment
* Linux Services
* Git Version Control
* GitHub Repository Management
* Idempotent Automation

---

## 👨‍💻 About This Project

This project was built as part of my DevOps learning journey.

I designed, configured, debugged, and deployed the project myself while studying DevOps concepts and best practices. Every component of the project was understood, tested, and reviewed as part of the learning process rather than simply copied and executed.

---

## 📄 License

This project is intended for educational and portfolio purposes.

