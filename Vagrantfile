Vagrant.configure("2") do |config|
config.vm.box = "ubuntu/jammy64"
config.vm.hostname = "linux-practice"
config.vm.provider "virtualbox" do |vb|
vb.memory = "2048"
vb.cpus = 2
# Agregar disco adicional de 2GB para ejercicios de LVM
unless File.exist?('./disk1.vdi')
vb.customize ['createhd', '--filename', './disk1.vdi', '--size',
2048]
end
vb.customize ['storageattach', :id, '--storagectl', 'SCSI',
'--port', 2, '--device', 0, '--type', 'hdd', '--medium', './disk1.vdi']
end
config.vm.network "public_network"
config.vm.provision "shell", inline: <<-SHELL
apt-get update
apt-get install -y fastfetch git docker.io docker-compose lvm2
usermod -aG docker vagrant
systemctl enable docker
systemctl start docker
SHELL
end

