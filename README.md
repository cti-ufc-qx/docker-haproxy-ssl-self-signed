# Forked Docker Official Image packaging for HAProxy

The Original Docker Image [here] (https://hub.docker.com/r/library/haproxy/)

This image add the support SSL via package 'openssl' and 'ssl-cert'. Besides, create a combined PEM SSL Certificate/Key File.

More informations: [Tutorial external] (https://www.digitalocean.com/community/tutorials/how-to-implement-ssl-termination-with-haproxy-on-ubuntu-14-04)

# How to use this image

All configurations there is in the file haproxy.cfg

You need to do bind mount on volume usr/local/etc/haproxy/haproxy.cfg

# Docker run

$ docker run -d --name my-haproxy -p 80:80 -p 443:443 -v /path/to/haproxy.cfg:/usr/local/etc/haproxy/haproxy.cfg:ro cti-ufc-qx/docker-haproxy-ssl-self-signed:1.6


