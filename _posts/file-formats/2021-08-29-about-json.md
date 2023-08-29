---
title: "What is JavaScript Object Notation (JSON)?"
author: Dachan Kyong
date: 2021-08-29 08:00:00 +0900
categories: [File Format, JavaScript Object Notation (JSON)]
tags: [json]
render_with_liquid: false
---

## About JSON
`JSON` (JavaScript Object Notation) is a lightweight data interchange format that is easy for humans to read and write, and easy for machines to parse and generate. It is often used to transmit data between a server and a web application, as well as for configuration files and other data storage purposes.

`JSON` is designed to be a language-independent format, meaning it can be used with various programming languages, not just JavaScript. It has become a popular choice for representing structured data due to its simplicity and flexibility.

Here are some key characteristics and concepts related to JSON:


## Keys To Know

### Syntax
`JSON` syntax is a subset of JavaScript object literal notation. It consists of key-value pairs, where keys are strings and values can be strings, numbers, objects, arrays, booleans, or null. Keys are enclosed in double quotes, and values can be enclosed in double quotes for strings, or left unquoted for numbers, booleans, and null.

### Data Types
- `Object`: An unordered collection of key-value pairs enclosed in curly braces {}.
- `Array`: An ordered collection of values enclosed in square brackets [].
- `String`: A sequence of characters enclosed in double quotes.
- `Number`: A numerical value, which can be integer or floating-point.
- `Boolean`: Represents true or false.
- `Null`: Represents a null value.

### Example

```bash
{
    "name": "John",
    "age": 30,
    "isStudent": false,
    "hobbies": ["reading", "swimming"],
    "address": {
        "street": "123 Main St",
        "city": "Cityville"
    },
    "isActive": null
}
```
{: file='json'}

### Parsing and Generating:
Most programming languages provide built-in support for parsing (converting a JSON string into a data structure) and generating (converting a data structure into a JSON string) JSON. For example, in JavaScript, you can use JSON.parse() to parse JSON and JSON.stringify() to generate JSON.

### Usage
JSON is commonly used in web APIs to transmit data between a server and a client, in configuration files for applications, and in data storage formats. It's particularly well-suited for situations where human readability is important, such as debugging or manual editing of configuration files.

### Limitations
JSON has some limitations, such as not supporting comments, functions, or circular references.


### Alternatives
There are other data interchange formats like XML (eXtensible Markup Language), YAML (YAML Ain't Markup Language), and Protocol Buffers. Each format has its own strengths and use cases.

---
---
---
---

Overall, JSON's simplicity, compatibility with various programming languages, and wide adoption make it a popular choice for representing structured data in a variety of applications.