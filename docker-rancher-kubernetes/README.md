# Docker, Rancher, Kubernetes... Minecraft? (Setup and Install Tutorial)

If you want to set up Kubernetes at home using Rancher to run Docker containers, this is the guide for you. This is a step by step tutorial of how to install and configure Rancher, Docker, and Kubernetes for your homelab.  In this video we set up and configure a Minecraft server in just a matter of minutes with some enterprise like features.  You can use this same process to spin up other Docker containers at home on your server or desktop.

https://www.youtube.com/watch?v=oILc0ywDVTk


You'll want to use a command similar to this so that there aren't any port conflicts with other services or kubernetes itself.
Also, you may want to consider pinning your docker tag to a version other than `latest` to make backing up and upgrading easier.

`docker run -d --restart=unless-stopped -p 9090:80 -p 9091:443 -v /opt/rancher:/var/lib/rancher --name=rancher_docker_server rancher/rancher:latest`