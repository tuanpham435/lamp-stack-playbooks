# Ansible LAMP Stack Deployment

This project uses Ansible to automate the deployment of a LAMP (Linux, Apache, MySQL, PHP) stack on Red Hat Enterprise Linux 9.

## Project Structure

```
.
├── README.md
├── ansible.cfg
├── deploy-lamp-stack.yml
├── group_vars/
├── host_vars/
├── inventory
├── roles/
│   ├── common/
│   ├── httpd-php/
│   └── mysql/
└── templates/
```

## Prerequisites

- Ansible installed on the control node
- Target EC2 instances:
  - AMI: ami-0583d8c7a9c35822c (64-bit x86) or ami-07472131ec292b5da (64-bit Arm)
  - OS: Red Hat Enterprise Linux 9 (HVM), EBS General Purpose (SSD)

## Roles

1. `common`: Basic system configuration
2. `httpd-php`: Apache web server and PHP installation and configuration
3. `mysql`: MySQL database installation and configuration

## Usage

Run the playbook:

   ```
   ansible-playbook deploy-lamp-stack.yml
   ```