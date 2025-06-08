# 🧩 FastAPI + MongoDB Todo App

This is a simple Todo API built using **FastAPI**, **MongoDB**, and **Uvicorn**. It supports retrieving and creating todo tasks.

---

## 🚀 Features

- ✅ Create new todo tasks
- 📋 Fetch all saved tasks from MongoDB
- 🌐 FastAPI backend with async routes
- ☁️ Connects to MongoDB Atlas using \`pymongo\`

---

## 📦 Installation

### 1. Clone the repository

```
git clone https://github.com/arabinda0704/Todo_Using_FastAPI.git
```

### 2. Create a virtual environment (optional but recommended)

```
python -m venv venv
source venv/bin/activate  # On Windows: venv\\Scripts\\activate
```

### 3. Install dependencies

```
pip install fastapi uvicorn pymongo dnspython
```

---

## ⚙️ MongoDB Configuration

1. Create a file named \`configurations.py\` (this should be in \`.gitignore\`).
2. Add your MongoDB URI and define the collection:

```python
from pymongo.mongo_client import MongoClient
from pymongo.server_api import ServerApi

uri = \"mongodb+srv://<username>:<password>@yourcluster.mongodb.net/?retryWrites=true&w=majority\"
client = MongoClient(uri, server_api=ServerApi('1'))
db = client.todo_db
collection = db[\"todo_data\"]
```

---

## ▶️ Run the FastAPI app

```
uvicorn main:app --reload
```

Visit: [http://127.0.0.1:8000](http://127.0.0.1:8000)

FastAPI's built-in Swagger UI is available at:
- [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)

---

## 📂 Project Structure

```
FastApi-Project/
│
├── main.py
├── configurations.py       # MongoDB URI and collection setup (gitignored)
├── database/
│   ├── models.py           # Pydantic models
│   └── schemas.py          # Response formatting functions
├── venv/                   # Virtual environment (gitignored)
├── .gitignore
└── README.md
```

---

## 📌 Notes

- Never push \`configurations.py\` or your MongoDB credentials to GitHub.
- Use environment variables or \`.env\` for secrets in production.

---

## 📫 Contact

Created by [Arabinda Das](mailto:7arabinda@gmail.com) – feel free to reach out!
" 
