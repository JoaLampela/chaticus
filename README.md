### ✅ `Chaticus/README.md`

# 🗨️ Chaticus

Chaticus is a simple chat app demo designed to teach Docker Compose, Node.js, PostgreSQL, and web development best practices.

This project demonstrates how to build and connect a frontend, backend, and database using Docker Compose — all with clean structure and minimal setup.

---

## 🧱 Project Structure

```
Chaticus/
├── Backend/          # Node.js + Express backend API
├── Frontend/         # Static HTML/CSS/JS frontend served by Nginx
├── Database/         # SQL files for initial database schema and content
├── .env              # Environment variables for PostgreSQL and pgAdmin
└── docker-compose.yml
```

---

## 🚀 How to Run It

> ⚠️ Make sure [Docker Desktop](https://www.docker.com/products/docker-desktop/) is running.

1. Open a terminal in the `Chaticus/` folder.
2. Run:

```bash
docker-compose up --build
```

To reset the database and re-run `init.sql` and `content.sql`, run:

```bash
docker-compose down -v
docker-compose up --build
```

---

## 🌐 Access the App

| Component | URL                       |
|----------|----------------------------|
| Frontend | http://localhost:8080      |
| Backend  | http://localhost:3000/chat |
| pgAdmin  | http://localhost:5050      |

**pgAdmin Login:**

- Email: `joalampela@gmail.com`
- Password: `password123`

Once logged in, add a new server:
- Hostname: `db`
- Username: `joal`
- Password: `password123`

---

## 🛠️ Technologies Used

- Node.js (v18+)
- Express
- PostgreSQL 15
- pgAdmin 4
- Docker + Docker Compose
- Nginx (for static frontend)

---

## 📦 Environment Configuration

`.env` file contents:

```env
POSTGRES_USER=joal
POSTGRES_PASSWORD=password123
POSTGRES_DB=chaticus

PGADMIN_DEFAULT_EMAIL=joalampela@gmail.com
PGADMIN_DEFAULT_PASSWORD=password123
```

---

## 📚 For Students

Try modifying:
- The HTML/CSS in `Frontend/`
- The backend logic in `Backend/server.js`
- The database contents in `Database/content.sql`

Then rebuild the project to see your changes!

---

Happy hacking! 🐳🧠
