# 🛠️ CI/CD Web Server Deployment with Ansible & Azure

This project demonstrates how to automatically provision and deploy a web server (Nginx) on an Azure Virtual Machine using Ansible and GitHub Actions.

## 📦 Stack

- **Infrastructure**: Azure VM (Ubuntu)
- **Automation Tool**: Ansible
- **CI/CD Pipeline**: GitHub Actions
- **Web Server**: Nginx
- **Languages**: Bash, YAML

## 🚀 Features

- SSH key-based deployment automation
- Ansible playbook to install and configure Nginx
- Deployment of a custom `index.html`
- Fully automated from `git push` → live update

## 📁 Project Structure
├── .github/
│   └── workflows/
│       └── deploy.yml          # CI/CD pipeline
│
├── ansible/
│   ├── inventory.ini           # Remote VM target definition
│   └── playbook.yml            # Web server provisioning script
│
└── index.html                  # Custom web page deployed to Nginx


## 🧪 How It Works

1. **Push to `main`** triggers the pipeline.
2. GitHub Actions installs Ansible.
3. Private SSH key is used to connect to the Azure VM.
4. Ansible playbook provisions Nginx and uploads `index.html`.

## ✅ Sample Output

![CI/CD Successful](screenshots/github-actions-success.png)
![Deployed Site](screenshots/deployed-site.png)

## 🛡️ Security

- SSH keys are stored in GitHub Secrets
- Access is limited to a specific VM IP

## 🔗 Live Demo

Try accessing: [http://<your-VM-IP>](http://<your-VM-IP>)


