# Skip lines with awk

When processing e.g. database dumps with awk, it is often handy to skip
a few of the first lines which may contain column headers.

```
NR > 2 { print ... }
```
