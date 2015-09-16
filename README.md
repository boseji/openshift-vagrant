# OpenShift Vagrant

This repository helps to create a **stable VM environment** using [*Virtual Box*](https://www.virtualbox.org/) and 
[*Vagrant*](https://www.vagrantup.com/) for working with [**Redhat's OpenShift**](https://openshift.redhat.com).

Additionally the internal provisioning adds packages `ruby-full`,`rubygems`, 
`python` and `node` to help in web-development.



## Dependencies

One must have the following software installed:

*  [VirtualBox](https://www.virtualbox.org/wiki/Downloads) - At least Version 5.0.4 (at the time of writing this)
*  [Vagrant](https://www.vagrantup.com/downloads.html)


## Usage

Clone this repository or download+extract the Zip of this repository.

In a command terminal, *(In windows use **GIT-BASH** as not all commands will work)* 
type the following commands:

    vagrant up

After this there would be a long process of downloads and internal processing steps done by *Vagrant* to setup the VM. 
It might take a while to get this ready. After this is done the VM would be created into its default directory.
Enter the following command to communicate with the VM using SSH.
    
    vagrant ssh

For the First time user you would need to Configure the `rhc` tool for working with **OpenShift**.
Run the folowing Command to setup ( This only needs to be run once ):

    rhc setup

In this program press enter for the Server name `|openshift.redhat.com|`

Next Enter the Login and Password for your *OpenShift Account*

Allow the program to create the keys needed and upload them by typing `yes`

Thats It! you VM would be now read to work with ***OpenShift***


## Notes for Vagrant

Additionally if you would like to ShutDown the VM instance *which is needed always* after everthing is done give the following command:

     vagrant halt

This would shutdown the VM and can be started back again in the same way by giving the `vagrant up` command.


In case things have gone wrong and you wish the start again from scratch give the following command sequence:

    vagrant destroy
    rm -rf .vagrant

Everything along with the VM would be deleted from the HDD and one can start a fresh by giving the `vagrant up` command. Also *not to worry about Download of VM*, the one that was done earlier is still in the **Vagrant local** area so it would be fast to make the VM again.


## License

Released under the [MIT License]()
