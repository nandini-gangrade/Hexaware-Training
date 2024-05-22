# File Handling in Python

File handling is an essential aspect of programming that allows you to read, write, and manipulate data stored in files. Python provides robust modules such as `json` and `csv` for handling different file formats.

## JSON File Handling

JSON (JavaScript Object Notation) is a lightweight data interchange format that is easy to read and write for humans and machines. Python's `json` module allows you to work with JSON data.

### Syntax and Usage

1. **json.loads**: Converts a JSON string to a Python dictionary.
   ```python
   import json

   bank_data = """
   [
       {
           "id": 1,
           "name": "John Doe",
           "email": "johndoe@example.com",
           "isActive": true,
           "balance": 150.75
       },
       {
           "id": 2,
           "name": "Jane Smith",
           "email": "janesmith@example.com",
           "isActive": false,
           "balance": 500.50
       },
       {
           "id": 3,
           "name": "Emily Jones",
           "email": "emilyjones@example.com",
           "isActive": true,
           "balance": 0.00
       }
   ]
   """

   bank_data_dict = json.loads(bank_data)
   ```
   - **Explanation**: `json.loads` takes a JSON formatted string and converts it into a Python dictionary, enabling you to work with the data programmatically.

2. **json.dumps**: Converts a Python dictionary to a JSON string.
   ```python
   bank_data1 = json.dumps(bank_data_dict)
   print(bank_data1)
   ```
   - **Explanation**: `json.dumps` takes a Python dictionary and converts it back to a JSON formatted string, which is useful for output or storage.

3. **Writing to a JSON File**
   ```python
   with open("bank_accounts.json", "w") as file:
       json.dump(bank_data_dict, file, indent=4)
   ```
   - **Explanation**: `with open("bank_accounts.json", "w") as file` opens a file named `bank_accounts.json` in write mode. The `json.dump` method writes the dictionary to the file in JSON format. The `indent=4` argument makes the output human-readable by adding indentation.

4. **Reading from a JSON File**
   ```python
   with open("bank_accounts.json", "r") as file:
       data = json.load(file)
       print(data)
   ```
   - **Explanation**: `with open("bank_accounts.json", "r") as file` opens the file in read mode. The `json.load` method reads the JSON data from the file and converts it into a Python dictionary.

### Practical Example

```python
# Convert JSON string to dictionary
bank_data_dict = json.loads(bank_data)

# Increase balance of active users by 10%
for i in bank_data_dict:
    if i["isActive"]:
        i["balance"] += i["balance"] * 0.10

# Convert dictionary back to JSON string
bank_data1 = json.dumps(bank_data_dict)
print(bank_data1)

# Write to a JSON file
with open("bank_accounts.json", "w") as file:
    json.dump(bank_data_dict, file, indent=4)

# Read from a JSON file
with open("bank_accounts.json", "r") as file:
    data = json.load(file)
    print(data)
```

## CSV File Handling

CSV (Comma-Separated Values) is a simple file format used to store tabular data. Python's `csv` module provides functionality to read from and write to CSV files.

### Syntax and Usage

1. **csv.writer**: Writes data to a CSV file.
   ```python
   import csv

   data = [
       ["id", "name", "email", "isActive", "balance"],
       [1, "John Doe", "johndoe@example.com", True, 150.75],
       [2, "Jane Smith", "janesmith@example.com", False, 500.50],
       [3, "Emily Jones", "emilyjones@example.com", True, 0.00]
   ]

   with open("citizens.csv", "w", newline="") as file:
       writer = csv.writer(file)
       writer.writerows(data)
   ```
   - **Explanation**: `with open("citizens.csv", "w", newline="") as file` opens a file named `citizens.csv` in write mode. The `csv.writer(file)` creates a CSV writer object. The `writer.writerows(data)` method writes the data to the CSV file, row by row.

2. **csv.reader**: Reads data from a CSV file.
   ```python
   with open("citizens.csv", "r", newline="") as file:
       reader = csv.reader(file)
       data = [row for row in reader]
       print(data)
   ```
   - **Explanation**: `with open("citizens.csv", "r", newline="") as file` opens the file in read mode. The `csv.reader(file)` creates a CSV reader object. The list comprehension `[row for row in reader]` reads all rows from the CSV file into a list.

### Practical Example

```python
import csv

# Data to be written to CSV
data = [
    ["id", "name", "email", "isActive", "balance"],
    [1, "John Doe", "johndoe@example.com", True, 150.75],
    [2, "Jane Smith", "janesmith@example.com", False, 500.50],
    [3, "Emily Jones", "emilyjones@example.com", True, 0.00]
]

# Write data to CSV file
with open("citizens.csv", "w", newline="") as file:
    writer = csv.writer(file)
    writer.writerows(data)

# Read data from CSV file
with open("citizens.csv", "r", newline="") as file:
    reader = csv.reader(file)
    data = [row for row in reader]
    print(data)
```

## Summary

- **json.dumps**: Converts a Python dictionary to a JSON string.
- **json.dump**: Writes a Python dictionary to a JSON file.
- **json.loads**: Converts a JSON string to a Python dictionary.
- **json.load**: Reads JSON data from a file and converts it to a Python dictionary.
- **csv.writer**: Writes data to a CSV file.
- **csv.reader**: Reads data from a CSV file.

This guide covers the basics of file handling in Python, focusing on JSON and CSV formats, providing you with the necessary tools to read, write, and manipulate data in these formats.
