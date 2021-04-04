# nginx-docker

**eggspot/nginx:1.19.9-rtmp**: pre-install Nginx RTMP module + Stunnel4 (restream to RTMPs) + NodeJs
- OBS connect to `rtmp://localhost/live`

```yaml
FROM eggspot/nginx:1.19.9-rtmp

# nginx.conf  file
COPY nginx.conf /etc/nginx/nginx.conf

# stunnel.conf file
COPY stunnel.conf /etc/stunnel/stunnel.conf

```