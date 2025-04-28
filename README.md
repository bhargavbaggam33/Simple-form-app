## Simple Form App

## 1. Install Required Software

Make sure the user has installed:
Docker

Docker Compose

Git

## 2. Authenticate to GitHub
1. Generate a GitHub Personal Access Token (PAT).
2. Clone the repository using
   
         https://<github-username>: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@github.com/bhargavbaggam01/simple-form-app.git
   
## 3. Running the Application
Start all services using Docker Compose:

      docker-compose up --build

This will:
Pull required images.
Create a Docker network.
Start MySQL, Redis, and Flask containers.

## 4. Verifications (Optional)
1. Check MySQL Database:
   
       mysql -h 127.0.0.1 -P 3307 -u root -p
   
       USE form_app;
   
       SELECT * FROM users;
   
You should see form submissions stored in the users table.

2. Check Redis Cache

         redis-cli -h 127.0.0.1 -p 6379

         keys *

## 5. Stopping the Application

When finished, gracefully stop all services:

      docker-compose down -v

-v flag removes attached volumes (MySQL persistent data).
