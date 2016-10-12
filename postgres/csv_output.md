# CSV output

I frequently build a complex SQL query which I would then like to have exported to CSV. 
`\copy` is one option, but it does not work well with piping input to `psql`.
Another way is:

```sh
psql -h localhost --port=5432 --username=... --password ... -F , --no-align  < query.sql | ghead -n -1 > query.csv
```

