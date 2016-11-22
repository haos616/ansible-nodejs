Ansible role nodejs
===================

# Install nodejs v 0.12
```
---
- hosts: all
  become_user: root
  become: yes
  gather_facts: yes
  tags: ['setup']
  roles:
    - { role: nodejs, task: setup }
```

# Install nodejs v4
```
---
- hosts: all
  become_user: root
  become: yes
  gather_facts: yes
  tags: ['setup']
  roles:
    - { role: nodejs, task: setup, nodejs_repo: "node_4.x" }
```
or add in group_vars/all
```
nodejs_repo: "node_4.x"
```

# Install nodejs v6
```
---
- hosts: all
  become_user: root
  become: yes
  gather_facts: yes
  tags: ['setup']
  roles:
    - { role: nodejs, task: setup, nodejs_repo: "node_6.x" }
```
or add in group_vars/all
```
nodejs_repo: "node_6.x"
```

# Install bower
add in group_vars/all
```
bower: true
```

# Install gulp
add in group_vars/all
```
gulp: true
```
