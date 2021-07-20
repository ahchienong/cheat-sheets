
## Drop All Tables from Schema

``` sql
-- generate drop tables sql scripts
SET @DATABASE_SCHEMA = "SCHEMA_NAME"; -- <- update this to your interested schema to drop

SELECT concat('DROP TABLE IF EXISTS `', table_name, '`;')
FROM information_schema.tables
WHERE table_schema = @DATABASE_SCHEMA;
```

``` sql
-- scripts to drop all tables for the schema selected
SET FOREIGN_KEY_CHECKS = 0;
-- 
-- <output from above goes here>
SET FOREIGN_KEY_CHECKS = 1;
```
