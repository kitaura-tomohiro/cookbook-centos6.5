Vagrant.configure(2) do |config|
  config.vm.box = "chef/centos-6.5"
  config.vm.hostname = "vagrant-centos6.5"

  # config.vm.box_check_update = false

  #config.vm.network "forwarded_port", guest: 80, host: 2015
  config.vm.network "private_network", ip: "192.168.33.10"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook-centos65.yml"
    #ansible.inventory_path = "hosts"
    ansible.limit = "all"
    ansible.verbose = "v"
  end

end