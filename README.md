## Simple Form App

## 1. Install Required Software

Make sure the user has installed:
Docker
Docker Compose
Git

## 2. Authenticate to GitHub
1. Generate a GitHub Personal Access Token (PAT).
2. Clone the repository using
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
