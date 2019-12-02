Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/bionic64"

    #config.vm.synced_folder "\%HOMEPATH%\.aws\credentials", "/home/vagrant/.aws/credentials", type: "smb"

    config.vm.provision "ansible" do |ansible|
        # ~ expansion did not work (unless the playbook was in the same dir)
        ansible.playbook = "playbook.yaml"
        ansible.extra_vars = {
        #env: "sandbox"
        }
    end

end