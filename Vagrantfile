Vagrant.configure(2) do |config|
  config.vm.box = "hellofresh/mapr"
  
  # Configure synced folder on host machine
  config.vm.synced_folder "../", "/hellofresh"
  
  # Configure private network IP. Default is 10.10.10.30
  config.vm.network "private_network", ip: "10.10.10.30"

  # Configure Virtualbox VM. Default is 4 CPUs and 8 GB of RAM
  # config.vm.provider "virtualbox" do |v|
  #	  v.memory = 1024
  # 	  v.cpus = 2
  # end
end
