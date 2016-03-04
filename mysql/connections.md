# Show current connections

To find out what clients are connected, and how many connections per client host are open:

```sql
use information_schema;
select substring(HOST, 1, (locate(':', HOST) - 1)) as host, count(host) 
  from PROCESSLIST group by substring(HOST, 1, (locate(':', HOST) - 1));
``
