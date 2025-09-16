# Chapter 4 - Web Server Automation with NGINX

This chapter focuses on **installing and configuring a web server** in a cross-platform environment.  
The playbook ensures that **NGINX** is properly installed and running while disabling any conflicting Apache services.

## Files

- **ansible.cfg** -> Sets defaults and YAML-style output for better readability.  
- **inventory** -> Defines Red Hat and Debian host groups, relying on `~/.ssh/config` for connection details.  
- **playbook.yml** -> Automates web server setup with NGINX across different OS families.

## Playbook Details

1. **Update apt cache (Debian only)** -> Ensures package lists are fresh.  
2. **Collect service facts** -> Gathers running services for later checks.  
3. **Stop and disable Apache/httpd if present**  
   - Debian: stops `apache2`  
   - Red Hat: stops `httpd`  
4. **Install NGINX** -> Installs the NGINX package on all hosts.  
5. **Start and enable NGINX** -> Ensures NGINX is running and enabled at boot.

## Goal

- Learn to **replace one service with another** using Ansible.  
- Practice **service detection** with `service_facts`.  
- Standardize **web server automation** across multiple Linux distributions.  

