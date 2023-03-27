
# Creating and running container

```sh
docker run --name nginx-local-dev -v $(PWD)/app:/usr/share/nginx/html:ro -v $(PWD)/nginx/conf.d:/etc/nginx/conf.d -p 8080:80 -d nginx
```

# View app in the browser

Visit  [localhost:8080](localhost:8080)

# Enter into container

Get container ID

```sh
docker ps
```

Open interactive shell

```sh
docker exec -it [container-id] /bin/sh
```

## Reload NGINX

```sh
nginx -t && nginx -s reload
```
