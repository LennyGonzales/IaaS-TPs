# Atelier 01

## Challenge 01

```bash
vagrant up ubuntu
vagrant ssh ubuntu
```

In the vm :
```bash
sudo apt update
apt-cache search --names-only ansible
sudo apt install -y ansible
ansible --version
exit
```

```bash
vagrant destroy -f ubuntu
```

Result :
```bash
vagrant@ubuntu:~$ ansible --version
ansible 2.10.8
  config file = None
  configured module search path = ['/home/vagrant/.ansible/plugins/modules', '/usr/share/ansible/plugins/modules']
  ansible python module location = /usr/lib/python3/dist-packages/ansible
  executable location = /usr/bin/ansible
  python version = 3.10.12 (main, Aug 15 2025, 14:32:43) [GCC 11.4.0]
```
![challenge 01](challenge_01.png)

## Challenge 02

```bash
vagrant up ubuntu
vagrant ssh ubuntu
```

In the vm :
```bash
sudo apt update
sudo apt-add-repository ppa:ansible/ansible
apt-cache search --names-only ansible
sudo apt install -y ansible
ansible --version
exit
```

```bash
vagrant destroy -f ubuntu
```

Result :
```bash
vagrant@ubuntu:~$ ansible --version
ansible [core 2.17.14]
  config file = /etc/ansible/ansible.cfg
  configured module search path = ['/home/vagrant/.ansible/plugins/modules', '/usr/share/ansible/plugins/modules']
  ansible python module location = /usr/lib/python3/dist-packages/ansible
  ansible collection location = /home/vagrant/.ansible/collections:/usr/share/ansible/collections
  executable location = /usr/bin/ansible
  python version = 3.10.12 (main, Aug 15 2025, 14:32:43) [GCC 11.4.0] (/usr/bin/python3)
  jinja version = 3.0.3
  libyaml = True
```
![challenge 02](challenge_02.png)

## Challenge 03

```bash
vagrant up rocky
vagrant ssh rocky
```

In the vm :
```bash
sudo dnf install python3-pip
python3 -m venv ~/.venv/ansible
source ~/.venv/ansible/bin/activate
pip install --upgrade pip
pip install ansible
ansible --version
exit
```

```bash
vagrant destroy -f rocky
```

Result :
```bash
(ansible) [vagrant@rocky ~]$ ansible --version
ansible [core 2.15.13]
  config file = None
  configured module search path = ['/home/vagrant/.ansible/plugins/modules', '/usr/share/ansible/plugins/modules']
  ansible python module location = /home/vagrant/.venv/ansible/lib64/python3.9/site-packages/ansible
  ansible collection location = /home/vagrant/.ansible/collections:/usr/share/ansible/collections
  executable location = /home/vagrant/.venv/ansible/bin/ansible
  python version = 3.9.21 (main, Aug 19 2025, 00:00:00) [GCC 11.5.0 20240719 (Red Hat 11.5.0-5)] (/home/vagrant/.venv/ansible/bin/python3)
  jinja version = 3.1.6
  libyaml = True
```
![challenge 03](challenge_03.png)
