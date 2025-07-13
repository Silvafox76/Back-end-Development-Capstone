# 🎵🎤 Django Concert Manager – Back-End Development Capstone

This capstone project is a full-stack Django application that manages concerts, songs, and photo submissions with admin oversight. It demonstrates key backend concepts including database modeling, authentication, migrations, CRUD logic, and deployment via Docker.

Originally built as part of a Back-End Development certification with IBM, this project simulates a realistic backend stack suitable for internal CMS tools or portfolio demonstration.

---

## 🧰 Tech Stack

- **Backend**: Python 3.x, Django
- **Frontend**: HTML, Django Templates, Bootstrap
- **Database**: SQLite (default), MySQL (optional upgrade)
- **Containerization**: Docker
- **CI/CD & Deployment**: DockerHub-ready with `deployment.yml`

---

## 🚀 Key Features

- 🎵 Manage concert entries (name, location, date, duration)
- 📸 Upload photos and list them dynamically
- 🎶 Songs module with CRUD operations
- 🛠️ Django admin site for backend management
- 🔐 Built-in user authentication
- 🗃️ SQLite to MySQL data migration support
- 🐳 Dockerfile + `deployment.yml` for containerization

---

## 🔧 Getting Started

### Clone and Setup

```bash
git clone https://github.com/Silvafox76/Back-end-Development-Capstone.git
cd Back-end-Development-Capstone
pip install -r requirements.txt
Start the Server
bash
Copy
Edit
python manage.py runserver
Visit http://localhost:8000 to view the app.

⚙️ Admin Access
bash
Copy
Edit
python manage.py createsuperuser
# Recommended:
# username: admin
# password: qwerty123 (or your own)
Visit http://localhost:8000/admin/ to log in.

🗄️ Migrations
bash
Copy
Edit
python manage.py makemigrations
python manage.py migrate
To move from SQLite to MySQL:

bash
Copy
Edit
python manage.py dumpdata > datadump.json
# Update database settings in settings.py
python manage.py loaddata datadump.json
🐳 Docker Support
bash
Copy
Edit
docker build -t concert:v1 .
docker run -p 8000:8000 concert:v1
🧪 Testing & Cleanup
bash
Copy
Edit
# Cleanup old migrations during dev:
find . -path "*/migrations/*.py" -not -name "__init__.py" -delete
find . -path "*/migrations/*.pyc" -delete
find . -path "*/db.sqlite3" -delete
📁 Project Structure
csharp
Copy
Edit
├── concert/             # Core Django app
├── static/              # Static files (CSS, JS)
├── templates/           # HTML templates
├── Dockerfile           # Docker configuration
├── deployment.yml       # Deployment setup
├── manage.py            # Django entry point
└── requirements.txt     # Dependencies
