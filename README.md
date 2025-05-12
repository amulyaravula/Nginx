STEPS:
- Installing docker:
   curl -sSL https://get.docker.com/ | sh

    sudo service docker start
- Adding user to the docker group
  
   sudo usermod -aG docker $(id -un)
-  Logout and logback to reflect the changes
-  Pull docker image
  
   docker pull nginx
   
- list images

   docker images
   
- Run the container
  docker run -d -p 90:80 nginx
  
  -d - runs the container in the background
  
  -p - port mapping
- list the docker containers
 
   docker ps
- Allowed 90 port for bastion-host
- Verify whether the nginx is running or not

   curl http:34.93.82.177:90   
![Screenshot from 2025-05-12 11-05-41](https://github.com/user-attachments/assets/68ca73f5-dfe0-483e-bc40-0a8699eb834e)
