#Trellis Overview

## Versions 

```
composer --version
Composer version 1.8.5 2019-04-09 17:46:47
```

```
ansible --version
ansible 2.7.0
  config file = None
  configured module search path = ['/home/pilou/.ansible/plugins/modules', '/usr/share/ansible/plugins/modules']
  ansible python module location = /home/pilou/miniconda3/lib/python3.6/site-packages/ansible
  executable location = /home/pilou/miniconda3/bin/ansible
  python version = 3.6.8 |Anaconda, Inc.| (default, Dec 30 2018, 01:22:34) [GCC 7.3.0]
```

```
VirtualBox GUI

vboxmanage --version
6.0.8r130520
```

```
vagrant -v
Vagrant 2.2.4
```

```
python -V
Python 3.6.8 :: Anaconda, Inc.
```

## Trellis Installation

- **Install php**

```
sudo apt-get update
sudo apt-get upgrade
sudo apt install php7.2-cli -y
```
  
- **[Install composer](https://getcomposer.org/download/)**  

`mv composer.phar /usr/local/bin/composer`

- **[Install VirtualBox](https://www.virtualbox.org/wiki/Linux_Downloads)**

- **Install Vagrant**

```
wget https://releases.hashicorp.com/vagrant/2.2.4/vagrant_2.2.4_x86_64.deb  
dpkg -i vagrant_2.2.4_x86_64.deb
```

- **Install php-xml**

`sudo apt-get install php-xml`

- **[Install vagrant-hostmanager](https://github.com/devopsgroup-io/vagrant-hostmanager#installation)**



- **Follow [README](https://github.com/roots/trellis)**

## Problems ?

Versions of Annsible, php, composer etc... -> add a very detailled requirements.txt ?   
_If Ansible >= 2.8 problem..._


/!\ NFS

/!\ Very well design your wordpress_sites.yml (www.example.com)

## Environnement de travail


## Tuto how to

- Comment mettre en place env de dev
- Conf du server distant
- Pousser le site en prod
- mettre en prod un changement
- tuto avec [loom](https://www.loom.com/)


## Tuto

### Requirements

- A Domain assigned with a IP
- Access to the machine with ssh (root)
- Github account

### Commands

1. start with a fresh thing

Need to have sudo access

```
apt-get update
apt-get upgrade -y
apt-get install git -y
apt-get install wget -y
apt-get install curl -y
apt-get install nano -y

git clone git@github.com:Plrerolle/pltrelliscool.tk.git
cd pltrelliscool.tk

apt install php7.2-cli -y
apt-get install php-xml -y
php --version

php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('sha384', 'composer-setup.php') === '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
mv composer.phar /usr/local/bin/composer

cd ..
apt-get install gnupg -y
wget -q https://www.virtualbox.org/download/oracle_vbox_2016.asc -O- | apt-key add -
wget -q https://www.virtualbox.org/download/oracle_vbox.asc -O- | apt-key add -
echo "deb [arch=amd64] http://download.virtualbox.org/virtualbox/debian bionic contrib"
apt-get update
apt-get install virtualbox-6.0 -y

wget https://releases.hashicorp.com/vagrant/2.2.4/vagrant_2.2.4_x86_64.deb  
dpkg -i vagrant_2.2.4_x86_64.deb

vagrant plugin install vagrant-hostmanager
vagrant hostmanager

apt-get install python -v
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
python get-pip.py
pip install ansible

```

**Checks**

```
composer --version
vboxmanage --version
vagrant -v
```