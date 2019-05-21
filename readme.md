## This repository provides a simple Vagrantfile to use with Vagrant, providing 1 VM with 2 CPUs and 2GB of RAM.

## How to install Vagrant :

- Information about installing Vagrant can be found on the official HashiCorp website [here](https://www.vagrantup.com/docs/installation/)

## How to use it :

- In a directory of your choice, clone the github repository with `git clone https://github.com/martinhristov90/vagrant1VM.git`
- Change into the directory using : `cd vagrant1VM`
- Execute `vagrant up`
- It might take some time to download the boxes since you do not have them added to Vagrant.
- Check with `vagrant status` that you have both Vagrant boxes running. The output should look like this:

```shell

Current machine states:

web                       running (virtualbox)

The VM is running. To stop this VM, you can run `vagrant halt` to
shut it down forcefully, or you can run `vagrant suspend` to simply
suspend the virtual machine. In either case, to restart it again,
simply run `vagrant up`.

```

- To verify the HW parameters of the VM, please do the following :
    - SSH to the VM with : `vagrant ssh`
    - Execute the following command : `lscpu | grep ^CPU\(s\) && free -m`
    - The output shows that 2 CPUs are avaiable and the VM has 2GB of ram, the output should look like this :
        ```shell
        CPU(s):                2
                      total        used        free      shared  buff/cache   available
        Mem:           2000          31        1397           3         571        1813
        Swap:          1023
        ```

- To stop the running machines execute `vagrant halt`, to destroy the setup use `vagrant destroy`.

