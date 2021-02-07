# C# Tutorial Basics 

## Lists 

Name: List  
Namespace: System.Collections.Generic 

In C#, arrays are immutable - that is to say they cannot be changed once they are created. Therefore, they are not practical in instances where we would want arrays in other languages. C#'s answer to this is the List class.

A List can be created through the following:

    List varname = new List<type>;

where *type* is the type the list is composed of, like *int* or *string*. 

## Key-Value Pair

Name: KeyValuePair  
Namespace: System.Collections.Generic 

To create a key-value pair, C# uses the KeyValuePair class.

    KeyValuePair<type,type> varname = new KeyValuePair<type,type>(value,value); 
    KeyValuePair<string,string> varname = new KeyValuePair<"Food", "Apple");

### A Group of Key-Value Pairs

To create a group of key-value pairs, C# uses a List of KeyValuePair objects. 

    List<KeyValuePair<type,type>> varname = new List<KeyValuePair<type,type>>();
    List<KeyValuePair<string,string> varname = new List<KeyValuePair<string,string>>;

To append values: 

    varname.Add(new KeyValuePair<string,string> ("Food", "Apple"));
