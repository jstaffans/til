# Select regexp

You can select whether or not a value matches a regular expression.
This can be useful for e.g. data migrations (some text field content
should now be represented as dedicated columns).

```sql
select p.id, c.content regexp '.*#cover([^12]|$)' as cover0, c.content regexp '.*#cover[1]' as cover1;
``
