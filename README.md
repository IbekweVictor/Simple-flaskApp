# 🚀 Simple Flask App

A minimal **Flask web application** with HTML templates, static styling, Docker support, and CI/CD integration via Jenkins.

## 📂 Project Structure

```
.
├── main.py                # Flask application entry point
├── templates/             # HTML templates (Jinja2)
│   ├── index.html
│   └── hello.html
├── static/css/            # Static assets (CSS)
│   └── style.css
├── requirements.txt       # Python dependencies
├── Dockerfile             # Docker build file
├── docker-compose.yaml    # Docker Compose configuration
├── jenkinsfile            # Jenkins pipeline definition
├── .gitignore             # Git ignore file
└── README.md              # Project documentation
```

---

## ⚙️ Installation & Setup

### 🔹 1. Clone the repository

```bash
git clone https://github.com/IbekweVictor/Simple-flaskApp.git
cd Simple-flaskApp
```

### 🔹 2. Create a virtual environment

```bash
python -m venv venv
source venv/bin/activate    # On Linux/Mac
venv\Scripts\activate       # On Windows
```

### 🔹 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 🔹 4. Run the app

```bash
python main.py
```

App will run at **[http://127.0.0.1:5000/](http://127.0.0.1:5000/)**.

---

## 🐳 Run with Docker

### Build the image

```bash
docker build -t simple-flask-app .
```

### Run the container

```bash
docker run -p 5000:5000 simple-flask-app
```

### Or with Docker Compose

```bash
docker-compose up --build
```

---

## 🔄 CI/CD with Jenkins

This project includes a **Jenkinsfile** for pipeline automation:

* Checkout code
* Install dependencies
* Run tests (if added)
* Build Docker image
* Deploy container

---

## 🎨 UI

* Basic HTML pages in `templates/`
* Styled with `static/css/style.css`

---

## 📌 Requirements

* Python 3.8+
* Flask
* Docker (optional for containerization)
* Jenkins (optional for CI/CD)

---

## 🤝 Contributing

1. Fork this repo
2. Create a feature branch (`git checkout -b feature-name`)
3. Commit changes (`git commit -m "Added feature"`)
4. Push to your fork and open a PR

---

## 📜 License

This project is licensed under the **MIT License** – feel free to use and modify.
