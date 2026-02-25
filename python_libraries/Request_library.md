# Request library

[`Requests`](https://github.com/psf/requests) is a straightforward and user-friendly HTTP toolkit for Python. In detail, it provides an intuitive API for making HTTP requests and handling responses in an easy and easy to understand way. 

| **Method** | **Description** |
| --- | --- |
| [`requests.request()`](https://requests.readthedocs.io/en/latest/api/#requests.request) | Sends a custom HTTP request with the specified method to the given URL |
| [`requests.get()`](https://requests.readthedocs.io/en/latest/api/#requests.get) | Sends a `GET` request to the specified URL |
| [`requests.post()`](https://requests.readthedocs.io/en/latest/api/#requests.post) | Sends a `POST` request to the specified URL |
| [`requests.put()`](https://requests.readthedocs.io/en/latest/api/#requests.put) | Sends a `PUT` request to the specified URL |
| [`requests.patch()`](https://requests.readthedocs.io/en/latest/api/#requests.patch) | Sends a `PATCH` request to the specified URL |
| [`requests.delete()`](https://requests.readthedocs.io/en/latest/api/#requests.delete) | Sends a `DELETE` request to the specified URL |
| [`requests.head()`](https://requests.readthedocs.io/en/latest/api/#requests.head) | Sends a `HEAD` request to the specified URL |

## 1. `requests.request()`

Used when you want to manually specify the HTTP method.

```python
import requests

url = input("Enter URL: ")

response = requests.get(url)

print("Status Code:", response.status_code)
print("Response Headers:", response.headers)
print("Response Text:", response.text)
```

---

## 2. `requests.get()`

Used to retrieve data.

```python
import requests

url = "https://httpbin.org/get"

response = requests.get(url)

print("Status Code:", response.status_code)
print("Data:", response.json())
```

---

## 3. `requests.post()`

Used to send data to a server.

```python
import requests

url = "https://httpbin.org/post"

data = {
    "username": "admin",
    "password": "1234"
}

response = requests.post(url, data=data)

print("Status Code:", response.status_code)
print("Response:", response.json())
```

---

## 4. `requests.put()`

Used to update or replace data on a server.

```python
import requests

url = "https://httpbin.org/put"

data = {
    "name": "John",
    "role": "Security Analyst"
}

response = requests.put(url, data=data)

print("Status Code:", response.status_code)
print("Response:", response.json())
```

---

## 5. `requests.patch()`

Used to partially update data.

```python
import requests

url = "https://httpbin.org/patch"

data = {
    "role": "Penetration Tester"
}

response = requests.patch(url, data=data)

print("Status Code:", response.status_code)
print("Response:", response.json())
```

---

## 6. `requests.delete()`

Used to delete data on a server.

```python
import requests

url = "https://httpbin.org/delete"

response = requests.delete(url)

print("Status Code:", response.status_code)
print("Response:", response.json())
```

---

## 7. `requests.head()`

Used to retrieve headers only (no response body).

```python
import requests

url = "https://httpbin.org/get"

response = requests.head(url)

print("Status Code:", response.status_code)
print("Headers:", response.headers)
```

Note:

- `HEAD` does not return the body.
- Useful for checking if a page exists or checking metadata.

---

### Quick Comparison

| Method | Purpose |
| --- | --- |
| GET | Retrieve data |
| POST | Send new data |
| PUT | Replace existing data |
| PATCH | Update part of data |
| DELETE | Remove data |
| HEAD | Get headers only |
| request() | Custom method |
