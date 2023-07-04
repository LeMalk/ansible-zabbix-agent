Vagrant.configure("2") do |config|
  
  config.vm.box = "ubuntu/focal64"

  config.vm.synced_folder "./ansible", "/ansible"

  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install -y ansible
    ansible-playbook --connection=local /ansible/playbook.yml
  SHELL

end