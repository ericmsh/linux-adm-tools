
# linux-adm-tools

Linux Servers Administration Tools

# add-disk-space.yml

This playbook will add disk space to the root logical volume part of vg01.   
It will also resize the / file system.  
Note: The value of /dev/sda and vg01 are hardcoded in the playbook. Edit when required.

## Step1: Increase the Disk Size of the Virtual Machine

Check the disk size on the server:  
```
fdisk -l /dev/sda
```

Increase the disk space of the main OS disk using the Proxmox or VMware console.  
Check the disk size to make sure additional space has been added:  
```
fdisk -l /dev/sda
```

## Step2: Clone repo

On the server itself, as root user, clone the repo:  
```
git clone https://github.com/ericmsh/linux-adm-tools.git
cd linux-adm-tools
```

## Step3: Run the playbook
```
ansible-playbook -i inventory add-disk-space.yml
```

