# Command Cheat Sheet 

## Sample Vagrant file and related commands
```bash
vagrant up  
##### Note - In case any port conflict comes on vagrant up on your laptop, update the host port with any of the available port.
vagrant ssh
``` 

## updates related to base box and python dependencies
```bash
sudo apt-get update
sudo apt-get install python-software-properties -y
```
## docker installation
```bash
wget -qO- https://get.docker.com/gpg | sudo apt-key add -
wget -qO- https://get.docker.com/ | sh
```
## enable docker without sudo 
```bash
sudo groupadd docker
sudo gpasswd -a ${USER} docker
sudo service docker restart
```
## docker compose-installation
```bash
sudo wget https://github.com/docker/compose/releases/download/1.1.0/docker-compose-Linux-x86_64 -O /usr/bin/docker-compose
sudo chmod +x /usr/bin/docker-compose
```
## configuration related updates
```bash
vi /etc/default/docker and Add DOCKER_OPTS with the details specific to your private docker registry

DOCKER_OPTS="$DOCKER_OPTS --dns 8.8.8.8  --dns 8.8.4.4 --insecure-registry 10.145.10.169:5000 --insecure-registry ctocacheserver.wipro.com:8000"

once you have updated the above file restart docker service

sudo service docker restart
```


