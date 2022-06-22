# mac_docker
Docker for MAC
Follow the below step
`brew install vagrant`
`mkdir -p ~/vagrant-machines/docker-daemon`
`cd ~/vagrant-machines/docker-daemon`
`vagrant box add {{../docker-daemon/docker-package.box}} --name {{docker-daemon}}`
`cp ~/Downloads/vagrant ./`
`vagrant up`
