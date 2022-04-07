Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/impish64"
  config.vm.hostname = "cloud-orchestration"
  config.vm.provision "shell", path: "terraform.sh", run: "once"
  config.vm.network :private_network, ip: "10.0.1.10"
  config.vm.provider "virtualbox" do |v|
    v.name = "cloud-orchestration"
    v.cpus = 2
    v.memory = 4096
  end
end