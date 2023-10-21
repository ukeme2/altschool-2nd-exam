Vagrant.configure("2") do |config|
  config.vm.define "master" do |master|
    master.vm.hostname = "master"
    master.vm.box = "ubuntu/focal64"
    master.vm.network "private_network", ip:"192.168.20.11"
    master.vm.provision "shell", path: "test-laravel.sh"
  end

  config.vm.define "slave" do |slave|
    slave.vm.hostname = "slave"
    slave.vm.box = "ubuntu/focal64"
    slave.vm.network "private_network", ip: "192.168.20.12"
  end

    config.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
      vb.cpus = "2"
    end
end
