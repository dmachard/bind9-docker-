# ISC Bind9 DNS Server Docker Image

This *[bind9](https://gitlab.isc.org/isc-projects/) Docker Image* is based on **Alpine**.

## Supported tags and respective `Dockerfile` links

- [`9.18.19`, `latest` (*9.18.19/Dockerfile*)](https://github.com/dmachard/docker-bind9/tree/master/9.18.19)

## How to use this image

The default configuration is with recursor mode.
Run bind9 with the following command:

```bash
sudo docker run --name=bind -d -p 53:53/udp -p 53:53/tcp dmachard/bind9:latest
```

## Custom configuration

You can run this image and provide your own bind configuration like that:

```bash
sudo docker run --name=bind -d -p 5354:53/udp -p 5354:53/tcp -v $PWD/named.conf:/etc/bind/named.conf dmachard/bind9:latest
```