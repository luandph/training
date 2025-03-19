In this exercise, you will create a basic HTTP server using Node.js without any external libraries. The server will be able to

- Serve static files and JSON data.
- Handle request payload, query parameters and dynamic routes
- Fetch external API data

Only use built-in Node.js modules `http`, `fs`, `url`, `path`.

Folder structure

- server
  - server.js
  - index.html
  - image.png

### 1.

Create `GET /` route that serves the file `index.html`.

### 2.

Create `POST /echo` route that returns the same data sent in the request payload and query parameters. For example

Request: `POST /echo?name=Alice&age=25`
Payload: `{"message": "Hello"}`
Response

```js
{
    "queryParams": {
        "name": "Alice",
        "age": "25"
    },
    "payload": {
        "message": "Hello"
    }
}
```

### 3.

Create `GET /image` route that serves the file `image.png`. If the file is missing, return `{"error": "Image not found"}`

### 4.

Create `POST /users/{id}` that returns the JSON response from the external API `https://jsonplaceholder.typicode.com/users/{id}`. If no user found, return `{"error": "User not found"}`
