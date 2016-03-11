# Statement cache pitfalls

A statement cache improves performance especially of complicated queries, because
it allows the database to re-use previously planned and optimized statements.

Beware though of queries like `SELECT *` in combination with schema migrations.
A cached statement will become invalid, because the result type changes. 

Another reason to not share DB schemas - migrations done for another application
can pull the rug out of another application by breaking its statement cache.
