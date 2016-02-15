elasticsearch-munin
===================

ElasticSearch munin plugins (from https://gist.github.com/2159398), for elasticsearch 1.2.1 or higher.

Change in this fork
-------------------

* Use sudo to list file in /proc/<PID>/fd/
* Export elasticsearch host and port with munin env 

File /etc/munin/plugin-conf.d/elasticsearch

    [elasticsearch*]
    env.host localhost
    env.port 9200

File /etc/sudoers.d/munin

    User_Alias MUNINUSER = munin,nobody
    Defaults:MUNINUSER !requiretty
    MUNINUSER    ALL=(ALL)     NOPASSWD:/bin/ls /proc/*/fd/*

