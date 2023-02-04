# replace bridge with system's network interface
# windows: ipconfig
# mac: ifconfig

# Windows
BRIDGE_ADAPTER = "Ethernet adapter Ethernet"
# Mac
# BRIDGE_ADAPTER = "en0"
Vagrant.configure("2") do |config|
  # Provision base virtual machine
  config.vm.hostname = "pg.wander.local"
  config.vm.box = "ubuntu/trusty64"

  config.vm.network "public_network", bridge: BRIDGE_ADAPTER
  config.vm.provider "virtualbox" do | virtualbox |
    virtualbox.cpus = 2
    virtualbox.memory = 2048
  end
end

