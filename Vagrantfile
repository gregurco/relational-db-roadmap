Vagrant.configure(2) do |config|
    config.vm.define "mysql_master", primary: true do |mysql_master|
        mysql_master.vm.box = "ubuntu/xenial64"
        mysql_master.vm.network "private_network", ip: "192.168.0.250"
        mysql_master.vm.hostname = "mysql-master"
        mysql_master.vm.provision "shell", path: "scripts/install.sh"
        mysql_master.vm.provider "virtualbox" do |v|
            v.memory = 4096
            v.cpus = 2
        end
    end
    config.vm.define "mysql_slave" do |mysql_slave|
        mysql_slave.vm.box = "ubuntu/xenial64"
        mysql_slave.vm.network "private_network", ip: "192.168.0.251"
        mysql_slave.vm.hostname = "mysql-slave"
        mysql_slave.vm.provision "shell", path: "scripts/install.sh"
        mysql_slave.vm.provider "virtualbox" do |v|
            v.memory = 4096
            v.cpus = 2
        end
    end
end
