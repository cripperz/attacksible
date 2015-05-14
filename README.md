Attacksible
===========

Ansible provisioned security platform.

Tested on:
* Fedora 19,20,21
* CentOS 7 (however a bunch of tools will be missing)
* Debian of various releases

Near future improvements:
* Install of the software from the git repos pulled in

Install
-----

    sudo yum install ansible || sudo apt-get install ansible

or

    git clone --recursive https://github.com/ansible/ansible.git
    source ansible/hacking/env-setup

Usage
-----

Tools will be located in /opt/attacksible, or otherwise installed globally as system packages

### For the full desktop install
    ansible-playbook play.yml -i attacksible --connection=local -K

### Headless
    ansible-playbook play.yml -i attacksible --skip-tags 'gui' --connection=local -K

### Untested software
Software we're yet to confirm as stable in the system has been tagged with 'untested'.  
These can be excluded by issuing `--skip-tags 'untested'`

    ansible-playbook play.yml -i attacksible --skip-tags 'untested' --connection=local -K

