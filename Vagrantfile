# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/trusty64"
  config.ssh.insert_key = false

  config.vm.provider :virtualbox do |v|
    v.memory = 256
    v.linked_clone = true
  end

  # App
  config.vm.define "app" do |app|
    app.vm.hostname = "app.host"
    app.vm.network :private_network, ip: "192.168.33.10"
  end

  # Prometheus
  config.vm.define "prometheus" do |prometheus|
    prometheus.vm.hostname = "prometheus.host"
    prometheus.vm.network :private_network, ip: "192.168.33.11"
  end
end
