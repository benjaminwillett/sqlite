### import CSV into database

Download the data-set as CSV and dump it into the sqlite database.

```
$ sqlite3 salaries.db
sqlite> .mode csv salaries
sqlite> .import employee_chicago.csv salaries
```

and imported CSV.

