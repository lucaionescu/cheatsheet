### container

```bash
# Show container metadata in JSON format
docker container inspect CONTAINER_ID

# Show live container resource usage statistics
docker container stats

# Remove all stopped containers
docker rm $(docker ps -a -q)

# Start a container in interactive mode and remove it after exiting
docker run -it --rm IMAGE bash

# Access a running container
docker exec -it CONTAINER_ID SHELL_COMMAD
```

### image

```bash
# Remove all unused images
docker image prune --all

# Show detailed information about an image
docker image inspect IMAGE

# Remove images with a specific name
docker rmi $(docker images | grep NAME)
```
