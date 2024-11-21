Category: [[Help]]
Tags: #help #docker #containers #podman 

# How do I execute a command in docker?

```bash
docker exec -it <container-name-or-id> sh -c "echo a && echo b"
```

# How do I get a shell in docker?

```bash
# Running container
docker exec -it <container-name-or-id> bash

# New container
docker run --rm -it --entrypoint bash <image-name-or-id>
```

# How do I remove all images?
https://stackoverflow.com/questions/44785585/how-can-i-delete-all-local-docker-images
To delete all containers including its volumes use,

```bash
docker rm -vf $(docker ps -aq)
```

To delete all the images,

```bash
docker rmi -f $(docker images -aq)
```

Use this to **delete everything**:

```bash
docker system prune -a --volumes
```

# Minimal Dockerfile for Nginx

```Dockerfile
FROM nginx:alpine

COPY public /usr/nginx/html
```