Vagrant.configure("2") do |config|
    config.vm.box = "bento/opensuse-leap-42"
    config.vm.define "hab-studio", primary: true do |host|
        host.vm.provider "virtualbox" do |v|
            v.memory = 2048 # increase memory from 1024
        end
        host.vm.hostname = "hab-studio"
        host.vm.network "private_network", type: "dhcp"
        host.vm.provision "shell", path: "bootstrap.sh"
    end
end