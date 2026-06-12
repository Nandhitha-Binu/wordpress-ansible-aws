# WordPress Deployment Automation using Ansible on AWS

## Project Overview

This project automates the deployment of a WordPress website on an AWS EC2 instance using Ansible. The deployment includes Nginx, PHP, MariaDB, phpMyAdmin, SFTP access, and SSL encryption using Let's Encrypt certificates.

The objective of this project is to demonstrate Infrastructure Automation, Configuration Management, and Web Application Deployment using Ansible role-based architecture.

---

## Technologies Used

* AWS EC2 (Amazon Linux 2023)
* Ansible
* Nginx
* PHP-FPM
* MariaDB
* WordPress
* phpMyAdmin
* SFTP
* DuckDNS
* Let's Encrypt SSL
* Git & GitHub

---

## Project Structure

```text
wordpress-ansible/
├── inventories/
├── roles/
│   ├── common/
│   ├── nginx/
│   ├── php/
│   ├── mariadb/
│   ├── wordpress/
│   ├── phpmyadmin/
│   ├── sftp_user/
│   └── ssl/
└── site.yml
```

---

## Ansible Roles

### Common

* System updates
* Basic package installation

### Nginx

* Web server installation
* Virtual host configuration
* WordPress site configuration

### PHP

* PHP and PHP-FPM installation
* Required PHP extensions

### MariaDB

* Database server installation
* WordPress database creation
* Database user creation

### WordPress

* WordPress download and configuration
* wp-config.php deployment

### phpMyAdmin

* phpMyAdmin installation and deployment

### SFTP User

* User and group creation
* Website directory ownership configuration

### SSL

* SSL configuration support

---

## Deployment

Run the complete deployment using:

```bash
ansible-playbook -i inventories/hosts site.yml
```

---

## Domain Configuration

DuckDNS domain used:

```text
mywordpressblog.duckdns.org
```

---

## SSL Configuration

SSL certificates were generated using Certbot and Let's Encrypt.

```bash
sudo systemctl stop nginx
sudo certbot certonly --standalone -d mywordpressblog.duckdns.org -v
sudo systemctl start nginx
```

---

## Website URLs

WordPress:

```text
https://mywordpressblog.duckdns.org
```

phpMyAdmin:

```text
https://mywordpressblog.duckdns.org/phpmyadmin
```

---

## Screenshots

Add screenshots of:

1. AWS EC2 Instance
2. Ansible Playbook Execution
3. WordPress Homepage
4. WordPress Admin Dashboard
5. phpMyAdmin Dashboard
6. SSL Certificate Verification

---

## Learning Outcomes

* Infrastructure automation using Ansible
* Web server deployment on AWS
* Database provisioning and management
* Domain and DNS configuration
* SSL certificate management
* Linux user and permission management

---

## Author

Nandhitha Binu

