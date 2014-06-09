# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version.
# Don't be touching this, Matey, lest ye send us all down to Dany Jones' locker!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.hostname = "aegir3.dev"

  config.vm.box = "hashicorp/precise64"

  config.vm.network "private_network", ip: "10.42.42.42"

  config.vm.provision "puppet" do |puppet|
    puppet.module_path = "modules"
    puppet.manifests_path = "manifests"
    puppet.manifest_file  = "nodes.pp"
    puppet.facter = {
      "fqdn" => "aegir3.dev"
    }
  end

end

