Vagrant.configure("2") do |config|
  
  config.vm.define "db" do |db|
    db.vm.box = "ubuntu/xenial64"
    db.vm.hostname = "db"
    db.vm.network :private_network, ip: "10.0.0.11"
  end

  config.vm.define "app" do |app|
    app.vm.box = "ubuntu/xenial64"
    app.vm.hostname = "app"
    app.vm.network :forwarded_port, guest: 80, host: 8080
    app.vm.network :private_network, ip: "10.0.0.10"
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "ansible/site.yml"
    ansible.compatibility_mode = "2.0"
  end

end
