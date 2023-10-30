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
- name: Configure Web Servers
  hosts: web_servers
  tasks:
    - name: Ensure Apache is installed
      package:
        name: apache2
        state: present

    - name: Start Apache Service
      service:
        name: apache2
        state: started
		
- name: Configure Database Servers
  hosts: db_servers
  tasks:
    - name: Ensure MySQL is installed
      package:
        name: mysql-server
        state: present

    - name: Start MySQL Service
      service:
        name: mysql
        state: started
````
