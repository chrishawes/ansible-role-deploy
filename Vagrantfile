VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "ubuntu/trusty64"
  config.vm.network "private_network", ip: "33.33.66.66"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "test.yml"
  end

end
