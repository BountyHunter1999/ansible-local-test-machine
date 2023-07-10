# ansible-local-test-machine

## Simple Server

[Simple Server Setup](./server/Vagrantfile)
![Simple Server](./server/simple_server.png)

### Windows

- For the windows machine without wsl2, I create a separate ansible control machine and work from there

### Linux

- For Linux, vagrant provision with ansible might be easier

```ruby
Vagrant.configure("2") do |config|
  config.vm.box = "geerlingguy/rockylinux8"

  # Provisioning configuration for Ansible
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end
end
```
