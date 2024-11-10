Introduction

Welcome to Plantsy! This project is an admin interface for a plant store, designed to manage plant inventory efficiently. Your task is to implement features that enhance the user experience by adding stateful logic and connecting to our backend API.
Setup
To get started with Plantsy, follow these steps:
Clone this repository to your local machine.
Navigate to the project directory in your terminal.
Run the following command to install the necessary dependencies:
bash
npm install

Start the backend server by running:
bash
npm run server

This will run your backend on port 6001.
In a new terminal window, start the frontend application with:
bash
npm start

Open your browser and navigate to http://localhost:6001/plants to verify that your backend is functioning correctly.
Core Features
As a user of Plantsy, you will be able to:
View all plants when the app starts.
Add a new plant by submitting a form.
Mark plants as "sold out".
Search for plants by name and see a filtered list.
API Endpoints
The base URL for the backend API is: http://localhost:6001
GET /plants
Fetches a list of all plants.
Example Response:
json
[
  {
    "id": 1,
    "name": "Aloe",
    "image": "./images/aloe.jpg",
    "price": 15.99
  },
  {
    "id": 2,
    "name": "ZZ Plant",
    "image": "./images/zz-plant.jpg",
    "price": 25.98
  }
]

POST /plants
Adds a new plant.
Required Headers:
json
{
  "Content-Type": "application/json"
}

Request Object:
json
{
  "name": "string",
  "image": "string",
  "price": number
}

Example Response:
json
{
  "id": 1,
  "name": "Aloe",
  "image": "./images/aloe.jpg",
  "price": 15.99
}

Advanced Features (Optional)
If you have additional time, consider implementing these advanced features:
Update the price of a plant, ensuring it persists after refreshing the page.
Delete a plant, confirming it is removed upon refresh.
Advanced API Endpoints
PATCH /plants/:id
Updates the price of a specific plant.
Required Headers:
json
{
  "Content-Type": "application/json"
}

Request Object:
json
{
  "price": number
}

Example Response:
json
{
  "id": 1,
  "name": "Aloe",
  "image": "./images/aloe.jpg",
  "price": 16.99
}

DELETE /plants/:id
Deletes a specific plant.
Example Response:
json
{}

Author : Steve Baars