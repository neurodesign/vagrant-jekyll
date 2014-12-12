# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.box = "ubuntu/trusty64"
  config.vm.box_url = "http://files.vagrantup.com/precise32.box"

  config.vm.network "forwarded_port", guest: 4000, host: 4000 

  config.vm.provision :shell,
    :privileged => true,
    :inline => "apt-get -y install ruby1.9.3 && apt-get -y install nodejs && gem install github-pages --no-ri --no-rdoc"
  config.vm.provision :shell,
    :run => "always",
    :inline => "cd /vagrant/pages && screen -d -m jekyll serve -P 4000 --watch --force_polling"
end
