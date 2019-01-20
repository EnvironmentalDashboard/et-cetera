# et-cetera
Important configuration files needed to set up servers that are symlinked into /etc

the following are our current symlinks:

On nyc1 (running HAProxy and Apache):
```
ln -s /et-cetera/haproxy/haproxy.cfg /etc/haproxy/haproxy.cfg
ln -s /et-cetera/apache2/nyc1-ports.conf /etc/apache2/ports.conf
ln -s /et-cetera/apache2/sites-available/nyc1.conf /etc/apache2/sites-available/environmentaldashboard.org.conf
ln -s /et-cetera/letsencrypt/cli.ini /etc/letsencrypt/cli.ini
```

On any worker node (running Apache):
```
ln -s /et-cetera/apache2/node-ports.conf /etc/apache2/ports.conf
ln -s /et-cetera/apache2/sites-available/node.conf /etc/apache2/sites-available/environmentaldashboard.org.conf
ln -s /et-cetera/letsencrypt/cli.ini /etc/letsencrypt/cli.ini
```

Apache needs the following modules enabled:
```
a2enmod access_compat alias auth_basic authn_core authn_file authz_core authz_host authz_user autoindex deflate dir env filter headers mime mpm_prefork negotiation php7.2 proxy_http proxy reqtimeout rewrite setenvif socache_shmcb ssl status
```
