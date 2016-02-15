elasticsearch-munin
===================

ElasticSearch munin plugins (from https://gist.github.com/2159398), for elasticsearch 1.2.1 or higher.

Change in this fork
-------------------

* Export elasticsearch host and port with munin env 

File /etc/munin/plugin-conf.d/elasticsearch

    [elasticsearch*]
    env.host localhost
    env.port 9200