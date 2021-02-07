# JSON 

A lot of information is transferred in JavaScript Object Notation, or JSON as it is more commonly known. Being a primary response from API calls, having the ability to manipulate JSON data is critical regardless of programming language. 

One way of handling JSON in C# is with the System.Text.Json namespace. 

## Deserialization

JSON data needs to be deserialized to be used in C#. Deserialization is the process of converting JSON data into C# objects. 

To do this requires knowledge of what information is coming in the JSON format. Classes must be made representing the data structure. For example, in the simple JSON below, all that is held is a status:

    {
        "status": "ok"
    }
    
To hold the information in C#, we need a class that replicates this structure: 

    class StatusInfo
    {
        public string status { get; set; }
    }

To convert the JSON information to the class, we can create an object to hold it: 

    string jsonString = '{ "status": "ok" }';

    StatusInfo info = JsonSerializer.Deserialize<StatusInfo>(jsonString);

From the above, we would be able to access the value of *status* with the following syntax:

    info.status

