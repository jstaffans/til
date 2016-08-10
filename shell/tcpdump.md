# Watch incoming traffic with tcpdump

If you really want to know what clients are sending to your server, use tcpdump.

```
tcpdump -s 0 -i eth0 -A 'port 80' > dump.log
```


