VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.box_check_update = false
  config.ssh.forward_agent = true

  config.ssh.shell = "bash -c 'BASH_ENV=/etc/profile exec bash'"

  config.vm.network "forwarded_port", guest: 3009, host: 3009
  # config.vm.network "forwarded_port", guest: 80, host: 10080
  # config.vm.network "private_network", ip: "192.168.33.10"
  # config.vm.network "public_network"

  # config.vm.synced_folder "../data", "/vagrant_data"

  description = {:username=>"zouhaisong", :password=>"123456",
    :usage=>"ubuntu workspace to spike rocketchat", :os=>"ubuntu"
  }

  config.vm.provider :virtualbox do |vb|
    vb.name = "spike-rocketchat"
    vb.memory = 2048
    vb.cpus = 2
    vb.customize ["modifyvm", :id, "--description", description.to_json]
  end
  config.vm.provision :shell, path: "bootstrap.sh"
end
