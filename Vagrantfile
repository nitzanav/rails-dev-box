# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure('2') do |config|

  config.vm.provider "virtualbox" do |v|
    v.memory = 2048
  end

  config.vm.box      = 'ubuntu/trusty64'
  config.vm.hostname = 'rails-dev-box'

  config.vm.network :forwarded_port, guest: 3000, host: 3000, auto_correct: true
  config.vm.network :forwarded_port, guest: 9292, host: 9292, auto_correct: true

  # config.vm.network :forwarded_port, guest: 3000, host: 80, auto_correct: true
  # config.vm.network :forwarded_port, guest: 9292, host: 80, auto_correct: true

  config.vm.provision :shell, path: 'bootstrap.sh', keep_color: true
end
