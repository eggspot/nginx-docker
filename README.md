# nginx-docker

**eggspot/nginx:1.19.9-rtmp**: pre-install Nginx RTMP module + Stunnel4 (restream to RTMPs) + NodeJs

**eggspot/nginx:1.19.9-rtmp-arm**: ARM supported, pre-install Nginx RTMP module + Stunnel4 (restream to RTMPs) + NodeJs

- OBS connect to `rtmp://localhost/live`

```yaml
FROM eggspot/nginx:1.19.9-rtmp

# nginx.conf  file
COPY nginx.conf /etc/nginx/nginx.conf
```

## Use Stunnel with ENTRYPOINT in docker 
Example
```bash
#!/bin/sh
  
# turn on bash's job control
set -e

/etc/init.d/stunnel4 start &
# Start nginx
nginx -g "daemon off;"
```

```yaml
# stunnel default config (enable/disable)
COPY stunnel4 /etc/default/stunnel4
# stunnel.conf file
COPY stunnel.conf /etc/stunnel/stunnel.conf
```

