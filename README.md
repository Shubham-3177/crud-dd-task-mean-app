# 🚀 CRUD DD Task – MEAN Stack Application
---

A production-ready full-stack MEAN (MongoDB, Express, Angular, Node.js) CRUD application containerized with Docker and deployed using CI/CD via GitHub Actions to AWS EC2.

---

## 📌 Project Overview
---

✔ Full-stack CRUD application using MEAN stack  
✔ Multi-container Docker architecture  
✔ Docker Hub image management  
✔ CI/CD automation using GitHub Actions  
✔ Automated deployment to AWS EC2  
✔ Nginx for frontend serving  

---

## 🏗️ Tech Stack
---

### Backend
- Node.js  
- Express.js  
- MongoDB  
- Mongoose  

### Frontend
- Angular 15  
- Bootstrap  

### DevOps & Deployment
- Docker  
- Docker Compose  
- GitHub Actions  
- Docker Hub  
- AWS EC2  
- Nginx  

---

## 🐳 Docker Architecture
---

The application runs using three containers:

1. MongoDB – Database  
2. Backend – Node + Express API  
3. Frontend – Angular app served via Nginx  

All services are orchestrated using `docker-compose.yml`.

---

## 📂 Project Structure
---

```
crud-dd-task-mean-app/
│
├── backend/
│   ├── Dockerfile
│   └── source code
│
├── frontend/
│   ├── Dockerfile
│   └── Angular source code
│
├── docker-compose.yml
└── .github/workflows/deploy.yml
```

---

## ⚙️ Running Locally with Docker
---

### Clone Repository
```bash
git clone https://github.com/Shubham-3177/crud-dd-task-mean-app.git
cd crud-dd-task-mean-app
```

### Start Containers
```bash
docker compose up -d --build
```

### Access Application
Frontend → http://localhost  
Backend API → http://localhost:8080  
MongoDB → localhost:27017  

---

## 🖼️ Demo Output
---

### 🔹 Tutorial 
![Tutorial Page](https://github.com/Shubham-3177/crud-dd-task-mean-app/blob/main/images/tutorial.png)

### 🔹 Add_Tutorial
![Add_Tutorial Page](https://github.com/Shubham-3177/crud-dd-task-mean-app/blob/main/images/add_tutorial.png)

### 🔹 Running Instance
![Running Instance](https://github.com/Shubham-3177/crud-dd-task-mean-app/blob/main/images/instance.jpeg)


---

## 🐳 Docker Hub Images
---

Backend → shubham3177/crud-dd-task-mean-app-backend:latest  
Frontend → shubham3177/crud-dd-task-mean-app-frontend:latest  

---

## 🔁 CI/CD Pipeline (GitHub Actions)
---

Triggered on every push to `main` branch.

1. Checkout code  
2. Login to Docker Hub  
3. Build Backend Docker image  
4. Push Backend image  
5. Build Frontend Docker image  
6. Push Frontend image  
7. SSH into EC2  
8. Pull latest images  
9. Restart containers  

Workflow file: `.github/workflows/deploy.yml`

---

## ☁️ AWS EC2 Deployment
---

✔ EC2 configured with Docker & Docker Compose  
✔ Port 80 exposed  
✔ docker-compose.yml inside `/home/ubuntu`  
✔ Automatic container updates via CI/CD  

Live Application:  
```
http://<EC2-PUBLIC-IP>
```

---

## 🔐 GitHub Secrets
---

- DOCKER_USERNAME  
- DOCKER_PASSWORD  
- EC2_HOST  
- EC2_KEY  

Configured under:  
GitHub → Settings → Secrets and Variables → Actions  

---

## ✨ Features
---

✔ Create Data  
✔ Read Data  
✔ Update Data  
✔ Delete Data  
✔ Containerized Architecture  
✔ Automated CI/CD Deployment  

---

## 👨‍💻 Author
---

Shubham S Kadatare  
DevOps Engineer | Cloud & Automation Enthusiast  

If this project helped you, consider giving it a ⭐
