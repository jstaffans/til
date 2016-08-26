# Use lsof to see open files, network activity

E.g. get location of log file created by a process:

```
lsof | grep <pid> | grep log
```

See TCP activity of user, 1s refresh:

```
lsof -r 1 -u john -i -a
```

Reference: http://www.catonmat.net/blog/unix-utilities-lsof/


