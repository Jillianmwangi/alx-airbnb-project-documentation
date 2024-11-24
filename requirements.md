# alx-airbnb-project-documentation

1. User Authentication
Technical Requirements
API Endpoints:

POST /api/auth/signup
Input:
json
Copy code
{
  "username": "string",
  "email": "string",
  "password": "string"
}
Output (Success):
json
Copy code
{
  "message": "User registered successfully",
  "userId": "string"
}
Output (Error):
json
Copy code
{
  "error": "User already exists"
}
POST /api/auth/login
Input:
json
Copy code
{
  "email": "string",
  "password": "string"
}
Output (Success):
json
Copy code
{
  "message": "Login successful",
  "token": "string"
}
Output (Error):
json
Copy code
{
  "error": "Invalid credentials"
}
Validation Rules:

Email must be a valid format.
Password must have at least 8 characters, including an uppercase letter, number, and special character.
Username should be unique and between 3-15 characters.
Performance Criteria:

Response time for login and signup requests should be <200ms.
Handle concurrent signups of up to 100 users/sec.
