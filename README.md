# 🐳 gokruzk-docker-dots

A collection of Docker configurations for local development environments, featuring ready-to-use stacks for **MySQL + phpMyAdmin** and **PostgreSQL + pgAdmin**.

---

## 📂 Project Structure

```
gokruzk-docker-dots/
├── mssql/
│   ├── docker-compose.yml
│   └── env_template.txt
└── mysql/
│   ├── docker-compose.yml
│   └── env_template.txt
└── postgres/
    ├── docker-compose.yml
    └── env_template.txt
```

Each folder contains a `docker-compose.yml` file and an environment variable template (`env_template.txt`).

---

## 🚀 Quick Start

### Clone the Repository

```bash
git clone https://github.com/Gokruzk/gokruzk-docker-dots.git
cd gokruzk-docker-dots
```

### Setup and Run

Choose your database stack and follow the steps below:

```bash
cd mysql
cp env_template.txt .env
# Edit .env with your preferred credentials and configuration
docker-compose up -d
```
---

## 🛠️ Management Commands

### Stop Containers

```bash
docker-compose down
```

### Stop and Remove All Data

To stop containers and remove persistent volumes:

```bash
docker-compose down -v
```

---

## 📝 Configuration

Before starting any stack, you must configure the environment variables:

1. Copy `env_template.txt` to `.env` in the respective folder
2. Update the values according to your needs (usernames, passwords, ports, etc.)
3. Save the file and run `docker-compose up -d`

---
