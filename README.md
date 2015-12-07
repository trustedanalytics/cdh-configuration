cdh-configuration
=========

Prepare a Host machines for a Hadoop/CDH installation. Perform a variety of
configurations like turning off iptables, updating file and process limits, ....

Requirements
------------
Redhat/CentOS 6
ansible 2.0
sudo access 

Role Variables
--------------

none

Dependencies
------------
libselinux-python - installed through yum automatically

Example Playbook
----------------

You can see the sample playbook in the [test directory](test)
---
- hosts: CDH
  become: yes
  become_user: root
  roles:
  - { role: ansible-cdh-opti }

License
-------

Apache 2.0

Author Information
------------------

trustedanalytics.github.io
