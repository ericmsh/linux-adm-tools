# linux-adm-tools
Linux Servers Administration Tools
# add-disk-space.yml
This playbook will add disk space to the root logical volume part of vg01.
It will also resize the / file system.

Step1: Increase the Disk Size of the Virtual Machine
Step2: Run the playbook
```
ansible-playbook -i inventory add-disk-space.yml
```


