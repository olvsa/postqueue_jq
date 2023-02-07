# postqueue_jq
prints to prometheus's textfile status of the Postfix queue (for multiple Postfix instances):

postqueue_jq.prom example:

# HELP postqueue_jq metric
# TYPE postqueue_jq gauge
postqueue_jq{cfg="postfix-mx",queue="deferred",sender="MAILER-DAEMON"} 3

where 'cfg' is Postfix instance
