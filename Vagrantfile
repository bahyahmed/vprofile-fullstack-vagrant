Vagrant.configure("2") do |config|
  config.hostmanager.enabled = true
  config.hostmanager.manage_host = true

  ### DB VM ###
  config.vm.define "db01" do |db01|
    db01.vm.box = "centos/stream9"
    db01.vm.hostname = "db01"
    db01.vm.network "private_network", ip: "192.168.56.15"
    db01.vm.provider "virtualbox" do |vb|
      vb.memory = "512"
    end
    db01.vm.provision "shell", path: "scripts/mysql.sh"
  end

  ### Memcache VM ###
  config.vm.define "mc01" do |mc01|
    mc01.vm.box = "centos/stream9"
    mc01.vm.hostname = "mc01"
    mc01.vm.network "private_network", ip: "192.168.56.14"
    mc01.vm.provider "virtualbox" do |vb|
      vb.memory = "256"
    end
    mc01.vm.provision "shell", path: "scripts/memcache.sh"
  end

  ### RabbitMQ VM ###
  config.vm.define "rmq01" do |rmq01|
    rmq01.vm.box = "centos/stream9"
    rmq01.vm.hostname = "rmq01"
    rmq01.vm.network "private_network", ip: "192.168.56.16"
    rmq01.vm.provider "virtualbox" do |vb|
      vb.memory = "512"
    end
    rmq01.vm.provision "shell", path: "scripts/rabbitmq.sh"
  end

  ### Tomcat VM ###
  config.vm.define "app01" do |app01|
    app01.vm.box = "centos/stream9"
    app01.vm.hostname = "app01"
    app01.vm.network "private_network", ip: "192.168.56.12"
    app01.vm.provider "virtualbox" do |vb|
      vb.memory = "512"
    end
    app01.vm.provision "shell", path: "scripts/tomcat.sh"
  end

  ### Nginx VM ###
  config.vm.define "web01" do |web01|
    web01.vm.box = "ubuntu/jammy64"
    web01.vm.hostname = "web01"
    web01.vm.network "private_network", ip: "192.168.56.11"
    web01.vm.provider "virtualbox" do |vb|
      vb.memory = "512"
    end
    web01.vm.provision "shell", path: "scripts/nginx.sh"
  end
end

