###  Docker version command
`docker --version`

### Docker Login
`docker login -u USER_NAME  DOCKER_REPO_URL -p PASSWORD`

### Docker tag image
`docker tag image_name:ver tag_name:ver`

## Docker pull image
`docker pull imageurl`

###  Build Docker image
` docker build -t my_image  .`

### list out docker images
`docker images`

### Run docker image
`docker run  -d -p 8080:8080 my_image`

### List out docker running processes
`docker ps`

### Enter into docker file system
`docker exec -t -i CONTAINER_ID  bash`

### How to stop docker process
`docker stop CONTAINER_ID `

### Copy file from docker filesystem to host file system
`docker cp <containerId>:/file/path/within/container /host/path/target`

### Delete docker image
`docker rmi -f  image_id`

### View docker logs
`docker logs processid`

### Pass env varible to docker container
`docker run -e var_name1="xxx" -e var_name2="35" -t my_image:2.0.0`

### Mount a host system folder
`docker run  -v D:/myHostFolder/apps:/dockerFolder/log -t my-image-2:0.0`

### Copy logs from docker container to host file system
`docker logs continerid >logs.log`


### List out docker process id
`docker ps -aq`

### Stop all Processes
`docker stop $(docker ps -aq)`

### Remove all processes
`docker rm $(docker ps -aq)`	

### Removing all images
`docker rmi $(docker images -q)`

### See the memory usage and cpu usage 
`docker stats`

### Limit resouces on docker container
`docker run -d  --cpus="1.0"  --memory="100m"  -t my-image-2:0.0`

### To Send logs to log stash
`docker run --log-driver=syslog --log-opt syslog-address=tcp://<logstash-system-ip(use ip not localhost)>:5000 my-image:2.0.0`
