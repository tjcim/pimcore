Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-20.04"
  # config.vm.post_up_message = $msg
  config.ssh.forward_x11 = true

  config.vm.network "forwarded_port", guest: 8085, host: 8085

  config.vm.provider "virtualbox" do |vb|
    vb.name = "pimcore"
    vb.memory = "4096"
    vb.cpus = "2"
    vb.customize ["modifyvm", :id, "--clipboard-mode", "bidirectional"]
    vb.customize ["modifyvm", :id, "--draganddrop", "bidirectional"]
  end
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provision/main.yml"
    ansible.compatibility_mode = "2.0"
  end
end
