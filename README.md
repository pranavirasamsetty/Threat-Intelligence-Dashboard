# Threat-Intelligence-Dashboard
A full-stack web application that enables cybersecurity analysts to browse, search, filter, and analyze threat data efficiently. Built as part of the ConSecure Full Stack Engineering Assignment.

## Features Implemented

### Core Features (Part 1)
- ✅ Database schema design for threat data
- ✅ Data ingestion script for CSV processing
- ✅ RESTful API with pagination, filtering, and search
- ✅ Responsive React frontend with dashboard and threat views
- ✅ Statistics visualization

### Advanced Features (Part 2)
- ✅ Machine Learning integration with real-time threat classification
- ✅ Containerization with Docker and Docker Compose
- ✅ Automated testing (backend and frontend)
- ✅ User authentication with JWT
- ✅ WebSocket real-time updates

## Technology Stack

### Backend
- **Node.js + Express**: Fast, lightweight, excellent JSON handling
- **PostgreSQL**: Robust relational database for structured threat data
- **Python**: For ML model training and prediction

### Frontend
- **React**: Most popular SPA framework with excellent ecosystem
- **Material-UI**: Professional UI components
- **Chart.js**: Data visualization for statistics

### DevOps
- **Docker**: Containerization for easy deployment
- **Jest**: Testing framework
- **WebSockets**: Real-time updates

## Project Structure
```
threat-dashboard/
├── backend/
│   ├── src/
│   │   ├── controllers/
│   │   ├── models/
│   │   ├── routes/
│   │   ├── middleware/
│   │   └── utils/
│   ├── ml/
│   │   ├── train_model.py
│   │   └── predict.py
│   ├── scripts/
│   │   └── ingest_data.js
│   ├── tests/
│   └── package.json
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/
│   │   └── utils/
│   ├── public/
│   └── package.json
├── docker-compose.yml
└── README.md
```

## Setup Instructions

### Prerequisites
- Node.js (v16 or later)
- Python (v3.8 or later)
- PostgreSQL
- Docker and Docker Compose (optional)

### Quick Start with Docker
1. Clone the repository
2. Download the dataset from Kaggle and place `cybersecurity_threats.csv` in the root directory
3. Run with Docker Compose:
```bash
docker-compose up --build
```

### Manual Setup

#### 1. Database Setup
```bash
# Create PostgreSQL database
createdb threat_intelligence

# Set environment variables
export DB_HOST=localhost
export DB_PORT=5432
export DB_NAME=threat_intelligence
export DB_USER=your_username
export DB_PASSWORD=your_password
```

#### 2. Backend Setup
```bash
cd backend
npm install

# Install Python dependencies for ML
pip install -r requirements.txt

# Run data ingestion
node scripts/ingest_data.js

# Train ML model
python ml/train_model.py

# Start server
npm start
```

#### 3. Frontend Setup
```bash
cd frontend
npm install
npm start
```

### Running Tests
```bash
# Backend tests
cd backend
npm test

# Frontend tests
cd frontend
npm test
```

## API Endpoints

### Core Endpoints
- `GET /api/threats` - Paginated threat list with filtering and search
- `GET /api/threats/:id` - Single threat details
- `GET /api/threats/stats` - Dataset statistics

### Advanced Endpoints
- `POST /api/analyze` - ML-based threat classification
- `POST /api/auth/login` - User authentication
- `POST /api/auth/register` - User registration

### Query Parameters
- `page` - Page number for pagination
- `limit` - Items per page
- `category` - Filter by threat category
- `search` - Text search in threat descriptions

## Features

### Dashboard View
- Key statistics visualization
- Threat category distribution
- Severity score breakdown
- Live activity feed

### Threats View
- Paginated threat list
- Search and filter functionality
- Detailed threat information
- Export capabilities

### ML Analysis
- Real-time threat classification
- Prediction confidence scores
- Model performance metrics

## Architecture Decisions

1. **PostgreSQL over MongoDB**: Structured data with relationships benefits from SQL
2. **Express over other frameworks**: Lightweight and fast development
3. **React over Vue/Angular**: Largest ecosystem and community
4. **Docker Compose**: Simplified development environment setup
5. **JWT Authentication**: Stateless and scalable

## Performance Considerations
- Database indexing on frequently queried fields
- API response caching
- Pagination for large datasets
- Lazy loading for frontend components

## Security Features
- JWT-based authentication
- Input validation and sanitization
- SQL injection prevention
- XSS protection
- CORS configuration

## Deployment
The application is containerized and can be deployed on any Docker-compatible platform:
- AWS ECS/EKS
- Google Cloud Run
- Azure Container Instances
- Local Docker deployment


