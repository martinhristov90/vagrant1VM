# This Vagrantfile provides 1 VM with 2 CPUs and 2GB of RAM.
Vagrant.configure("2") do |config|
    #Defining the VM
    config.vm.define vm_name="web" do |node|
        node.vm.box = "martinhristov90/ubuntu_nginx"
        node.vm.hostname = vm_name
    end
    #Defining the HW parametars of the VM.
    config.vm.provider "virtualbox" do |v|
        v.memory = 2048
        v.cpus = 2
    end
end
