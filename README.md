PROJECT STRUCTURE :

discover-dollar-devops-assignment/
│
├── backend/
│   └── Dockerfile
│
├── frontend/
│   └── Dockerfile
│
├── docker-compose.yml
│
├── .github/workflows/
│   └── deploy.yml
│
└── README.md


DOCKER IMAGES:
    BACKEND:
      player8598/dd-backend:latest
    FRONTEND:
      player8598/dd-frontend:latest

DOCKER SETUP:

   docker-compose up -d
   docker ps

CI/CD Pipeline (GitHub Actions):
   .github/workflows/deploy.yml
