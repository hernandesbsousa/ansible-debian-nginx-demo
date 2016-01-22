Vagrant.configure(2) do |config|
  config.vm.box = "debian/wheezy64"

  config.vm.hostname = "myserver"

  config.vm.network "private_network", ip: "192.168.33.11"

  config.vm.provision "ansible" do |ansible|
    ansible.groups = { "webservers" => ["default"] }
    ansible.playbook = "./playbook.yml"
    ansible.ask_sudo_pass = true
  end

end
