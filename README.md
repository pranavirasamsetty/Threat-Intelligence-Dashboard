# Threat Intelligence Dashboard

## 📦 Stack
- Backend: Python (Flask)
- Frontend: React + Vite
- Database: PostgreSQL
- ML: Scikit-learn (Logistic Regression + TF-IDF)
- DevOps: Docker, Docker Compose

## 🚀 Setup Instructions

### 1. Clone the repository
```bash
git clone <your-repo-url>
cd threat-intelligence-dashboard
```

### 2. Add CSV dataset
Place the Kaggle dataset CSV (`threat-data.csv`) into `backend/`

### 3. Train ML model
```bash
cd backend
python model/train_model.py
```

### 4. Build and run app
```bash
docker-compose up --build
```

### 5. Open in browser
- Frontend: http://localhost:3000
- Backend API: http://localhost:5000/api/threats

## 🧪 Test Endpoints
- `/api/threats`
- `/api/threats/:id`
- `/api/threats/stats`
- `/api/analyze` (POST: `{ "description": "some text" }`)

## 👨‍💻 Author
Pranavi Rasamsetty
