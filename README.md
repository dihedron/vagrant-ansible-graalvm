# A Vagrant + Ansible recipe to setup a VM running Oracle GraalVM

This repository contains:

1. a `Vagrantfile` that sets up a virtual machine ready to run Oracle GraalVM
2. an 'Ansible' playbook that performs all the actions needed to install and configure the said Oracle GraalVM.

## How to run

To start the virtual machine, make sure you have `vagrant` installed on your machine, than change into the `vagrant/` directory and run

```bash
$> vagrant up
```

Once the virtual machine is up and running, make sure the guest's SSH port is mapped to port 2222 on the host. If not, take a not about the mapped port.

Then change into the `ansible/` directory, if the guest's SSH port is not mapped to 2222 adjust the `ansible/inventory` file accordingly. Then run the following:

```bash
$> ANSIBLE_NOCOWS=1 ansible-playbook playbook.yml
```
  
