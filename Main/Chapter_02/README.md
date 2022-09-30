# Chapter 02 - Creating linux and docker lab


### Docker lab creation and its installation:
Use centos installation tutorials on the internet in order to install it.  
Then:  
1. Switch to root user:
```shell
$ sudo su
```
2. Install *net-tools* package that contains basic networking tools, including *ifconfig* and ...
using command below:
```shell
yum install net-tools 
```
3. change hostname to *master* in order to distinguish from other nodes:
```shell
hostnamectl set-hostname master
```
4. Install *yum-utils* package which is a collection of tools and programs for managing yum 
repositories, installing debug packages, source packages, etc:
```shell
yum install yum-utils
```
5. Add docker repository to the list of repositories:
```shell
yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
```
6. Install docker tools collection:
```shell
yum install docker-ce docker-ce-cli containerd.io docker-compose-plugin
```
7. Check docker service status:
```shell
systemctl status docker
```
8. Start docker service:
```shell
systemctl start docker
```
9. Enable docker service to start running automatically on startup:
```shell
systemctl enable docker
```
10. Run docker *hello-world* container in order to make sure that you installed docker successfully:
```shell
docker container run hello-world
```

**Note:** Don't forget to take a snapshot of existing docker lab; we will use it in further chapters.
