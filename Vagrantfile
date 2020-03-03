Vagrant.configure("2") do |config|
  config.vm.box = "opensuse/Tumbleweed.x86_64"
  config.vm.hostname = "laboratorio-01"
  config.vm.network :private_network, :ip => "10.10.0.100"
  config.vm.synced_folder "www", "/var/www"

config.vm.provider :virtualbox do |v| 
	v.cpus = 1
	v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
	v.customize ["modifyvm", :id, "--memory", 512]
	v.customize ["modifyvm", :id, "--name", "laboratorio-01"]

	end
end
