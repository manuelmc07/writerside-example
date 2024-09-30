# Overview

## Introduction

The **Localhost CRUD API** is a simple RESTful API designed to demonstrate basic Create, Read, Update, and Delete (CRUD) operations on a localhost server. The API allows developers to perform CRUD actions on a resource called `items`. This API is built following the OpenAPI 3.0.2 specification, ensuring clarity and adherence to RESTful conventions.

## Main Features

1. **Retrieve All Items**: Get a complete list of all items in the system.
2. **Retrieve a Single Item**: Fetch a specific item by its unique ID.
3. **Create a New Item**: Add a new item to the system with a unique ID, name, and description.
4. **Update an Existing Item**: Modify an existing item's details, such as its name and description.
5. **Delete an Item**: Remove an item from the system using its unique ID.

## Endpoints

### `/items`
- **GET**: Retrieve all items.
- **POST**: Create a new item.

### `/items/:id`
- **GET**: Retrieve an item by its ID.
- **PUT**: Update an existing item by its ID.
- **DELETE**: Delete an item by its ID.

## Example Request

### Create a New Item (POST `/items`)

```http
POST /items
Content-Type: application/json

{
  "name": "Item 1",
  "description": "This is a sample item"
}
```

### Example Response

```json
{
  "id": "1",
  "name": "Item 1",
  "description": "This is a sample item"
}
```

## Error Handling

The API uses a consistent error response format across all endpoints. Common HTTP status codes include:

- **200 OK**: The request was successful, and the expected data is returned.
- **400 Bad Request**: The request is invalid, usually due to missing or incorrect parameters.
- **404 Not Found**: The requested item or resource could not be found.
- **500 Internal Server Error**: An error occurred on the server.

### Example Error Response

```json
{
  "type": "about:blank",
  "title": "Error",
  "detail": "An error occurred",
  "instance": "/items",
  "timestamp": "2024-09-20T14:00:00Z",
  "time": 1726846312308
}
```

## Security

Since this is a simple demonstration API for local development, no authentication is required. However, you can integrate authentication layers such as JWT or OAuth if needed for production environments.

## Getting Started

To use this **Localhost CRUD API**, follow these steps:
1. Set up a local development server on `http://localhost:3000`.
2. Use the provided endpoints to manage `items` by creating, retrieving, updating, and deleting them.
3. Test the API using tools such as Postman or curl for local testing.
