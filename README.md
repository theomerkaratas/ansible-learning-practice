# ansible-learning-practice
Step-by-step practice repository for learning Ansible with real server automation examples.
=======
# Ansible Learning Repository

This repository documents my journey of **learning Ansible** step by step.  
Each `chapterX/` directory contains a different scenario that demonstrates key Ansible concepts, from basic configuration to more advanced automation.

## Structure

- **chapter1** -> Basic Ansible configuration and ad-hoc command usage (no playbooks yet).  
- **chapter2** -> First playbook: installing and managing the `chronyd` service.  
- **chapter3** -> Cross-platform package & service management with conditionals (`when`) and asynchronous tasks.  
- **chapter4** -> Web server automation: install NGINX, disable Apache/httpd if present.  
- **chapter5** -> Advanced playbooks: variables, file downloads, unarchiving, and systemd service management.  

## Goals

- Learn Ansible fundamentals in a **progressive, scenario-based approach**.  
- Demonstrate practical skills in:  
  - Writing and running playbooks  
  - Managing packages and services across Linux distributions  
  - Using variables and conditionals  
  - Automating real-world server setups (time sync, web servers, etc.)  

## How to Run

To run a playbook from any chapter:

```bash
cd chapterX
ansible-playbook playbook.yml

>>>>>>> 06fc463 (Initial commit: Ansible learning practice)
