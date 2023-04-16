# Social Media API using NoSQL Database

This is a social media startup API that uses a NoSQL database to handle large amounts of unstructured data. The API allows users to create accounts, post thoughts, react to thoughts, add and remove friends, and manage their profiles.

## Technologies used
The API is built with Node.js and Express.js. Mongoose is used as the Object Data Modeling (ODM) library to handle communication with the MongoDB NoSQL database. The API is tested using Insomnia, a popular REST API client.

## Walkthrough Video

[social_media_api_testing.webm](https://user-images.githubusercontent.com/55256787/232344247-27c44e0f-e1ee-4417-8adc-f4e4d57c07df.webm)

## Installation
1. Clone the repository
2. Install dependencies using the following command:`npm install`
3. Create a `.env file` in the root directory and add the following environment variables:
```
MONGODB_URI=<your MongoDB URI>
JWT_SECRET=<your JWT secret>
```
4. Start the API using the following command: `npm start`

The server will be started and the Mongoose models will be synced to the MongoDB database.

## API routes
### Users
- GET `/api/users`: Get all users
- GET `/api/users/:id`: Get a single user by ID
- POST `/api/users`: Create a new user
- PUT `/api/users/:id`: Update an existing user by ID
- DELETE `/api/users/:id`: Delete a user by ID

### Thoughts
- GET `/api/thoughts`: Get all thoughts
- GET `/api/thoughts/:id`: Get a single thought by ID
- POST `/api/thoughts`: Create a new thought
- PUT `/api/thoughts/:id`: Update an existing thought by ID
- DELETE `/api/thoughts/:id`: Delete a thought by ID
### Reactions
- POST `/api/thoughts/:thoughtId/reactions`: Add a reaction to a thought
- DELETE `/api/thoughts/:thoughtId/reactions/:reactionId`: Remove a reaction from a thought
### Friends
- POST `/api/users/:userId/friends/:friendId`: Add a friend to a user's friend list
- DELETE `/api/users/:userId/friends/:friendId`: Remove a friend from a user's friend list

## Testing
The API can be tested using Insomnia or a similar REST API client. The following test cases should be performed:

1. Create a user
2. Get all users and verify that the created user is in the list
3. Get the created user by ID
4. Update the created user
5. Delete the created user
6. Create a thought
7. Get all thoughts and verify that the created thought is in the list
8. Get the created thought by ID
9. Update the created thought
10. Delete the created thought
11. Add a reaction to a thought
12. Remove a reaction from a thought
13. Add a friend to a user's friend list
14. Remove a friend from a user's friend list

### Author: Naz Yasar
[![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)](https://github.com/nazyasar)
[![LinkedIn](https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nazyasar/)
