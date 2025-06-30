## 📁 Distributed FTP Server (Microservices + CLI + Web)

A simple, educational **distributed file transfer system** built with Python and Flask, featuring:

* 🔐 Auth microservice (`auth_service`)
* 📂 File upload/download microservice (`file_service`)
* 🌐 Web frontend (`frontend`)
* 💻 Command-line client (`ftp_cli`)

This project is designed as a **Distributed Systems semester project**, supporting both **web UI** and **CLI interface**.

---

## 📦 Features

* 🧩 Modular microservices (Auth, File)
* ✅ User registration & login
* 📤 Upload/download files via web or CLI
* 🔐 Secure password hashing
* ⛔ Max upload size + file type restrictions
* 🌐 Deployable on Render (free tier)
* 📊 Clean architecture for showcasing distributed design

---

## 📁 Project Structure

```bash
DISTRIBUTED-FTP-SERVER/
├── auth_service/         # Auth microservice
├── file_service/         # File handling microservice
├── frontend/             # Web UI using Flask + templates
├── ftp_cli/              # Command-line interface client
├── docs/                 # Project report/docs
└── README.md
```

---

## 🚀 Deployment (Render)

Each microservice is deployed separately:

| Service      | Deployed URL (Example)                         |
| ------------ | ---------------------------------------------- |
| Auth Service | `https://auth-service.onrender.com`            |
| File Service | `https://file-service.onrender.com`            |
| Frontend     | `https://ftp-frontend.onrender.com` (Optional) |

### 🛠 Render Setup Steps

1. Push each folder to GitHub
2. Add `requirements.txt`, `app.py`, and `Procfile` in each service
3. Deploy as **Web Services** on [Render](https://render.com)
4. Set Build: `pip install -r requirements.txt`
5. Set Start Command: `gunicorn app:app`

See full deployment steps in the project report or [Deployment Guide](#).

---

## 🖥️ CLI Usage

### ⬇️ Setup

```bash
cd ftp_cli
pip install -r requirements.txt
python main.py
```

### 🔐 Commands

| Command    | Description                  |
| ---------- | ---------------------------- |
| `signup`   | Register new user            |
| `login`    | Login with username/password |
| `upload`   | Upload file to server        |
| `list`     | List uploaded files          |
| `download` | Download file from server    |
| `logout`   | Logout current session       |

---

## 🌐 Web Usage

Go to your deployed **frontend URL**, sign up/login, and use the UI to upload and download files.

---

## 🛡️ Security Notes

* Passwords are hashed with `werkzeug.security`
* `MAX_CONTENT_LENGTH` prevents large uploads (default: 10MB)
* `ALLOWED_EXTENSIONS` limits file types

---

## 🧪 Testing

Each microservice can be tested individually using:

* **Postman**
* **curl**
* **Browser UI**
* **CLI**

---

## 📄 License

This project is for **educational and academic use** under [MIT License](LICENSE).

---

## 🙌 Acknowledgements

* Flask / Flask-Login
* Render.com
* Bootstrap
* MAKAUT (for the Distributed Systems curriculum)
