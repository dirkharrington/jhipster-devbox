Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/bionic64"
    config.vm.provision :shell, :path => "scripts/setup.sh"
    config.vm.network :forwarded_port, host: 8080, guest: 30080
    config.vm.network :forwarded_port, host: 27017, guest: 27017
    config.vm.network :forwarded_port, host: 27018, guest: 27018
    config.vm.network :forwarded_port, host: 5601, guest: 5601
    config.vm.network :forwarded_port, host: 8081, guest: 5601
    config.ssh.insert_key = true

    config.vm.provider :virtualbox do |vb|
        vb.gui = true
        # Use VBoxManage to customize the VM. For example to change memory:
        vb.customize ["modifyvm", :id, "--name", "devbox"]
        vb.customize ["modifyvm", :id, "--memory", "8192"]
        vb.customize ["modifyvm", :id, "--vram", 64]
        vb.customize ["modifyvm", :id, "--accelerate3d", "on"]
        vb.customize ['modifyvm', :id, '--clipboard', 'bidirectional']
        vb.customize ['modifyvm', :id, '--draganddrop', 'bidirectional']
    end
end
