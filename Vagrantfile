Vagrant.configure("2") do |config|
	config.vm.box = "centos/7"
	config.vm.network :public_network, ip: "192.168.1.103", netmask: "255.255.255.0"
	config.vm.provision "ansible_local" do |ansible|
		ansible.playbook = "provisioning/playbook.yaml"
		ansible.limit = "all,localhost"
	end	

end