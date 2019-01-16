# et-cetera
Important configuration files needed to set up servers that are symlinked into /etc

the following are our current symlinks:

On nyc1:
```
ln -s /et-cetera/haproxy/haproxy.cfg /etc/haproxy/haproxy.cfg
ln -s /et-cetera/apache2/nyc1-ports.conf /etc/apache2/ports.conf
ln -s /et-cetera/apache2/sites-available/nyc1.conf /etc/apache2/sites-available/environmentaldashboard.org.conf
```

On any worker node:
```
ln -s /et-cetera/apache2/node-ports.conf /etc/apache2/ports.conf
ln -s /et-cetera/apache2/sites-available/node.conf /etc/apache2/sites-available/environmentaldashboard.org.conf
```