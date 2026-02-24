# ╔══════════════════════════════════════════════════════════╗
# 🚀 CRUD DD Task – MEAN Stack Application
# ╚══════════════════════════════════════════════════════════╝

A production-ready full-stack MEAN (MongoDB, Express, Angular, Node.js) CRUD application containerized with Docker and deployed using CI/CD via GitHub Actions to AWS EC2.

---

# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# 📌 PROJECT OVERVIEW
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

This project demonstrates:

✔ Full-stack CRUD application using MEAN stack  
✔ Multi-container Docker architecture  
✔ Docker Hub image management  
✔ CI/CD automation using GitHub Actions  
✔ Automated deployment to AWS EC2  
✔ Nginx for frontend serving  

---

# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# 🏗️ TECH STACK
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

## 🔹 Backend
- Node.js  
- Express.js  
- MongoDB  
- Mongoose  

## 🔹 Frontend
- Angular 15  
- Bootstrap  

## 🔹 DevOps & Deployment
- Docker  
- Docker Compose  
- GitHub Actions  
- Docker Hub  
- AWS EC2  
- Nginx  

---

# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# 🐳 DOCKER ARCHITECTURE
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

The application runs using three containers:

1️⃣ MongoDB → Database  
2️⃣ Backend → Node + Express API  
3️⃣ Frontend → Angular app served via Nginx  

All services are orchestrated using `docker-compose.yml`.

---

# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# 📂 PROJECT STRUCTURE
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

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

# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# ⚙️ RUNNING LOCALLY WITH DOCKER
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

## Step 1: Clone Repository

```bash
git clone https://github.com/Shubham-3177/crud-dd-task-mean-app.git
cd crud-dd-task-mean-app
```

## Step 2: Start Containers

```bash
docker compose up -d --build
```

## Step 3: Access Application

Frontend → http://localhost  
Backend API → http://localhost:8080  
MongoDB → localhost:27017  

---

# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# 🐳 DOCKER HUB IMAGES
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Backend Image  
shubham3177/crud-dd-task-mean-app-backend:latest  

Frontend Image  
shubham3177/crud-dd-task-mean-app-frontend:latest  

---

# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# 🔁 CI/CD PIPELINE (GITHUB ACTIONS)
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

The pipeline is triggered on every push to the `main` branch.

## Workflow Steps

1️⃣ Checkout code  
2️⃣ Login to Docker Hub  
3️⃣ Build Backend Docker image  
4️⃣ Push Backend image to Docker Hub  
5️⃣ Build Frontend Docker image  
6️⃣ Push Frontend image to Docker Hub  
7️⃣ SSH into EC2  
8️⃣ Pull latest images  
9️⃣ Restart containers using Docker Compose  

Workflow file location:

```
.github/workflows/deploy.yml
```

---

# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# ☁️ AWS EC2 DEPLOYMENT
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

## Deployment Flow

✔ EC2 instance configured with Docker & Docker Compose  
✔ Nginx stopped (Docker handles port 80)  
✔ docker-compose.yml present in /home/ubuntu  
✔ CI/CD automatically updates containers on every push  

Live Application:

```
http://<EC2-PUBLIC-IP>
```

---

# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# 🔐 GITHUB SECRETS USED
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

1️⃣ DOCKER_USERNAME  
2️⃣ DOCKER_PASSWORD  
3️⃣ EC2_HOST  
4️⃣ EC2_KEY  

Configured under:

GitHub → Settings → Secrets and Variables → Actions  

---

# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# ✨ FEATURES IMPLEMENTED
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

✔ Create Data  
✔ Read Data  
✔ Update Data  
✔ Delete Data  
✔ Containerized Architecture  
✔ Automated CI/CD Deployment  
✔ Production-ready Docker images  

---

# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# 🎯 WHAT THIS PROJECT DEMONSTRATES
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

✔ Real-world DevOps workflow  
✔ Containerized full-stack application  
✔ Infrastructure automation  
✔ Cloud deployment  
✔ CI/CD best practices  

---

# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# 👨‍💻 AUTHOR
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Shubham S Kadatare  
DevOps Engineer | Cloud & Automation Enthusiast  

If you found this project useful, feel free to ⭐ star the repository.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
