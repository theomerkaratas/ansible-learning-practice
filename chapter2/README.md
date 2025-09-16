# Chapter 2 - First Playbook: Chrony Setup

This chapter introduces the **first Ansible playbook**.  
It demonstrates how to install and manage a time synchronization service (`chronyd`) on an Amazon Linux host.

## Files

- **ansible.cfg** -> Basic Ansible configuration, points to the local inventory.  
- **inventory** -> Defines the managed host with connection variables (user, private key, Python interpreter).  
- **playbook.yml** -> Installs and configures the `chronyd` service.

## Playbook Details

The playbook performs the following tasks:
1. **Install chrony** -> Ensures the `chrony` package is present on the server.  
2. **Enable & Start chronyd** -> Makes sure the `chronyd` service is running and enabled at boot.  

## Goal

- Learn how to write a **basic playbook** with tasks.  
- Practice **package management** and **service control** using Ansible.  

