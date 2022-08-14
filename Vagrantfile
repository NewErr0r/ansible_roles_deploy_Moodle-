Vagrant.configure("2") do |config|

#--------------------------------Debian-----------------------------------------

    config.vm.define "debian" do |debian|
        debian.vm.hostname = "debian"
        debian.vm.box = "generic/debian11"
        debian.vm.network "public_network", bridge: "br0", ip: "192.168.0.152"

        debian.vm.provider "virtualbox" do |vb|
           vb.name = "debian"
            vb.cpus = 2
            vb.memory = "4096"
        end

    debian.vm.provision "shell", inline: <<-SHELL
        sudo echo "root:toor" | chpasswd
    SHELL
   end
##############################################################
end