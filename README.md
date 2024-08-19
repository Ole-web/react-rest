My REST API


Overview
This project is a REST API built using Node.js, Express.js, and MongoDB with Mongoose. It provides CRUD operations for managing items in a MongoDB database. The API is designed to be integrated with a React application, providing endpoints to create, read, update, and delete items.

Features
Create: Add new items to the database.
Read: Retrieve all items or a specific item by ID.
Update: Modify an existing item by ID.
Delete: Remove an item from the database by ID.
Installation
Prerequisites
Node.js (v14 or higher recommended)
MongoDB (for local development)
Getting Started
Clone the Repository
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd my-rest-api
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd my-rest-api
npm install
Set Up MongoDB

Ensure MongoDB is installed and running on your local machine. By default, the application connects to mongodb://localhost:27017/mydatabase. You can modify this in config/db.js if needed.

Run the Application

Use nodemon to start the server in development mode:
npm start
The server will start on port 5000 (or the port specified in your environment).

API Endpoints
1. Create a New Item
Endpoint: POST /api/items

Request Body:
{
  "name": "Item Name",
  "description": "Item Description"
}
Response:
{
  "_id": "item_id",
  "name": "Item Name",
  "description": "Item Description",
  "__v": 0
}
 Get All Items
Endpoint: GET /api/items

Response:
[
  {
    "_id": "item_id",
    "name": "Item Name",
    "description": "Item Description",
    "__v": 0
  }
]
Get an Item by ID
Endpoint: GET /api/items/:id

Response:
{
  "_id": "item_id",
  "name": "Item Name",
  "description": "Item Description",
  "__v": 0
}
 Update an Item by ID
Endpoint: PUT /api/items/:id

Request Body:
{
  "name": "Updated Item Name",
  "description": "Updated Item Description"
}
Response:
{
  "_id": "item_id",
  "name": "Updated Item Name",
  "description": "Updated Item Description",
  "__v": 0
}
Delete an Item by ID
Endpoint: DELETE /api/items/:id

Response:
{
  "message": "Item deleted"
}
Testing the Integration
To test the integration with the React application, ensure that the React app is configured to make HTTP requests to the API endpoints provided above. Make sure to handle CORS if your React app and API are running on different ports.

License
This project is licensed under the MIT License - see the LICENSE file for details.

Contributing
Feel free to fork this repository, create a branch, and submit a pull request with your improvements or fixes. Please follow the existing code style and ensure that all tests pass before submitting.

