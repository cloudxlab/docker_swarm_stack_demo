# docker_multi_apps_single_compose

#build the image

docker-compose -f docker-compose.yml build

#list the images

docker-compose images

docker image ls

#run the containers for the images of this docker compose file, in detached mode

#this also builds the images if not present already

docker-compose -f docker-compose.yml up -d

#list the comtainers

docker container ls -a

docker-compose ps

#rebuild the images if compose file has changed, and run the containers

docker-compose -f docker-compose.yml up --build -d

#check the docker logs

docker logs eaefbe528ab0

#display running services

docker-compose ps --services

#dispplay running processes

docker-compose top
docker-compose top web

#run the curl to verify that app is working

curl http://localhost:5001
