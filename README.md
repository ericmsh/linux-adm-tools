
# linux-adm-tools

Linux Servers Administration Tools

# add-disk-space.yml

This playbook will add disk space to the root logical volume part of vg01.   
It will also resize the / file system.  
Note: The value of /dev/sda and vg01 are hardcoded in the playbook. Edit when required.

## Step1: Increase the Disk Size of the Virtual Machine

Increase the disk space of the main OS disk using the Proxmox or VMware console.

## Step2: Run the playbook
```
ansible-playbook -i inventory add-disk-space.yml
```


