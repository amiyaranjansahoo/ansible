It defines a set of tasks to be executed on one or more remote hosts. 
Playbooks are written in YAML format and provide a way to organize and execute complex automation tasks.

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
