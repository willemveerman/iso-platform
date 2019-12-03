Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/bionic64"

    config.vm.synced_folder ENV["HOMEPATH"] + "\\.aws", "/root/.aws", type: "smb"

    config.vm.provision "ansible_local" do |ansible|
        ansible.playbook = "playbook.yaml"
        ansible.extra_vars = {
        tf_version: "0.12.16",
        eksctl_version: "latest_release" # 0.10.2
        }
    end

end