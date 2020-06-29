# Jitsi Videobridge Zabbix Stats
An simple implementation of Jitsi Videobridge Statistics, to Zabbix. 

Jitsi Videobridge Stats. Based on Colibri stats bulit-in api to present Staticis from Jitsi Videobridge. I've added the most important data, some stats not added, but it is easy to add them by using the Zabbix Server GUI. 

If you don't enabled Videobridge statistics, see Jitsi documenation below.

### Full Documentation of Jitsi Videobridge Colibri Stats

`https://github.com/jitsi/jitsi-videobridge/blob/master/doc/statistics.md`
`https://github.com/jitsi/jitsi-videobridge/blob/master/doc/rest.md`


The only thing what must you do is from Zabbix site is:

Add the XML template to throughout Zabbix GUI.

### Macro for servername

The template contains the macro JITSISERVER. This allows to override the default of localhost (127.0.0.1) in
order to monitor a jitsi instance on another host from a zabbix agent.

###  UserParameter File

1. Add the xml template to throughout Zabbix GUI.&#13;
2. Add in following zabbix UserParameters on videobridge machine with installed zabbix-agent

```
UserParameter=jvb.stats[*],curl -s curl -s http://localhost:8080/colibri/stats | jq '.'
```
