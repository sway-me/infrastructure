# Deployment Docs

![](deployment.svg)

## Prereqs

### Configure NFS

1. turn on `sudo systemctl enable systemd-networkd-wait-online.service`
2. disable ipv6

### Configure Mariadb
1. After installation and setting up admin user change bind address:

```python
# sudo vim mariadb.conf.d/50-server.cnf
bind-address	= 0.0.0.0:
```


### Manifesto
- prefer docker commands over config files