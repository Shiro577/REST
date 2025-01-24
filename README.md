# User Management API

## Setup
1. Clone the repository
2. Run `npm install`
3. Start the server: `node index.js`
4. API will be available at `http://localhost:3000`

## API Endpoints

### Get All Users
- **URL**: `/api/users`
- **Method**: `GET`
- **Success Response**:
  - Code: 200
  - Content: 
    ```json
    [
      { "id": 1, "name": "John", "email": "john@example.com" },
      { "id": 2, "name": "Jane", "email": "jane@example.com" }
    ]
    ```
- **Error Response**: 
  - Code: 500
  - Content: `{ message: "Internal Server Error" }`

### Get User by ID
- **URL**: `/api/users/:id`
- **Method**: `GET`
- **URL Params**: `id=[integer]`
- **Success Response**:
  - Code: 200
  - Content: 
    ```json
    { "id": 1, "name": "John", "email": "john@example.com" }
    ```
- **Error Response**:
  - Code: 404
  - Content: `{ message: "User not found" }`

### Create a New User
- **URL**: `/api/users`
- **Method**: `POST`
- **Request Body**: 
  ```json
  { "name": "Alice", "email": "alice@example.com" }
