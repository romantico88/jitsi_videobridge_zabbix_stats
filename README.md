# Jitsi Videobridge Zabbix Stats
An simple implementation of Jitsi Videobridge Statistics, to Zabbix. 

Jitsi Videobridge Stats. Based on Colibri stats bulit-in api to present Staticis from Jitsi Videobridge. I've added the most important data, some stats not added, but it is easy to add them by using the Zabbix Server GUI. 

If you don't enabled Videobridge statistics, see Jitsi documenation below.

### Full Documentation of Jitsi Videobridge Colibri Stats

`https://github.com/jitsi/jitsi-videobridge/blob/master/doc/statistics.md`
`https://github.com/jitsi/jitsi-videobridge/blob/master/doc/rest.md`


The only thing what must you do is from Zabbix site is:

Add the XML template to throughout Zabbix GUI.

### MacroS

The template contains the macros: 

`{$JITSI_COLIBRI_HOST}` - An IP/FQDN of Jitsi Videobridge. Default: `localhost` (in most cases there is no needed to change this value)


`{$JITSI_MEET_HOST}` - FQDN or IP of Prosody XMPP Server. Default: `meet.jitsi` (you must change this valute, mandatory)

### Versions:

Tested and implemated on Zabbix 4.2.6.

Several people reported to me a problem with importing to 3><4.0 versions of zabbix. I can't reproduce the problem right know - you can try import an old version of this template (depending on UserParamFile, 1.0 Release), or if you have a time, find a sulution and create push request/give me a message.

If newest version of this template will not run on older zabbix's verisons , please switch to 1.0/old branch to download UserParameter version.


### To Do:

* SDK callstats.io lib integration
