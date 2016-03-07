#Overview
This is an [Ansible](http://www.ansible.com/) playbook designed to tweak a fresh 
[Ubuntu 14.04](http://www.ubuntu.com/) desktop installation.

#Prerequisites

* an Ubuntu Desktop instance with [SSH](http://www.openssh.com/) enabled and working
* the instance must have a user that has `sudo` privledges
* a box with the most current Ansible installed
 
#Building
Since this project is just a collection of configuration and data files for Ansible to consume, no building is necessary.

#Installation
The first step is to get the files onto your Ansible box.  A great way is to use [Git](https://git-scm.com/) and
simply clone this project via `git clone https://github.com/kurron/ansible-ubuntu-desktop.git`.

Once you have the files available to you, you are going to have to edit the `hosts` file with a text editor.  The 
file is documented and should be easily understood. **You must also edit the `ansible.cfg` file, specifically the 
`remote_user` property.**  Failure to do this will prevent Ansible from SSH'ing into the instance.

To install the environment all you have to do is issue `./playbook.yml` from the command line.  Ansible will ask you for the password 
of the SSH account being used as well as the password to use for `sudo` (normally, you can just hit `Enter` here). You will 
also be prompted for configuration values that have reasonable defaults that can optionally be changed. the In a few moments your instance 
should be provisioned and ready to go.  **Please note that you must reboot the instance in order for some of the optimizations to take affect.** 

#Tips and Tricks

#Troubleshooting

##Only Works On Ubuntu
When Ansible runs, it gathers up information about the target machine and will refuse to provision machine if 
it isn't an Ubuntu box.

#License and Credits
This project is licensed under the [Apache License Version 2.0, January 2004](http://www.apache.org/licenses/).

#List of Changes
