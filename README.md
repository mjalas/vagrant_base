# Vagrant base

Vagrant base provides a base structure for Vagrant usage. The project provides a modular way of adding shell scripts for provisioning a virtual machine environment, through shell provisioning.
Other tools are also available that provides more or less the same functionality, but this project provides a mean of working with shell scripts to provision a Vagrant vm.

## Getting started

A simple base provision script is provided as an example, and should be modified according to users needs. The configuration file enables usage of adding additional provisioning scripts, by adding the file names into the 'extra-provision' list. 

Additional Vagrant configurations can be added into the Vagrantfile, as with normal Vagrant usage. The provided Vagrantfile does only include the required configurations to enable modular shell script provisioning.

