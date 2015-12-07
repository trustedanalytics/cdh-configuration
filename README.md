cdh-configuration
=========

Prepare a Host machines for a Hadoop/CDH installation.

Performs the following
- turns off huge pages
- turns off iptables
- increases [file and process limits](vars/limits.yml) for hadoop, spark, hdfs, and hbase
- mount all unformated disks
- update network configuration in [sysctl](vars/network.yml)
- turn off selinux
- set vm swappiness to [10](vars/RedHat.yml)

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
