# web-monitroring-elk
 This is containerised way to do monitoring of web application using ELK.
 This does monitoring of web application using ELK, all running in containers.
 
 Build containers for elk and web application using command `docker-compose up` . Images being used are : `sebp\elk` and `nginx-filebeat`
 
 This will bring ELK listening at ports: 5601, 9200, 5044 and Nginx at 8080
 
 Logs being monitored by ELK on Nginx are : 
 `/var/log/niginx/*.log`
 `/var/log/syslog`
 `/var/log/auth.log`

ou might see follwing error while bringin ELK up:
 `max virtual memory areas has low memory`
 
 This can be fixed by, if using ubuntu:
 `sudo sysctl -w vm/max_map_count=262144`
 
 Tools I would use for conatiner deployment :
- Terraform ( To automate Infrastructure creation )
- AWS ECS  ( Container management srevice by AWS )
- Jenkins ( Test image and deploy on ECS )
- Docker Hub / AWS ECR ( As container Registery )
