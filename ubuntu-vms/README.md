# vagrant-projects: ubuntu-vms

Vagrantfile that deploys three Ubuntu 18.04 VMs with the same network configuration.

## Create VMs
```vagrant up```

## Login to a VM
```vagrant ssh vagrant@ubuntu-1```

```vagrant ssh vagrant@ubuntu-2```

```vagrant ssh vagrant@ubuntu-3```

# Create a Chef User and Organization

sudo chef-server-ctl user-create USER_NAME FIRST_NAME LAST_NAME EMAIL 'PASSWORD' --filename ~/.chef/USER_NAME.pem
sudo chef-server-ctl user-create vagrant vagrant vagrant cloudtrybe.io@gmail.com 'vagrant' --filename ~/.chef/cloudtrybe.pem

sudo chef-server-ctl user-list

sudo chef-server-ctl org-create ORG_NAME "ORG_FULL_NAME" --association_user USER_NAME --filename ~/.chef/ORG_NAME.pem
sudo chef-server-ctl org-create cloudtrybe "cloudtrybe" --association_user vagrant --filename ~/.chef/cloudtrybe.pem

sudo chef-server-ctl org-list

# Setting Up a Workstation
# Download the latest Chef Workstation:
wget  https://packages.chef.io/files/stable/chef-workstation/0.2.43/ubuntu/18.04/chef-workstation_0.2.43-1_amd64.deb

sudo dpkg -i chef-workstation_*.deb
chef generate repo chef-repo

127.0.0.1 localhost
192.168.33.101 example.com
192.168.33.102 workstation
192.168.33.103 
192.168.33.104
