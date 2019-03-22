Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.network "forwarded_port", guest: 5000, host: 80
  config.vm.network "private_network", ip: "10.10.10.20"
  ####### Provision #######
  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "provision/playbook.yml"
    ansible.verbose = true
    ansible.install_mode = "pip"
  end
end
