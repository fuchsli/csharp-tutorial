# SQLite 

## Connecting to SQLite

Connecting to a database first requires a means of making a connection. One option for this is the System.Data.SQLite namespace. 

    // necessary for using SQLite
    using System.Data.SQLite

    // create a new connection to the sqlite database
    using SQLiteConnection conn = new SQLiteConnection("path/to/database.db");
    
