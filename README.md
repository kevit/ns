export DOCKER_URL=tcp://188.42.224.135:4243 
rake pack
rake run


#Docker daemon logs
http://188.42.224.135/docker.txt

#Docker container logs
##forming by * * * * * docker logs $(docker ps -a -q) > /usr/share/nginx/html/container.txt
http://188.42.224.135/container.txt
