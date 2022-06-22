# mac_docker
Docker for MAC
Follow the below step
`brew install vagrant`
`mkdir -p ~/vagrant-machines/docker-daemon`
`cd ~/vagrant-machines/docker-daemon`
`vagrant box add {{../docker-daemon/docker-package.box}} --name {{docker-daemon}}`
`cp ~/Downloads/vagrant ./`
`vagrant up`

``vagrant box add docker-daemon docker-package.box``
export DOCKER_HOST=tcp://127.0.0.1:2375
`vagrant ssh
 
---- Now that you are sshed into your vm, lets set that up
sudo su - root
apt update
apt install -y docker.io
mkdir /etc/systemd/system/docker.service.d
printf "[Service]\nExecStart=\nExecStart=/usr/bin/dockerd -H unix:// -H tcp://0.0.0.0:2375\n" > /etc/systemd/system/docker.service.d/options.conf
cd /vagrant
cp *.crt /usr/local/share/ca-certificates/
update-ca-certificates
systemctl daemon-reload
systemctl restart docker
exit
exit
vagrant halt`
