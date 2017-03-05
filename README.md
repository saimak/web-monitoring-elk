# web-monitroring-elk
This does monitoring of web application using ELK, all running in containers.

Build containers for elk and web application using command `docker-compose up` . Images being used are : `sebp\elk` and `nginx-filebeat`

This will bring ELK listening at ports: 5601, 9200, 5044 and Nginx at 8080

Logs being monitored by ELK on Nginx are : 
`/var/log/niginx/*.log`
`/var/log/syslog`
`/var/log/auth.log`
