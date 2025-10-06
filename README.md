
# 🐳 Docker Quick Guide

## 📌 Definition

Docker is a **platform to run applications** inside lightweight, isolated containers.

---

## 🎯 Key Benefits

* **Consistency/Compatibility** → Runs identically everywhere.
* **Portability** → Works on Windows, Mac, Linux.
* **Speed & Efficiency** → Lightweight, fast startup.

---

## 🧩 Key Concepts

* **Containers** → Packaged software with code + runtime + libraries + environment.
* **Images** → Read-only templates used to create containers.
* **Docker Compose** → Manages multiple containers with one file (`docker-compose.yml`).

---

## 🛠️ Basic Docker Commands

* **Check Docker version**

  ```bash
  docker --version
  ```

* **List running containers**

  ```bash
  docker ps
  ```

* **List all containers (including stopped)**

  ```bash
  docker ps -a
  ```

* **Run a container** (example: Nginx)

  ```bash
  docker run -d -p 8080:80 nginx
  ```

* **Stop a container**

  ```bash
  docker stop <container_id>
  ```

* **Remove a container**

  ```bash
  docker rm <container_id>
  ```

---

## 📂 Why Docker is Useful

* Consistency across environments
* Easy isolation of services
* Simple deployment & scaling

----

# 📂 What is Docker Compose?

**Docker Compose** is a tool that allows you to:

* **Manage multiple containers at once**
* Using a single file (`docker-compose.yml`)
* Instead of typing long `docker run ...` commands multiple times

👉 Perfect for multi-service applications (e.g., Web + Database + Cache).

<img width="1147" height="718" alt="Image" src="https://github.com/user-attachments/assets/20c3b134-835d-451a-ae83-6e8d76d8d1b0" />

---


## ⚙️ Install Docker (Quick Steps)

1. **Download** → Get Docker Desktop (Mac/Windows).
2. **Verify** → `docker --version`
3. **Test Run** → `docker run hello-world`

---

## 🛠️ Basic Docker Compose Commands

* **Start all services (background mode):**

  ```bash
  docker-compose up -d
  ```

* **List containers managed by Compose:**

  ```bash
  docker-compose ps
  ```

* **Stop all containers:**

  ```bash
  docker-compose down
  ```

* **View logs of a service:**

  ```bash
  docker-compose logs -f
  ```

* **Run only a specific service (e.g., db):**

  ```bash
  docker-compose up -d db
  ```

---

## 🎯 Benefits of Docker Compose

* **Easy to use** → Manage all containers with a single file
* **Convenient** → No need to type long commands
* **Flexible** → Can scale services, e.g., run 3 instances of a web service:

  ```bash
  docker-compose up --scale web=3 -d
  ```

---



## 💾 Use Case: Running Databases with Docker

Instead of installing databases manually, use pre-built containers:

* **PostgreSQL** → SQL relational database
* **Cassandra** → NoSQL distributed database
* **InfluxDB** → Time-series database

**Example: Run PostgreSQL**

```bash
docker run -d --name postgres -e POSTGRES_PASSWORD=admin -p 5432:5432 postgres:15
```

---

## 🐍 Anaconda + Docker

Run Anaconda (Python environment) inside a container for Data Science projects without installing Python locally.

**Example:**

```bash
docker run -it continuumio/anaconda3 /bin/bash
```

---

## ✅ Verifying Everything

Check containers:

```bash
docker ps
```

**Expected running services:**

* Postgres
* Cassandra
* InfluxDB
* Anaconda

---



