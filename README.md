# postqueue_jq
prints to prometheus's textfile status of the Postfix queue (for multiple Postfix instances):

##### postqueue_jq.prom ('cfg' is Postfix instance)
```
# HELP postqueue_jq metric
# TYPE postqueue_jq gauge
postqueue_jq{cfg="postfix-mx",queue="deferred",sender="MAILER-DAEMON"} 3
```

##### crontab example query
```
#Ansible: postqueue_jq
*/5 * * * * sleep `jot -r 1 1 17`; /bin/sh /srv/textfiles/postqueue_jq >/dev/null
```
