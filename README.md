# E-Shop – Full-Stack E-Commerce Website

## 1. Project Overview

E-Shop is a full-stack e-commerce website built with:

- **Backend:** Node.js, Express, MongoDB
- **Frontend:** React, Vite
- **Deployment:** Docker Compose
- **Redis:** Asynchronous task queue
- **Worker:** Background email sending
- **Nginx:** Reverse proxy and load balancer
- **Realtime:** Socket.IO
- **Authentication:** JWT & Google OAuth

---

## 2. How to Run (Docker Compose)

### Build images
```bash
docker compose build
```

### Start all containers
```bash
docker compose up -d
```

### Build and start in one command
```bash
docker compose up -d --build
```

### View running containers
```bash
docker ps
```

### Stop and remove containers
```bash
docker compose down
```

### Clean all unused images, volumes, and networks
```bash
docker compose down -v --rmi all
docker system prune -a --volumes -f
docker volume rm $(docker volume ls -q)
```

> **Note:** You may need to adjust environment variables in `.env` if running locally.

---

## 3. Testing Functionality

### Check which port the application is running on
```bash
docker ps
```

### Access frontend
```
http://localhost
```

### Verify backend load balancing
```bash
docker logs -f ecommerce_api_1
docker logs -f ecommerce_api_2
```

### Verify asynchronous email worker
```bash
docker logs -f ecommerce_worker
```

---

## 4. Access Information

- **Frontend:** http://localhost  
- **Backend API:** http://localhost:5000/api/products  
- **MongoDB:** Internal port `27017`  
- **Redis:** Internal port `6379`  

---

## 5. Admin Account (Demo)

- **Email:** admin@gmail.com  
- **Password:** 123456  

> *This account is for demonstration purposes only.*
