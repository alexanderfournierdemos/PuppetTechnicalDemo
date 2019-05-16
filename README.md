
# PuppetTechnicalProject


## Requirements

*  The solution must run on a clean installation of the chosen operating system without errors.
* Jenkins and its prerequisites must be installed without manual intervention.
* Jenkins must be configured to serve requests over port 8000.
NOTE: It is not sufficient to forward port 8000 on either the host or the guest OS to the default Jenkins port. Jenkins itself must be configured to listen on port 8000.
* Subsequent applications of the solution should not cause failures or repeat redundant configuration tasks


## Project Overview 

The solution provided Uses Ansible to deploy Jenkins on Vagrant. You must first install ansible and configure your development environment to run this project. You can do so using the "Getting Started" section below. The project links to a custom ansible role repository that makes configuration of future deployments version controlled and highly customizable. 



## Q & A 
https://docs.google.com/document/d/17lKg2-c4-K6GH8U8nZc2ffhDyuB8IyOBOUvIPY5laL8/edit?usp=sharing



## Getting Started

To use the vagrant file, you will need to have done the following:

  1. Download and Install [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
  2. Download and Install [Vagrant](https://www.vagrantup.com/downloads.html)
  3. Install [Ansible](http://docs.ansible.com/ansible/latest/intro_installation.html)
  4. Open a shell prompt (Terminal app on a Mac) and cd into the folder containing the `Vagrantfile`
  5. Run the following command to install the necessary Ansible roles for this profile: `$ ansible-galaxy install -r requirements.yml`

Once all of that is done, you can simply type in `vagrant up`, and Vagrant will create a new VM, install the base box, and configure it.

Once the new VM is up and running (after `vagrant up` is complete and you're back at the command prompt), you can log into it via SSH if you'd like by typing in `vagrant ssh`. Otherwise, the next steps are below.

### Setting up your hosts file

You need to modify your host machine's hosts file (Mac/Linux: `/etc/hosts`; Windows: `%systemroot%\system32\drivers\etc\hosts`), adding the line below:

    192.168.33.55  jenkins



## Dependent Ansible Role Repository 

* https://github.com/alexanderfournierdemos/ansible-role-jenkins.git
 
 
## Documentation:

* https://docs.ansible.com : Ansible 



## To Do/ Improvements

* Obviously less than ideal having to do manual setup of dev machine/ansible master. Probably could have figured out a way to tie vagrant together similar to a docker-compose. 
