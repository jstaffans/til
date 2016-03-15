# chef-runner, the fastest way to run Chef recipes

Use [chef-runner](https://github.com/mlafeldt/chef-runner) for rapidly running 
Chef recipes on VMs (Docker) or remote hosts. Can also [automatically install a Chef client](https://github.com/mlafeldt/chef-runner/wiki/Installing-Chef) on the host.

With Docker:

```
chef-runner --ssh Port=2200 -H root@$(docker-machine ip docker-vm) mycookbook
```
