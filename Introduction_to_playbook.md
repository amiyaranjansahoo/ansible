#### What is playbook
```sh
A playbook is a single YAML file containing a set of plays
Play defines a set of tasks to be executed on one or more remote hosts.
The task is a single action to be performed on a host or group of hosts
Playbooks are written in YAML format and provide a way to organize and execute complex automation tasks.
Some examples of a task are 
	executing a command
        copy a file
	Run a script
	Installing a package on the host 
	performing a shutdown or a restart operation etc etc
````

#### Example of playbok
```sh
---
- name: First Play - Manage Web Servers
  hosts: webservers
  become: yes
  tasks:
    - name: Install Apache web server
      yum:
        name: httpd
        state: present

    - name: Start Apache web server
      service:
        name: httpd
        state: started
        enabled: yes

- name: Second Play - Manage Database Servers
  hosts: dbservers
  become: yes
  tasks:
    - name: Install MySQL server
      yum:
        name: mysql-server
        state: present

    - name: Start MySQL service
      service:
        name: mysqld
        state: started
        enabled: yes
````
