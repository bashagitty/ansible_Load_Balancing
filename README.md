

# NGINX Load Balancer Setup with Ansible

This guide provides instructions on how to use Ansible to set up an NGINX load balancer for a web application that serves cricket strategies. The setup includes configuring NGINX to balance traffic across multiple backend web servers hosting the application.

## Directory Structure

The project directory should have the following structure:

```
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
```

### Description of Files and Directories:

- **`inventory.txt`**: Inventory file containing IP addresses or hostnames of servers (`webserver12` and `loadbalancer` groups).
  
- **`playbook.yml`**: Ansible playbook file defining tasks for setting up web servers (`webservers` role) and load balancer (`loadbalancer` role).

- **`roles/`**:
  - **`webservers/`**:
    - **`tasks/main.yml`**: Tasks file for installing NGINX and deploying the static website (`index.html`).
    - **`files/index.html`**: HTML file containing cricket strategies content.
  
  - **`loadbalancer/`**:
    - **`tasks/main.yml`**: Tasks file for installing NGINX, configuring load balancing, and restarting NGINX service.
    - **`templates/load_balancer.conf.j2`**: Jinja2 template for NGINX load balancer configuration.





