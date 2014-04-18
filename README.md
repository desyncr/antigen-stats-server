antigen-stats-server
====================

A server to aggragate stats for antigen

Install
=======
1. clone the repsitory
2. run `npm install`

Usage
=====
Start the server `./start_statd`

Send stats to the server: `echo "plugin.simon:+1|g" | nc -u -w0 127.0.0.1 8125`

View the stats: 

```
$ telnet 127.0.0.1 8125
Trying 127.0.0.1...
Connected to localhost.
Escape character is '^]'.
gauges
{ 'plugin.simon': 2, 'statsd.timestamp_lag': 0 }
END

gauges
{ 'plugin.simon': 2, 'statsd.timestamp_lag': 0, 'plugin.bbb': 1 }
END

help
Commands: stats, counters, timers, gauges, delcounters, deltimers, delgauges, health, quit
```
