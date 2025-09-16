# Chapter 3 - Cross-Platform Time Sync Management

This chapter introduces **multi-distribution playbook design**.  
The playbook ensures that time synchronization (`chrony/chronyd`) is installed, configured, and running on both **Debian** and **Red Hat** based systems.

## Files

- **ansible.cfg** -> Configures Ansible defaults and output formatting.  
- **inventory** -> Defines host groups (`redhat_family`, `debian_family`) and variables.  
- **playbook.yml** -> Handles cross-platform package installation, service management, and system updates.

## Playbook Details

The playbook performs these tasks:

1. **APT cache update (Debian only)** -> Keeps package index up to date.  
2. **Install chrony** -> Ensures the `chrony` package is present.  
3. **Service management**  
   - Debian: `chrony`  
   - Red Hat: `chronyd`  
   Ensures the service is started and enabled on boot.  
4. **System updates**  
   - Debian: Runs `apt-get update && apt-get -y upgrade` asynchronously.  
   - Red Hat: Runs `yum -y update` asynchronously.  
5. **Debug job IDs** -> Displays background update job IDs for tracking.

## Goal

- Learn to use **conditional tasks** (`when`) for different OS families.  
- Practice **asynchronous execution** with `async` and `poll`.  
- Manage **packages, services, and updates** across heterogeneous environments.  

