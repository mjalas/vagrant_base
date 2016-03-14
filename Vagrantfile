# -*- mode: ruby -*-
# vi: set ft=ruby :

require 'yaml'

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

current_dir = File.dirname(File.expand_path(__FILE__))
configs = YAML.load_file("#{current_dir}/config.yaml")
vagrant_config = configs['configs']
vagrant_provision = vagrant_config['provision']
provision_path = vagrant_provision['provision-folder']
base_provision = provision_path + "/" + vagrant_provision['base-provision']

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  
  config.vm.box = "ubuntu/trusty64"

  config.vm.provision "shell", path: base_provision
  vagrant_provision['extra_provision'].each do |filename|
  	if !filename.nil? && !filename.empty?
  		config.vm.provision "shell", path: "#{provision_path}/#{filename}"
    end
  end  
end