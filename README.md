OpenBSD vmm with veb(4)
=======================

Setup OpenBSD with veb(4) and vport(4)

Requirements
------------

OpenBSD >=7.0 and a processor with flags: SLAT for AMD or EPT for Intel.

Example hosts & Playbook
------------------------

hosts:
[current:vars]
ansible_python_interpreter=/usr/local/bin/python3

[current]
100.65.0.100

playbook:

- hosts: current
  remote_user: gonzalo
  become: yes
  become_method: doas
  roles:
    - vmm_setup_veb

License
-------

BSD

Author Information
------------------

Gonzalo L. R. <gonzalo@x61.sh>
