# Build docker image by Packer on OSX

* Now packer provision with docker from osx docker client is [not worked]((https://github.com/mitchellh/packer/issues/901).

## How to build

Run docker 

```
$ vagrant up
```

This will install docker and packer in vagrant box.

```
$ vagrant ssh
```

### Chef

Build docker image with chef provisioning

```
$ packer build machine_chef.json
```

Check it.

```bash
$ docker run -t -i tcnksm/packer-chef:0.1 bash
```

### Puppet

Build docker image with pupet provisioning

```
$ packer build machine_pupet.json
```

Check it.

```bash
docker run -t -i tcnksm/packer-puppet:0.1 bash
```

### Ansible

Build docker image with ansible provisioning

```
$ packer build machine_pupet.json
```

Check it.

```bash
docker run -i -t tcnksm/packer-ansible:0.1 bash
```

