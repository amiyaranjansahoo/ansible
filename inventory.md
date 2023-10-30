#### Inventory file format for password based login
```sh
server1 ansible_host=<private ip> ansible_user=user1 \
ansible_password=user1
````

#### Inventory file format for aws cloud
```sh
server1 ansible_host=<private ip> ansible_user=ec2-user \
ansible_private_key_file=/home/ec2-user/ws/key.pem
````

#### Inventory file format for multiple targets
```sh
# Web Servers
server1 ansible_host=172.31.32.15 ansible_user=ec2-user ansible_private_key_file=/home/ec2-user/ws/key.pem
server2 ansible_host=172.31.12.140 ansible_user=ec2-user ansible_private_key_file=/home/ec2-user/ws/key.pem
server3 ansible_host=172.31.32.17 ansible_user=ec2-user ansible_private_key_file=/home/ec2-user/ws/key.pem


[web_servers]
server1
server2
````
