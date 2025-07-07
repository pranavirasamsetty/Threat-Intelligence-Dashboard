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
git clone https://github.com/pranavirasamsetty/Threat-Intelligence-Dashboard.git
cd Threat-Intelligence-Dashboard
```

### 2. Download CSV dataset from Kaggle
- Dataset link: https://www.kaggle.com/datasets/hussainsheikh03/nlp-based-cyber-security-dataset
- Download and rename the CSV to `threat-data.csv`
- Place it inside the `backend/` folder

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
- `GET /api/threats`
- `GET /api/threats/:id`
- `GET /api/threats/stats`
- `POST /api/analyze` (Payload: `{ "description": "some text" }`)

## 👨‍💻 Author
Pranavi Rasamsetty
