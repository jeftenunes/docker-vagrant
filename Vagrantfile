Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.define "docker" do |docker|
    docker.vm.provider "virtualbox" do |vbox|
      vbox.cpus = 1
      vbox.memory = 512
      vbox.name = "docker_host"
    end

    docker.vm.provision "shell",
      inline: "apt-get update && apt-get install -y docker.io"
  end
end