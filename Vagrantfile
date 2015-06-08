
unless Vagrant.has_plugin?('vagrant-hostmanager')
  raise 'Please run --- vagrant plugin install vagrant-hostmanager ---'
end

ip = "10.20.1.11"
hostname = "ipc15se";

Vagrant.configure("2") do |config|

  config.vm.define hostname do |pagetion|
  
    pagetion.vm.box = "ubuntu/trusty64"
    
    pagetion.vm.hostname = hostname 
    
    pagetion.vm.network "private_network", :ip => ip
   
    pagetion.hostmanager.enabled     = true
    pagetion.hostmanager.manage_host = true

    pagetion.vm.provider :virtualbox do |vm|
      vm.memory = 1024
    end
  
    pagetion.vm.provision :ansible do |ansible|
      
      ansible.playbook = "provisioning/playbook.yml"

    end
   
  end
 
end