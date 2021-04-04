# nginx-docker

**eggspot/nginx:1.19.9-rtmp**: pre-install Nginx RTMP module + NodeJs
```yaml
FROM eggspot/nginx:1.19.9-rtmp
# Set up config file
COPY nginx.conf /etc/nginx/nginx.conf
```