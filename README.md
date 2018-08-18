# Awesome Mssql Cheatsheet
MS SQL cheat-sheet.

## SQL Auto increment field
```
CREATE TABLE Demo (
    ID int IDENTITY(1,1) PRIMARY KEY,
    user varchar(255),
);
```
The MS SQL Server uses the IDENTITY keyword to perform an auto-increment feature.  
The starting value for IDENTITY is 1, and it will increment by 1 for each new record. 
> Tip: To specify that the above column "ID" should start at value x and increment by y, change keyword to : IDENTITY(x,y).
