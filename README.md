# Forked Docker Official Image packaging for HAProxy

The Original Docker Image [here] (https://hub.docker.com/r/library/haproxy/)

This image add the support SSL via package 'openssl' and 'ssl-cert'. Besides, create a combined PEM SSL Certificate/Key File.

# How to use this image

All configurations there is in the file haproxy.cfg

You need to do bind mount on volume usr/local/etc/haproxy/haproxy.cfg

# Docker run

$ docker run -d --name my-haproxy -v /path/to/haproxy.cfg:/usr/local/etc/haproxy/haproxy.cfg:ro haproxy:1.6


