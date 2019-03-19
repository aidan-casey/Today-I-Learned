# Find Database Files

To easily find the location of database files, run the following query against the SQL server.

```sql
USE master;
SELECT 
  name 'Logical Name', 
  physical_name 'File Location'
FROM sys.master_files;
```

The result will be a list of databases and their corresponding file location.

[Found on Database.Guide](https://database.guide/how-to-find-the-location-of-data-files-and-log-files-in-sql-server/)