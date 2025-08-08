# 🐍 Python Flask + Redis Counter App using Custom Docker Bridge Network (`JHC`)

This example demonstrates a simple Flask (Python) frontend connecting to a Redis backend, using a **custom Docker bridge network** called `JHC`. The app displays a counter that increments every time the page is loaded.

---

## ✅ Prerequisites

- Docker installed on your system
- Basic understanding of Docker commands

---

## 🚀 How to Run This Example
### 1. Create custom bridge network
```
docker network create JHC
```
### 2. Build the Python Flask image (run this from the directory containing the Dockerfile)
```
docker build -t python-frontend .
```
### 3. Run Redis container
```
docker run -d --name redis --network JHC redis:alpine
```
### 4. Run Flask frontend container
```
docker run -d --name frontend  --network JHC -p 8080:5000 python-frontend
```
### 5. Access the app in your browser
### Open: http://localhost:8080
#### 6. Commonds and steps
#docker create network MYN
#docker ps -a
#docker images
#docker build -t python-backend .
#docker run -d --name backend-container -p 1234:5000 --network MYN python-backend
#docker logs backend-container
#curl http://localhost:1234
#docker ps -a
#docker rm -f 229f8b8637dd
#docker rmi -f python-backend
#docker build -t python-backend .
#docker run -d --name backend-container -p 1234:5000 --network MYN python-backend
#docker ps -a
#docker backend-container
#logs
#docker logs backend-container
#cd .
#cd ..
#ls
#cd frontend/
#docker ps
#docker build -t fronted-ui .
#docker build -t frontend-ui .
#docker run -d --name frontend-container --network MYN -p 10:80 frontend-ui
#docker ps -a
#docker images
#docker rm -f fronted-ui
#docker rmi -f fronted-ui
#docker ps -a
