# ansible-role-git [![Build Status](https://travis-ci.org/shengyou/ansible-role-git.svg?branch=master)](https://travis-ci.org/shengyou/ansible-role-git)

=========

安裝 git，可選透過 package management 安裝，或 source code 安裝。

適用於
* CentOS 6
* CentOS 7
* Ubuntu 14.04
* Ubuntu 16.04
* Ubuntu 18.04

Requirements
------------

* ansible >= 2.4
* python >= 2.6

Role Variables
--------------

```
# 如要透過 package management (apt, yum) 安裝，請設為 true
install_from_package_management: (default: false  | false, true)

# 請根據 https://github.com/git/git 釋出的 tag 填寫。
git_version:                     (default: 2.20.0 )
```


Dependencies
------------

none.

Example Playbook
----------------

```
- name: ansible-role-git.yml
  hosts: your_host
  gather_facts: yes
  become: yes

  roles:
    - ansible-role-git
```

License
-------

MIT
