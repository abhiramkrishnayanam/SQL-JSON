# SQL-JSON

JSON (JavaScript Object Notation) is a lightweight, text-based format for representing structured data. It is easy for humans to read and write and for machines to parse and generate.
JSON is widely used for data exchange between web servers and applications, as well as for configuration files and APIs.<br>

## Key Features of JSON
Lightweight and Text-Based: Easily readable by humans and processed by machines.<br>
Language-Independent: Derived from JavaScript but can be used with many programming languages.<br>
Hierarchical Structure: Supports nested objects and arrays, making it flexible for complex data.<br>
Self-Describing: The structure is self-explanatory, allowing easy understanding of the data format.<br>
## JSON Syntax
JSON represents data as key-value pairs enclosed in curly braces {}. It can contain:<br>

* Objects: Represented by {} and consist of key-value pairs.
* Arrays: Represented by [] and contain a list of values.
* Values: Can be strings, numbers, booleans, null, arrays, or objects.

### Example JSON
Simple JSON Object:<br>

```{
    "name": "John Doe",
    "age": 30,
    "isEmployed": true
}
```<br>

JSON with Nested Objects and Arrays:

```{
    "name": "Jane Doe",
    "age": 25,
    "skills": ["Python", "SQL", "Data Analysis"],
    "address": {
        "city": "New York",
        "zip": "10001"
    }
}
```

## Common Use Cases
* Web APIs: Sending and receiving data between client and server.
* Configuration Files: Storing settings for applications.
* Data Storage: Saving lightweight, semi-structured data.
* Log Files: Storing event logs in a structured format.

## Advantages of JSON
* Ease of Use: Readable by humans and easily processed by programs.
* Interoperability: Works with almost all programming languages.
* Flexible Schema: Suitable for evolving data structures.
* Compact: Minimal syntax reduces payload size in data transmission.

### MySQL provides functions like JSON_EXTRACT, ->, and ->> to retrieve JSON values.
```-- Extract a JSON value
SELECT JSON_EXTRACT(json_column, '$.key') AS value
FROM table_name;

-- Shortcut using -> (returns JSON)
SELECT json_column->'$.key' AS value
FROM table_name;

-- Shortcut using ->> (returns plain text)
SELECT json_column->>'$.key' AS value
FROM table_name;
```
