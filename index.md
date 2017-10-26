## Welcome to my SQLite Pages

## Install SQLite on Windows
1. Go to SQLite download page, and download precompiled binaries from Windows section.

2. Download sqlite-shell-win32-*.zip and sqlite-dll-win32-*.zip zipped files.

3. Create a folder C:\>sqlite and unzip above two zipped files in this folder, which will give you sqlite3.def, sqlite3.dll and sqlite3.exe files.

4. Add C:\>sqlite in your PATH environment variable and finally go to the command prompt and issue sqlite3 command, which should display the following result.

```
C:\>sqlite3
SQLite version 3.7.15.2 2013-01-09 11:53:05
Enter ".help" for instructions
Enter SQL statements terminated with a ";"
sqlite>
```

## Install SQLite on Linux
Today, almost all the flavours of Linux OS are being shipped with SQLite. So you just issue the following command to check if you already have SQLite installed on your machine.

```
$sqlite3
SQLite version 3.7.15.2 2013-01-09 11:53:05
Enter ".help" for instructions
Enter SQL statements terminated with a ";"
sqlite>
```

If you do not see the above result, then it means you do not have SQLite installed on your Linux machine. Following are the following steps to install SQLite −
1. Go to SQLite download page and download sqlite-autoconf-*.tar.gz from source code section.
2. Run the following command −

```
$tar xvfz sqlite-autoconf-3071502.tar.gz
$cd sqlite-autoconf-3071502$./configure --prefix = /usr/local
$make
$make install
```

The above command will end with SQLite installation on your Linux machine. Which you can verify as explained above.

## Install SQLite on Mac OS X
Though the latest version of Mac OS X comes pre-installed with SQLite but if you do not have installation available then just follow these following steps −
1. Go to SQLite download page, and download sqlite-autoconf-*.tar.gz from source code section.2. Run the following command −
```$tar xvfz sqlite-autoconf-3071502.tar.gz$cd sqlite-autoconf-3071502$./configure --prefix=/usr/local$make$make install```
The above procedure will end with SQLite installation on your Mac OS X machine. Which you can verify by issuing the following command −
```$sqlite3SQLite version 3.7.15.2 2013-01-09 11:53:05Enter ".help" for instructionsEnter SQL statements terminated with a ";"sqlite>```
In SQLite, sqlite3 command is used to create a new SQLite database. You do not need to have any special privilege to create a database.Following is the basic syntax of sqlite3 command to create a database: −`$sqlite3 DatabaseName.db`
Always, database name should be unique within the RDBMS.
Example
If you want to create a new database <testDB.db>, then SQLITE3 statement would be as follows −
```$sqlite3 testDB.dbSQLite version 3.7.15.2 2013-01-09 11:53:05Enter ".help" for instructionsEnter SQL statements terminated with a ";"sqlite>```
The above command will create a file testDB.db in the current directory. This file will be used as database by SQLite engine. If you have noticed while creating database, sqlite3 command will provide a sqlite> prompt after creating a database file successfully.
Once a database is created, you can verify it in the list of databases using the following SQLite .databases  command.
```sqlite>.databasesseq  name             file---  ---------------  ----------------------0    main             /home/sqlite/testDB.db```
You will use SQLite .quit command to come out of the sqlite prompt as follows −
```sqlite>.quit$```
The .dump Command
You can use .dump dot command to export complete database in a text file using the following SQLite command at the command prompt.`$sqlite3 testDB.db .dump > testDB.sql`
The above command will convert the entire contents of testDB.db database into SQLite statements and dump it into ASCII text file testDB.sql. You can perform restoration from the generated testDB.sql in a simple way as follows −`$sqlite3 testDB.db < testDB.sql`
At this moment your database is empty, so you can try above two procedures once you have few tables and data in your database.

