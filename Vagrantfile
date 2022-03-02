Vagrant.configure("2") do |config|

  # config.vm.box = "rockylinux/8"
  config.vm.box = "almalinux/8"
  config.ssh.insert_key = false

    # Web Server 1.
    config.vm.define "srv1" do |app|
      app.vm.hostname = "web1"
      config.vm.network "private_network", ip: "192.168.60.8"
      config.vm.provision :shell, :inline => "sudo sed -i 's/PasswordAuthentication no/PasswordAuthentication yes/g' /etc/ssh/sshd_config; sudo systemctl restart sshd;", run: "always"
    end
  
  #   Web Server 2.
  #  config.vm.define "srv2" do |app|
  #    app.vm.hostname = "web2"
  #    config.vm.network "private_network", ip: "192.168.60.9"
  #    config.vm.provision :shell, :inline => "sudo sed -i 's/PasswordAuthentication no/PasswordAuthentication yes/g' /etc/ssh/sshd_config; sudo systemctl restart sshd;", run: "always"
  #  end

end
