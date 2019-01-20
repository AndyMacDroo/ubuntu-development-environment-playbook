# Development Environment Setup #

Use ansible playbooks to provision an Ubuntu machine with what is required to get started with a basic development environment.

## Clone Repo ##

Clone the repository:

```
git clone --recursive <GIT_URI>
```

## Install Ansible ##

Run the following commands:

```
#!/usr/bin/env bash
sudo apt-get install software-properties-common
sudo apt-add-repository ppa:ansible/ansible
sudo apt-get update
sudo apt-get install ansible
```

## Running the Playbooks ##

* In the directory of the project run:

```
ansible-playbook -i "localhost," -c local configure.yml
```

## Vagrant Test Box (for testing playbooks) ##

* The ansible playbook comes with a `Vagrantfile` which allows you to test the result of the build of the environment. 

### Running Box ###

In the directory of the project run the following to get a base box:

```
vagrant up dev
```

### Provision Existing Box ###

In the directory of the project run the following to provision a base box:

```
vagrant provision dev
```


### Remove Existing Box ###

In the directory of the project run the following to remove a base box:

```
vagrant destroy dev
```

