# 🐳 gokruzk-docker-dots

A collection of Docker configurations for local development.  
Includes ready-to-use stacks for **MySQL + phpMyAdmin** and **PostgreSQL + pgAdmin**.

---

## 📂 Project Structure

gokruzk-docker-dots/
│
├── mysql/
│ ├── docker-compose.yml
│ └── env_template.txt
│
└── postgres/
├── docker-compose.yml
└── env_template.txt

yaml
Copy code

Each folder contains a `docker-compose.yml` file and an environment variable template (`env_template.txt`).

---

## ⚙️ How to Use

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/<your-username>/gokruzk-docker-dots.git
cd gokruzk-docker-dots
2️⃣ Configure Environment Variables
Each stack includes an env_template.txt file.
You must copy it and rename it to .env before starting the containers.

🐬 MySQL
bash
Copy code
cd mysql
cp env_template.txt .env
Then edit .env and update the values (user, password, ports, etc).

🐘 PostgreSQL
bash
Copy code
cd postgres
cp env_template.txt .env
Then edit .env and update the values.

3️⃣ Run the Containers
From the corresponding folder:

🐬 MySQL + phpMyAdmin
bash
Copy code
cd mysql
docker-compose up -d
phpMyAdmin → http://localhost:8081

🐘 PostgreSQL + pgAdmin
bash
Copy code
cd postgres
docker-compose up -d
pgAdmin → http://localhost:8080

4️⃣ Stop and Remove Containers
bash
Copy code
docker-compose down
To also remove persistent data volumes:

bash
Copy code
docker-compose down -v
```
