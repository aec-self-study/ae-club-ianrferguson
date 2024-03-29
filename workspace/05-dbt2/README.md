# dbt 201 - Tests, Docs, Sources

* Tets are assertions made about the data in your model
	** "This column is unique" ... if true, it passes the test

* Built-in dbt tests
	** unique
	** not null
	** accepted_values
	** relationships

* dbt generates target and logs directories
	** target/compiled contains run-able select statements (including tests)
	** target/run contains the executable SQL dbt uses to build your models
	** logs/dbt.log contains all the queries that dbt runs + additional logging
		- Recent errors will be at the bottom here

* dbt has native documentation tools to generate rich docs

* dbt docs generate
	** Creates a bunch of .json files in target/

* dbt docs server
	** Launches localhost with rendered docs

```sql
-- Adding sources tells dbt about the tables in your warehouse
-- Links dependencies between models and their relevant sources
select * from {{ source('coffee_shop', 'orders') }} as orders;
```