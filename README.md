# Infrastructure Automation using Ansible, Jenkins & GitHub

## Project Overview

This repository demonstrates an Infrastructure Automation pipeline using **Ansible**, **Jenkins**, and **GitHub** following enterprise DevOps practices.

The objective of this project is to automate software installation and configuration on Linux servers while maintaining Infrastructure as Code (IaC), Git version control, and CI/CD workflows.

---

## Architecture

```
GitHub Repository
        │
        ▼
Jenkins Pipeline
        │
        ▼
Ansible Control Node
        │
        ▼
Target Linux Servers
```

---

## Technologies Used

- Ansible
- Jenkins
- Git
- GitHub
- Ubuntu Linux
- Docker
- Apache HTTP Server
- Nginx
- Apache Tomcat
- OpenSSH

---

## Repository Structure

```
ansible/
│
├── inventories/
│   ├── dev/
│   ├── uat/
│   └── prod/
│
├── playbooks/
│   ├── apache.yml
│   ├── docker.yml
│   ├── nginx.yml
│   └── tomcat.yml
│
├── roles/
│   ├── apache/
│   ├── docker/
│   ├── nginx/
│   └── tomcat/
│
└── ansible.cfg
```

---

## Features

- Infrastructure as Code (IaC)
- Modular Ansible Roles
- Environment-specific inventories
- Jenkins Integration
- Private GitHub Repository Integration
- Parameterized Jenkins Jobs
- Git Feature Branch Workflow
- Automated Infrastructure Deployment
- Idempotent Ansible Playbooks
- Passwordless SSH Authentication
- Sudo Privilege Automation

---

## Current Roles

| Role | Status |
|------|--------|
| Apache | ✅ |
| Nginx | ✅ |
| Docker | ✅ |
| Tomcat | ✅ |

---

## Workflow

1. New infrastructure request is received.
2. Create a feature branch.
3. Develop or modify the required Ansible role.
4. Test locally.
5. Commit changes.
6. Push feature branch.
7. Raise Pull Request.
8. Review and Merge.
9. Jenkins executes approved playbooks.
10. Ansible deploys changes to target servers.

---

## Jenkins Deployment

Jenkins executes Ansible playbooks using parameterized builds.

Parameters include:

- Environment
    - DEV
    - UAT
    - PROD

- Playbook
    - Apache
    - Nginx
    - Docker
    - Tomcat

Deployment command:

```bash
ansible-playbook \
-i inventories/<environment>/hosts.ini \
playbooks/<playbook>.yml \
--limit <target>
```

---

## Branching Strategy

```
master
│
├── feature/apache-role
├── feature/nginx-role
├── feature/docker-role
└── feature/tomcat-role
```

- Feature development is performed in dedicated branches.
- Changes are merged to `master` after testing and review.

---

## Project Highlights

- Automated software installation
- Modular role-based Ansible architecture
- Environment segregation (DEV/UAT/PROD)
- GitHub Version Control
- Jenkins Continuous Deployment
- Enterprise-inspired Infrastructure Automation workflow

---

## Future Enhancements

- Jenkins Declarative Pipeline
- ServiceNow Change Request Simulation
- Dynamic Inventory
- Ansible Vault
- AWX / Ansible Automation Platform
- Terraform Integration
- Kubernetes Deployment
- Docker Compose Automation
- Application Deployment Automation
- Monitoring Integration (Prometheus & Grafana)

---

## Author

Ahmed Shaikh

DevOps | Cloud | Infrastructure Automation

GitHub: https://github.com/Ahmedshaikh1899
