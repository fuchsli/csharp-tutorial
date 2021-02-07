# Database Basics 

SQL database connections begin with "Data Source=".

In this example, we will assume a database is stored in the same directory as the project. 

We need to get the working directory. However, there is no immediate way to get the project's root directory. The following is a workaround: 

    // the Environment class exists in the System namespace
    using System; 

    string workingDirectory = Environment.CurrentDirectory;

The above code will pull the location of the current executable, typically in a bin file. To extract the project directory from this, we need to use the Directory class:

    // Environment uses System
    // Directory uses System.IO
    using System;
    using System.IO;

    string workingDirectory = Environment.CurrentDirectory;
    string projectDirectory = Directory.GetParent(workingDirectory).Parent.Parent.FullName;

To get the path of the database in the project's directory, append the name of the database to the projectDirectory string:

    string dbname = "sample.db";
    string dbpath = projectDirectory + "/" + dbname;

To create the full minimum string for the connection, we need to use the Data Source= prefix:

    string db = "Data Source=" + dbpath;