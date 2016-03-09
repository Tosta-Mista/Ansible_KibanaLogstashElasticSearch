Kibana Logstash ElasticSearch Ansible install Script
===================
[Kibana](https://www.elastic.co/products/elasticsearch) is a static frontend to
elasticsearch which allows you to monitor your data in realtime.

Requirements
------------
 - Debian 8 Jessie

Role Variables
--------------
### Set the user ansible will log in with
    user: root

### Set the domain name kibana will resolve to - this is for the nginx configuration
    kibana_domain: localhost

### Set the location of the elastic search database
    es_address: http://<your_server_ip>

Dependencies
------------
 - Nginx installed and runnning
 - Elasticsearch installed and running

Setup
-----
Generate a htpasswd file (You can use an online tool if you don't have apache
installed - [Htpasswd Generator](http://www.htpasswdgenerator.net/)) and
put it in `roles/kibana/files/htpasswd`.
