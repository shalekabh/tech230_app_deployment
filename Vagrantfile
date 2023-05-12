Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/xenial64"
  config.vm.network "private_network", ip:"192.168.10.100"
  #provision the VM to have nginx
  #config.vm.provision "shell", inline: <<-SHELL
    #sudo apt-get update -y
    #sudo apt-get upgrade -y
    #sudo apt-get install -y nginx
    #sudo systemctl enable nginx
    #sudo systemctl start nginx
    #cd tech230_app_deployment
    #cd app
    #sudo apt-get install nodejs -y
    #sudo apt-get install python-software-properties
    #curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -
    #sudo apt-get install nodejs -y
    #sudo npm install pm2 -g
    #npm start

  #SHELL

  config.vm.provision "shell", path: "provisions.sh"

  # Put the app folder from our local machine to the VM

  config.vm.synced_folder "app", "/home/vagrant/app"

end
