# Ansible + AWS Web Hosting (WSL Compatible)

A beginner-friendly project that uses **Ansible** to automate provisioning of an **AWS EC2 instance**, installing **Nginx**, and deploying a sample website.  
Designed for cloud learners and DevOps beginners who want hands-on experience with **Ansible, AWS, and WSL**.

---

## Features

- Provision a Free Tier EC2 instance (t2.micro / t3.micro)  
- Automatically install and start **Nginx**  
- Deploy a sample static website via Ansible templates  
- Configure security groups to allow SSH and HTTP  
- End-to-end automation from local WSL to AWS  

---

## Tech Stack

- **Ansible** (for automation)  
- **AWS EC2** (cloud hosting)  
- **Python 3.x + Boto3** (AWS SDK)  
- **Jinja2 Templates** (for website deployment)  
- **WSL (Ubuntu)** as the development environment  

---

## Project Structure

ansible-aws-webhost/
├── ansible.cfg
├── playbook.yml
├── roles/
│ ├── ec2-provision/
│ │ └── tasks/main.yml
│ ├── nginx-install/
│ │ └── tasks/main.yml
│ └── website-deploy/
│ ├── tasks/main.yml
│ └── templates/index.html.j2


---

## Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/Dharsan111/ansible-aws-webhost.git
cd ansible-aws-webhost

### 2. Create Virtual Environment & Install Dependencies
```bash
python3 -m venv ansible-env
source ansible-env/bin/activate
pip install ansible boto3 botocore amazon.aws

### 3. Configure AWS CLI
```bash
aws configure


(Enter your AWS Access Key, Secret Key, region → e.g., ap-south-1)

### 4. Run the Playbook
```bash
ansible-playbook playbook.yml
