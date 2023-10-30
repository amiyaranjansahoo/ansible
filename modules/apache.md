```sh
- hosts: apache
  become: True
  tasks:
    - name: Install Apache
      yum:
        name: httpd
        state: present
````

```sh
- hosts: apache
  become: True
  tasks:
    - name: Install Apache
      yum:
        name: httpd
        state: present
    - name: Start and Enable Apache
      service:
        name: httpd
        state: started
        enabled: True
````

```sh
- hosts: apache
  become: True
  tasks:
    - name: Install Apache
      yum:
        name: httpd
        state: present
    - name: Copy index file on to Apache server
      copy:
        src: index.html
        dest: /var/www/html/
    - name: Start and Enable Apache server
      service:
        name: httpd
        state: started
        enabled: True
````
