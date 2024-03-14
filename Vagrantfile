Vagrant.configure("2") do |config|
  config.vm.define "ansible" do |ansible|
    ansible.vm.box = "ubuntu/jammy64"
    ansible.vm.network "private_network", type: "static", ip: "192.168.99.10"
    ansible.vm.hostname = "ansible"
    ansible.vm.provider "virtualbox" do |v|
      v.name = "ansible"
      v.memory = 2048
      v.cpus = 2
    end
  end

  ram_client=2048
  cpu_client=2
  config.vm.define "client1" do |client|
    client.vm.box = "ubuntu/jammy64"
    client.vm.network "private_network", type: "static", ip: "192.168.99.11"
    client.vm.hostname = "client1"
    client.vm.provider "virtualbox" do |v|
      v.name = "client1"
      v.memory = ram_client
      v.cpus = cpu_client
    end
  end
end
