```sh
- hosts: apache
  become: True
  tasks:
    - name: install apache
      yum:
        name: httpd
        state: present
````

```sh
- hosts: apache
  become: True
  tasks:
    - name: install apache
      yum:
        name: httpd
        state: present
    - name: start and enable apache server
      service:
        name: httpd
        state: started
        enabled: True
````

```sh
- hosts: apache
  become: True
  tasks:
    - name: install apache
      yum:
        name: httpd
        state: present
    - name: copy index file on to apceh server
      copy:
        src: index.html
        dest: /var/www/html/
    - name: start and enable apache server
      service:
        name: httpd
        state: started
        enabled: True
````
