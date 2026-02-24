# Discover Dollar DevOps Assignment – MEAN Stack Application

This project demonstrates complete setup, containerization, CI/CD integration, Docker Hub image push, and deployment of a MEAN stack application with Nginx reverse proxy.

------------------------------------------------------------

Step 1: Clone the repository

git clone https://github.com/Rakesss/discover-dollar-devops-assignment.git
cd discover-dollar-devops-assignment

------------------------------------------------------------

Step 2: Setup Backend

Navigate to backend folder:

cd backend

Install dependencies:

npm install

Run backend:

npm start

Backend will run on:

http://localhost:5000

------------------------------------------------------------

Step 3: Setup Frontend

Navigate to frontend folder:

cd ../frontend

Install dependencies:

npm install

Run frontend:

ng serve

Frontend will run on:

http://localhost:4200

------------------------------------------------------------

Step 4: Build Docker Images

Go to project root folder:

cd ..

Build backend image:

docker build -t your-dockerhub-username/backend-image ./backend

Build frontend image:

docker build -t your-dockerhub-username/frontend-image ./frontend

Verify images:

docker images

------------------------------------------------------------

Step 5: Login to Docker Hub

docker login

Enter your Docker Hub username and password or access token.

------------------------------------------------------------

Step 6: Push Images to Docker Hub

Push backend image:

docker push your-dockerhub-username/backend-image

Push frontend image:

docker push your-dockerhub-username/frontend-image

Verify images on Docker Hub dashboard.

------------------------------------------------------------

Step 7: Run Application Using Docker Compose

docker-compose up -d

Check running containers:

docker ps

Application will be accessible via browser.

------------------------------------------------------------

Step 8: CI/CD Configuration and Execution

CI/CD pipeline is configured using GitHub Actions or CI server.

Pipeline performs the following automatically:

1. Pull latest code from repository
2. Build Docker images
3. Push Docker images to Docker Hub
4. Deploy application containers

CI/CD execution screenshots are available in:

Screenshots/CI-success/

------------------------------------------------------------

Step 9: Docker Image Build and Push Verification

Docker Hub screenshots showing image build and push are available in:

Screenshots/Dockerhub/

These confirm successful image creation and upload.

------------------------------------------------------------

Step 10: Application Deployment and Working UI

Application deployment screenshots showing running containers and working UI are available in:

Screenshots/VM Images (ubuntu)/

These confirm successful deployment and application functionality.

------------------------------------------------------------

Step 11: Nginx Setup and Configuration

Install Nginx:

sudo apt install nginx -y

Edit Nginx configuration:

sudo nano /etc/nginx/sites-available/default

Example configuration:

server {
    listen 80;

    location / {
        proxy_pass http://localhost:4200;
    }

    location /api {
        proxy_pass http://localhost:5000;
    }
}

Restart Nginx:

sudo systemctl restart nginx

------------------------------------------------------------

Step 12: Infrastructure Verification

Check containers:

docker ps

Check images:

docker images

Check application in browser:

http://localhost

------------------------------------------------------------

Screenshots Included

Screenshots/CI-success/
Shows CI/CD pipeline configuration and successful execution.

Screenshots/Dockerhub/
Shows Docker image build and push process.

Screenshots/VM Images (ubuntu)/
Shows deployed containers and working application UI.

Screenshots/Dockerhub/Container/
Shows running containers.

Screenshots/Dockerhub/Images/
Shows Docker images.

------------------------------------------------------------

All required screenshots and deployment steps are included in this repository.
