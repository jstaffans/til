# Use watch to continuously run command 

The 'watch' utility is useful for e.g. monitoring the last started process 
matching some name pattern:

```
$> watch 'ps -p $(pgrep -o -f "node server") -o "pid command pcpu pmem"'
``` 

As seen [here](http://blog.yld.io/2016/02/08/squeeze-the-juice-out-of-node/)
