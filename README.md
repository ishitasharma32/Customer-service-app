# AI-Powered Customer Service Platform

An intelligent customer service platform that automates query handling, ticket management, and feature request prioritization using AI.

## 🌟 Features

- AI-powered customer query analysis and classification
- Automated JIRA ticket creation and management
- Smart feature request prioritization based on client metrics
- Intelligent ticket assignment to engineers
- Real-time chat interface for customer support
- Analytics dashboard for tracking system performance

## 🛠 Tech Stack

### Frontend
- React.js with TypeScript
- Redux for state management
- Tailwind CSS for styling
- Socket.io-client for real-time communication
- Chart.js for analytics visualization

### Backend
- FastAPI (Python)
- SQLAlchemy for database management
- Transformers library for NLP
- JIRA API integration
- PostgreSQL database
- Redis for caching

### ML Components
- HuggingFace Transformers
- Sentiment Analysis
- Zero-shot Classification

## 📁 Project Structure
flowchart TD
    subgraph Frontend
        A[React App] --> B[Components]
        B --> B1[Dashboard]
        B --> B2[TicketForm]
        B --> B3[ChatInterface]
        A --> C[Redux Store]
        A --> D[API Services]
    end
    
    subgraph Backend
        E[FastAPI Server] --> F[Routes]
        E --> G[ML Models]
        E --> H[Services]
        H --> H1[JIRA Service]
        H --> H2[Chat Service]
        H --> H3[Ticket Service]
        E --> I[Database]
    end
    
    D <-->|REST API| E

```
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── services/
│   │   ├── store/
│   │   └── types/
│   ├── public/
│   └── package.json
├── backend/
│   ├── app/
│   │   ├── api/
│   │   ├── core/
│   │   ├── models/
│   │   └── services/
│   ├── tests/
│   └── requirements.txt
├── ml_models/
│   ├── training/
│   └── inference/
└── docker/
    ├── frontend.Dockerfile
    └── backend.Dockerfile
```

## 🚀 Getting Started

### Prerequisites
- Python 3.9+
- Node.js 16+
- Docker and Docker Compose
- JIRA API credentials
- PostgreSQL

### Installation

1. Clone the repository
```bash
git clone https://github.com/yourusername/customer-service-platform.git
cd customer-service-platform
```

2. Set up backend
```bash
cd backend
python -m venv venv
source venv/bin/activate  # On Windows: .\venv\Scripts\activate
pip install -r requirements.txt
```

3. Set up frontend
```bash
cd frontend
npm install
```

4. Create environment files
```bash
# Backend (.env)
DATABASE_URL=postgresql://user:password@localhost:5432/dbname
JIRA_API_TOKEN=your_token
JIRA_SERVER=your_server
MODEL_PATH=path_to_models

# Frontend (.env)
REACT_APP_API_URL=http://localhost:8000
```

5. Start the application
```bash
# Start backend
cd backend
uvicorn app.main:app --reload

# Start frontend
cd frontend
npm start
```

## 🌐 API Documentation

The API documentation is available at `http://localhost:8000/docs` when running the backend server.

### Key Endpoints
- POST `/api/queries` - Submit customer query
- GET `/api/tickets` - Get all tickets
- POST `/api/tickets/{id}/assign` - Assign ticket to engineer
- GET `/api/analytics` - Get system analytics

## 🧪 Testing

```bash
# Backend tests
cd backend
pytest

# Frontend tests
cd frontend
npm test
```

## 📦 Deployment

### Using Docker
```bash
docker-compose up --build
```

### Manual Deployment
1. Build frontend
```bash
cd frontend
npm run build
```

2. Set up backend server
```bash
cd backend
gunicorn app.main:app
```

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.# Customer-service-app
