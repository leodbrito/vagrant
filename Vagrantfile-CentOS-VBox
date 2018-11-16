# Vagrantfile CentOS

# -*- mode: ruby -*-

# vi: set ft=ruby :

Vagrant.configure("2") do |config|

	#servidores para o labotorio do Vagrant
	config.vm.define :vm1 do |config|
		config.vm.hostname = "vm1.myproject.local"
		config.vm.provider "virtualbox"
		config.vm.box = "centos/7"
		#config.vm.box_url = ""
		config.vm.network "private_network", ip:"192.168.2.11", virtualbox__intnet: "InernalNetwork"
		config.disksize.size = '20GB'
		#config.vm.synced_folder ".", "/vagrant", disabled: true
		config.vm.synced_folder ".", "/vagrant"
		config.vm.provision "shell", inline: <<-SHELL
			yum -y install epel-release
			yum -y install net-tools
			yum -y install netcat
			yum -y install nmap
			yum -y install traceroute
			yum -y install telnet
			yum -y install glances
			yum -y install git
			yum -y install vim
		SHELL
		
		config.vm.provider "virtualbox" do |vb|
			vb.name = "CentOS7_vm1"
			vb.cpus = "1"
			vb.memory = "1024"
		end
	end
	
	
	config.vm.define :vm2 do |config|
		config.vm.hostname = "vm2.myproject.local"
		config.vm.provider "virtualbox"
		config.vm.box = "centos/7"
		#config.vm.box_url = ""
		config.vm.network "private_network", ip:"192.168.2.12", virtualbox__intnet: "InternalNetwork"
		config.disksize.size = '20GB'
		#config.vm.synced_folder ".", "/vagrant", disabled: true
		config.vm.provision "shell", inline: <<-SHELL
			yum -y install epel-release
			yum -y install net-tools
			yum -y install netcat
			yum -y install nmap
			yum -y install traceroute
			yum -y install telnet
			yum -y install glances
			yum -y install vim
			yum -y install git
		SHELL
		
		config.vm.provider "virtualbox" do |vb|
			vb.name = "CentOS7_vm2"
			vb.cpus = "1"
			vb.memory = "1024"
		end
	end
# Exemplo de loop para criação de maquinas virtuais:
#	(1..3).each do |i|
#		config.vm.define "node-#{i}" do |node|
#		node.vm.provision "shell",
#		inline: "echo hello from node #{i}"
#		end
#	end
end
