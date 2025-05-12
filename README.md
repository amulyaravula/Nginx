STEPS:
1) Installing docker:
   curl -sSL https://get.docker.com/ | sh
   sudo service docker start
2) Adding user to the docker group
   sudo usermod -aG docker $(id -un).
3) Logout and logback to reflect the changes
4) Pull docker image
   docker pull nginx
5) list images
   docker images
6)Run the container
  docker run -d -p 90:80 nginx
  -d - runs the container in the background
  -p - port mapping
7) list the docker containers
   docker ps
8) Allowed 90 port for bastion-host
9)Verify whether the nginx is running or not
   curl http:34.93.82.177:90   
