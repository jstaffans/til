# docker stop may not work

There's a quirk with launching a process inside a Docker container: trying to stop it
may not lead to expected results. `SIGTERM` may have no effect. Adding a lightweight
init handler in front of the process helps.

Reference: http://engineeringblog.yelp.com/2016/01/dumb-init-an-init-for-docker.html

