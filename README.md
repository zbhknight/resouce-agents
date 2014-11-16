These scripts are OCF resource agents that are not included in the pacemaker package.

Create a folder /var/lib/ocf/resource.d/custom, and put them into it.

Notice: make sure that these scripts are executable

###Simple Examples###

####Haproxy####
```
crm configure primitive haproxy ocf:custom:haproxy params conffile=/etc/haproxy/haproxy.cfg pidfile=/var/run/haproxy.pid op monitor interval=20s
```
