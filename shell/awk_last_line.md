# Awk: treat last line differently

Cross-platform way of first getting size of input in number of lines, then doing something differently with the last line.
Must be ran with an input file (`awk -f awkfile.awk input.txt`), won't work for stdin.

```
BEGIN { "wc -l < \""ARGV[1]"\"" | getline filesize; filesize += 0
        print "BEGIN;"
        print "INSERT INTO foo (bar, spam)"
        print "VALUES" }
      { if (NR < filesize && NR > 1) {
          print "('" $1 "', " $2 ", '" $3),"
        }
        $last = "('" $1 "', " $2 ", '" $3);"
      } 
END   { print $last
        print "COMMIT;" }
```
