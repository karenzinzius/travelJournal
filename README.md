# Full-Stack Application (SPA + Auth + API)

This project is a full-stack application structured into three main parts:

- SPA – Frontend single-page application
- Auth – Authentication and authorization service
- API – Backend API for business logic and data handling

The project is designed to keep concerns separated and make the codebase easier to scale and maintain.

## Project Structure

.
├── spa/        # Frontend (Single Page Application)
├── auth/       # Authentication service
├── api/        # Backend API
├── package.json
└── README.md

## SPA (Frontend)

The SPA folder contains the client-side application.

Responsibilities:
- User interface (UI)
- Client-side routing
- Calling the API and Auth services
- Displaying data and handling user interactions

Typical features:
- Login and signup forms
- Protected routes
- API data rendering

## Auth (Authentication Service)

The Auth folder handles everything related to authentication and authorization.

Responsibilities:
- User registration
- User login
- Token generation (e.g. JWT)
- Token validation
- Password hashing

Typical endpoints:
- POST /register
- POST /login
- POST /logout
- GET /me

## API (Backend)

The API folder contains the main backend logic.

Responsibilities:
- Business logic
- Database access
- CRUD operations
- Protected routes (authentication required)

Example endpoints:
- GET /items
- POST /items
- PUT /items/:id
- DELETE /items/:id

## Environment Variables

Create environment files where needed:

OPENAI_API_KEY=your_api_key_here  
DATABASE_URL=your_database_url  
JWT_SECRET=your_secret  

Never commit .env files to version control.

## Running the Project

Install dependencies:
npm install

Run SPA:
cd spa
npm run dev

Run Auth service:
cd auth
npm run dev

Run API:
cd api
npm run dev

## Authentication Flow (Overview)

1. User logs in via the SPA
2. Auth service validates credentials
3. Auth service returns a token
4. SPA stores the token (e.g. localStorage)
5. SPA sends the token with API requests
6. API validates the token before responding

## Project Goals

- Practice full-stack architecture
- Learn authentication flows
- Separate frontend, auth, and backend logic
- Build a scalable and maintainable system

