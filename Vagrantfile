Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"

  config.vm.network "forwarded_port", guest: 8080, host: 8081

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "8192"
  end

  config.vm.provision "shell", inline: "sudo apt-get update && sudo apt-get upgrade -y && sudo apt-get install -y wget python3; sudo ln -sf /usr/bin/python3 /usr/bin/python"

  config.vm.provision "ansible" do | ans |
    ans.playbook = "playbooks/playbook.yml"
  end

end
