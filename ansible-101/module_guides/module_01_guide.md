:Author:    Lindis Webb and Jason Smith
:Email:     lindis@solinea.com, jason@solinea.com
:Date:      Feb 2016
:Revision:  0.1a
:Module:    Module 01 Ansible 101

# Module 01: Ansible 101

## Syntax and usage section

Command that is run by a user or instructor looks like this:

 $ sudo apt-get upgrade

<<<

## Module 01: Introduction to Ansible and Configuration Management +

Scope: The scope for this document is to help drive the narrative for the in
lecture demos that are performed by the instructor. +

Audience: The audience for this doc is the instructor and the course content
creator. +

--
Module Narrative:
--
[source]
--
"You work at ACME are  tasked with deploying a new WordPress application
and conduct a pilot on how Ansible can be used for configuration management."
--

Environment: +
1 x Management Server +
1 x dev01 Dev Server +


*Objectives of this module:* +

* Explain what Configuration Management is
* Summarize the Architecture of Ansiblei

'''

## *demo01* +
This demo starts near the start of the module. The intent is to do the manual
install of several applications
Instructor lead install of packages on ansible test machine. +
Install packages (to be updated when test application is known) +

 $ sudo apt-get install htop
 $ sudo apt-get install nmon
 $ sudo apt-get install tree

Instructor lead install of application x on ansible test machine. +

 $ sudo apt-get install
 $ git clone <url>

Instructor lead moving of configuration for wordpress application +

 $ scp source destination

Instructor lead starting of application x  +

 $ sudo start application x

Instructor valdiation of applicatio x functionality +

 Open browser, go to http(s)//localhost:<port>

## *demo 02*
This demo kicks off during the python block of instruction and continues to run
in concert to the lectures covering python, apt-get ansible, ansible.cfg,
inventory.ini, and core modules.


### *Python version* +
Python version 2.x is the base requirement for Ansible. To check for version
of Python, run python:

 $ python
 Python 2.7.6 (default, Jun 22 2015, 17:58:13)
 [GCC 4.8.2] on linux2
 Type "help," "copyright", "credits" or "license" for more information.
 >>> exit()
 $

### *Install Ansible*
Dependencies:
software-properties-common +

 $ sudo apt-get -y install software-properties-common
 $ sudo apt-add-repository -y ppa:ansible/ansible
 $ sudo apt-get update
 $ sudo apt-get -y install ansible

Once Ansible is installed, Ansible is tested

 $ ansible
 Usage: ansible <host-pattern> [options]
 Options:
  -a MODULE_ARGS, --args=MODULE_ARGS
                        module arguments
  --ask-become-pass     ask for privilege escalation password
  -k, --ask-pass        ask for connection password
  --ask-su-pass         ask for su password (deprecated, use become)
  -K, --ask-sudo-pass   ask for sudo password (deprecated, use become)
  --ask-vault-pass      ask for vault password

Check the installed version of ansible:

 ansible --version
 ansible 2.0.0.2
  config file = /home/vagrant/ansible.cfg
  configured module search path = Default w/o overrides

### *Overview of the /etc/ansible/ansible.cfg file*
The ansible.cfg maintains the configuration parameters of Ansible.
Student and Instructor open /etc/ansible/ansible.cfg and discuss content.
On Ansible Control Server <lab_server_name>, run the following:

 $ cat /etc/ansible/ansible.cfg

### *Overview of the /etc/ansible/hosts file* +
The hosts (inventory file) provides a list of potential ansible targets.
Student and Instructor open /etc/ansible/hosts and discuss content.
On Ansible Control Server <lab_server_name>, run the following:

 $ cat /etc/ansible/hosts

### *Overview of install CORE modules*
The ansible Core modules are modules that ship Ansible.
link: https://github.com/ansible/ansible-modules-core

 $ ansible-doc --list

### *recap architecture*
The above demos are instructor lead and used to illustrate the architecture of
ansible from a high level.

