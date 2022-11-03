
Vagrant.configure("2") do |config|

  config.vm.box_check_update = false

  # Creates prometheus VM
  config.vm.define "prometheus" do |prometheus|
    prometheus.vm.box = "ubuntu/focal64"
    # Create a private network, which allows host-only access to the machine using a specific IP.
    prometheus.vm.network "public_network", ip: "192.168.10.20", bridge: "enp6s0"

    # Customize the amount of memory and cpu on the VM:
    prometheus.vm.provider "virtualbox" do |vb|
      vb.gui = false
      vb.name = "prometheus"
      vb.memory = 512
      vb.cpus = 1  
    end
    prometheus.vm.provision "shell" do |s|
      ssh_pub_key = File.readlines("/.ssh/vagrant.pub").first.strip
      s.inline= <<-SHELL 
        echo #{ssh_pub_key} >> /home/vagrant/.ssh/authorized_keys
        echo #{ssh_pub_key} >> /root/.ssh/authorized_keys
      SHELL
    end
  end

# -----------------------------------------------------------------------------------------------------
  # Creates s1 VM
  config.vm.define "s1" do |s1|
    s1.vm.box = "ubuntu/focal64"
    # Create a private network, which allows host-only access to the machine using a specific IP.
    s1.vm.network "public_network", ip: "192.168.10.21", bridge: "enp6s0"
    
    # Customize the amount of memory and cpu on the VM:
    s1.vm.provider "virtualbox" do |vb|
      vb.gui = false
      vb.name = "s1"
      vb.memory = 512
      vb.cpus = 1
    end
    s1.vm.provision "shell" do |s|
      ssh_pub_key = File.readlines("/.ssh/vagrant.pub").first.strip
      s.inline= <<-SHELL 
        echo #{ssh_pub_key} >> /home/vagrant/.ssh/authorized_keys
        echo #{ssh_pub_key} >> /root/.ssh/authorized_keys
      SHELL
    end
  end
# -----------------------------------------------------------------------------------------------------
  # Creates s2 VM
  config.vm.define "s2" do |s2|
    s2.vm.box = "ubuntu/focal64"
    # Create a private network, which allows host-only access to the machine using a specific IP.
    s2.vm.network "public_network", ip: "192.168.10.22", bridge: "enp6s0"
    
    # Customize the amount of memory and cpu on the VM:
    s2.vm.provider "virtualbox" do |vb|
      vb.gui = false
      vb.name = "s2"
      vb.memory = 512
      vb.cpus = 1
    end
    s2.vm.provision "shell" do |s|
      ssh_pub_key = File.readlines("/.ssh/vagrant.pub").first.strip
      s.inline= <<-SHELL 
        echo #{ssh_pub_key} >> /home/vagrant/.ssh/authorized_keys
        echo #{ssh_pub_key} >> /root/.ssh/authorized_keys
      SHELL
    end
  end

  # -----------------------------------------------------------------------------------------------------
  # Creates s2 VM
  config.vm.define "s3" do |s3|
    s3.vm.box = "ubuntu/focal64"
    # Create a private network, which allows host-only access to the machine using a specific IP.
    s3.vm.network "public_network", ip: "192.168.10.24", bridge: "enp6s0"
    
    # Customize the amount of memory and cpu on the VM:
    s3.vm.provider "virtualbox" do |vb|
      vb.gui = false
      vb.name = "s3"
      vb.memory = 512
      vb.cpus = 1
    end
    s3.vm.provision "shell" do |s|
      ssh_pub_key = File.readlines("/.ssh/vagrant.pub").first.strip
      s.inline= <<-SHELL 
        echo #{ssh_pub_key} >> /home/vagrant/.ssh/authorized_keys
        echo #{ssh_pub_key} >> /root/.ssh/authorized_keys
      SHELL
    end
  end

end

