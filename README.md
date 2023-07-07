# kakoghost/WEBMIN-SQUID

## To Create image:

```bash
docker build -t kakoghost/WEBMIN-SQUID .
```

## To run this image, you need create folder's:

- /volume/squid
- /volume/webmin
- /volume/sarg

```bash
docker run -it --name squidProxy --hostname proxy \
--volume /volume/squid/:/etc/squid \
--volume /var/spool/squid/:/var/spool/squid \
--volume /var/log/squid/:/var/log/squid \
--volume /volume/webmin/:/etc/webmin \
--volume /volume/sarg/:/etc/sarg \
kakoghost/WEBMIN-SQUID /bin/bash
```

