# Python Requests Methods Tutorial

This repository demonstrates the use of the Python `requests` library for making HTTP requests. Each method is showcased with examples and explanations.

## Table of Contents
- [Introduction](#introduction)
- [Setup](#setup)
- [HTTP Methods](#http-methods)
  - [GET](#get)
  - [POST](#post)
  - [PUT](#put)
  - [DELETE](#delete)
  - [HEAD](#head)
  - [OPTIONS](#options)
  - [PATCH](#patch)
- [Mock API](#mock-api)
- [Code Samples](#code-samples)
- [License](#license)

---

## Introduction
The `requests` library in Python provides an easy way to interact with HTTP APIs. This project showcases the practical use of different HTTP methods to communicate with a sample API.

---

## Setup
1. Clone this repository:
   ```bash
   git clone <repository-url>
   ```
2. Install the required dependencies:
   ```bash
   pip install requests
   ```

---

## HTTP Methods

### GET
Retrieves data from the server. Example:
```python
import requests

response = requests.get('<mockapi-url>/books')
print(response.json())
```

### POST
Sends new data to the server. Example:
```python
data = {"title": "New Book", "author": "Author Name"}
response = requests.post('<mockapi-url>/books', json=data)
print(response.json())
```

### PUT
Updates an entire resource. Example:
```python
data = {"title": "Updated Title"}
response = requests.put('<mockapi-url>/books/1', json=data)
print(response.json())
```

### DELETE
Deletes a resource. Example:
```python
response = requests.delete('<mockapi-url>/books/1')
print(response.status_code)
```

### HEAD
Fetches headers for a resource. Example:
```python
response = requests.head('<mockapi-url>/books')
print(response.headers)
```

### OPTIONS
Fetches supported HTTP methods for a resource. Example:
```python
response = requests.options('<mockapi-url>/books')
print(response.headers['allow'])
```

### PATCH
Partially updates a resource. Example:
```python
data = {"author": "Updated Author"}
response = requests.patch('<mockapi-url>/books/1', json=data)
print(response.json())
```

---

## Mock API
We used [MockAPI](https://mockapi.io) to create and test endpoints. For this project, the base URL is:  
**https://67336ac32a1b1a4ae11378af.mockapi.io/books**

Feel free to replace `<mockapi-url>` in the examples with this URL.

---

## Code Samples
The complete code is available in the repository under the `examples` directory.

---

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

---
 
