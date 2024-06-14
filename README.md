NGINX Load Balancer Setup with Ansible

This guide provides instructions on using Ansible to set up an NGINX load balancer for a web application that serves cricket strategies. The setup includes configuring NGINX to balance traffic across multiple backend web servers hosting the application
Directory Structure

.

├── inventory.txt

├── playbook.yml

└── roles

    ├── webservers
    │   ├── tasks
    │   │   └── main.yml
    │   └── files
    │       └── index.html
    └── loadbalancer
        ├── tasks
        │   └── main.yml
        └── templates
            └── load_balancer.conf.j2
