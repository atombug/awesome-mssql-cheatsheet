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

## Establish SQL Connection:
```
using (SqlConnection connection = new SqlConnection(connectionString))  
    {  
        connection.Open();  
        // Fire Queries Here, connection closed on following line.  
    }  
```
Above code is example to establish Connection with database in c#.
> To ensure that connections are always closed, open the connection inside of a using block, as shown in the above code fragment. Doing so ensures that the connection is automatically closed when the code exits the block. - [MSDN](https://docs.microsoft.com/en-us/dotnet/api/system.data.sqlclient.sqlconnection?view=netframework-4.7.2)
