Vagrant.configure("2") do |config|
    config.vm.boot_timeout = 1200
    # Configuration for the "Master" server
    config.vm.define "Master" do |master|
      master.vm.box = "ubuntu/focal64"
      master.vm.hostname = "Master"
      master.vm.network "private_network", type: "dhcp"
    end
    # Configuration for the "Slave" server
    config.vm.define "Slave" do |slave|
      slave.vm.box = "ubuntu/focal64"
      slave.vm.hostname = "Slave"
      slave.vm.network "private_network", type: "dhcp"
    end
  end
