## Build new container
docker run -i -t centos bash
### do stuff to running container

## Then Commit it so you have a new image
```shell
docker ps -a
docker commit {container} yourname/image-name
```
## Push it up to repo
``` shell
docker login
docker push yourname/newimage
```
