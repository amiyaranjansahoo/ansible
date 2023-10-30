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
