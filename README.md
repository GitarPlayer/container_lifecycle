# container_lifecycle
```bash
podman pull httpd
podman images
podman save -o ID httpd.tar
podman load -i httpd.tar
podman images
podman create --name created httpd
podman run -d --name -p $PORT:80 httpd-container httpd
curl localhost:$PORT
podman exec httpd-container sed -i 's/works/works v2/g' $INDEX
curl localhost:$PORT
pkill httpd && curl localhost:$PORT
podman rm httpd-container
podman stop httpd-container
podman rm httpd-container
```
