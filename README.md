# unifi-docker-compose-template
All (example) files for a runnning a unifi network application in Docker.


## What is this?
This is my docker-compose files for runnning a unifi network appliance with docker. Based on [Linuxservers](https://github.com/linuxserver/docker-unifi-network-application) container

## How to use:
0. Install docker and docker-compose (depending on your distro)
1. Put the db_password.txt, the docker-compose.yml and the init-mongo.js files in a new directory in the home folder of your docker host user
2. Change the password for the database in db_password.txt and init-mongo.js to your desired password
3. create the network with "docker network create net-unifi-external"
4. run the container with "docker-compose up -d"
5. Update the container with "docker-compose pull" and "docker-compose up -d"

## Notes:
- check out the [Linuxserver](https://github.com/linuxserver/docker-unifi-network-application) Container. The Github page explains most of the settings in detail.
- this repository is mostly for my own documentation. I like it to have docker-compose files which run without changing much or anything. since most container developer use very simple examples for their docker-compose examples
- the external network is only optional. It could be used with a reverse proxy for the WEBGUI. I don't want to expose the backend DB Container to other Containers, like a reverse proxy
- i tried to make this as secure as possible. But Feedback is realy appreciated. I am only beginning using docker.
- **This conatiner can be used for home usage with a good feel of safety. If you want to use it in a prod. enviroment, maybe check for missing best practices and security errors.**
