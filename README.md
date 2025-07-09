Project Structure
threat-intelligence-dashboard/
├── backend/
│   ├── app.js
│   ├── package.json
│   ├── config/
│   │   └── database.js
│   ├── models/
│   │   ├── Threat.js
│   │   └── User.js
│   ├── routes/
│   │   ├── threats.js
│   │   ├── auth.js
│   │   └── analyze.js
│   ├── middleware/
│   │   └── auth.js
│   ├── scripts/
│   │   ├── ingest-data.js
│   │   └── train-model.py
│   ├── ml-models/
│   │   └── (generated model files)
│   ├── tests/
│   │   └── threats.test.js
│   └── Dockerfile
├── frontend/
│   ├── package.json
│   ├── src/
│   │   ├── App.js
│   │   ├── index.js
│   │   ├── components/
│   │   │   ├── Dashboard.js
│   │   │   ├── ThreatsView.js
│   │   │   ├── ThreatDetail.js
│   │   │   ├── AnalysisView.js
│   │   │   ├── Login.js
│   │   │   └── Navigation.js
│   │   ├── services/
│   │   │   └── api.js
│   │   └── styles/
│   │       └── App.css
│   └── Dockerfile
├── docker-compose.yml
├── README.md
└── .gitignore
