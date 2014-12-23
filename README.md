sql-stuff
=========
* Restore database
```
USE master;
GO
RESTORE DATABASE dbname
  FROM DISK = 'c:\backup path\backup.bak'
  WITH REPLACE, RECOVERY,
    MOVE 'data_file_name' TO 'D:\data file path\dbname.mdf',
    MOVE 'log_file_name'  TO 'L:\log file path\dbname.ldf';
```
