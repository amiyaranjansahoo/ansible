# Ansible Installation
## For AMI: Amazon Linux 2
amazon-linux-extras install ansible2 -y
## For AMI: Amazon Linux 2 (Alternative)
```sh
sudo amazon-linux-extras install epel -y
sudo amazon-linux-extras disable ansible2
sudo yum --enablerepo epel install ansible -y
ansible --version
cd /etc;chmod -R 777 ansible/
````
## For AMI: Amazon Linux 2023
### system update
```sh
sudo dnf update
```
### Check If pip is installed
```sh
pip --version
pip3 --version
```

### Check If Python is Available, if not install python
```sh
python3 --version
sudo dnf install python3.11
```
### Install pip3
```sh
sudo dnf install python3-pip
pip --version
```

### Install Ansible using pip
```sh
pip install ansible
ansible --version
```

### Install sshpass, whereever required
```sh
 wget http://sourceforge.net/projects/sshpass/files/latest/download -O sshpass.tar.gz
 tar -xvf sshpass.tar.gz
 cd sshpass-1.06
 ./configure
sudo make install
````
