Vagrant.require_version ">= 2.2.4"

Vagrant.configure("2") do |config|

  # Global configuration
  config.vm.box_check_update = true
  config.vm.communicator = "ssh"
  config.vm.graceful_halt_timeout = 60

  # VirtualBox configuration
  config.vm.provider "virtualbox" do |vb|
    vb.cpus = 2
    vb.customize ["modifyvm", :id, "--audio", "none"]
    vb.customize ["modifyvm", :id, "--boot1", "dvd"]
    vb.customize ["modifyvm", :id, "--boot2", "disk"]
    vb.customize ["modifyvm", :id, "--boot3", "none"]
    vb.customize ["modifyvm", :id, "--boot4", "none"]
    vb.customize ["modifyvm", :id, "--description", "Boom"]
    vb.customize ["modifyvm", :id, "--groups", "/Ansible-test"]
    vb.customize ["modifyvm", :id, "--vram", "64"]
    vb.gui = false
    vb.linked_clone = false
    vb.memory = "1024"
  end

  # Centos box
  config.vm.define "ansible-cts" do |cts|
    cts.vm.box = "generic/centos7"
    cts.vm.box_version = ">= 4.3.12"
    cts.vm.hostname = "ansible-cts"
    cts.vm.network "private_network", ip: "192.168.56.20"
    cts.vm.post_up_message = "Starting ansible-cts"
  end

  # Debian box
  config.vm.define "ansible-deb" do |deb|
    deb.vm.box = "generic/debian12"
    deb.vm.box_version = ">= 4.3.12"
    deb.vm.hostname = "ansible-deb"
    deb.vm.network "private_network", ip: "192.168.56.21"
    deb.vm.post_up_message = "Starting ansible-deb"
  end

  # Ubuntu box
  config.vm.define "ansible-ubt" do |ubt|
    ubt.vm.box = "generic/ubuntu2204"
    ubt.vm.box_version = ">= 4.3.12"
    ubt.vm.hostname = "ansible-ubt"
    ubt.vm.network "private_network", ip: "192.168.56.22"
    ubt.vm.post_up_message = "Starting ansible-ubt"
  end

  # Mint box
  config.vm.define "ansible-sls" do |sls|
    sls.vm.box = "generic/opensuse15"
    sls.vm.box_version = ">= 4.3.12"
    sls.vm.hostname = "ansible-sls"
    sls.vm.network "private_network", ip: "192.168.56.23"
    sls.vm.post_up_message = "Starting ansible-sls"
  end

end
