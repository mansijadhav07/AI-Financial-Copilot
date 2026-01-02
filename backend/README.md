# Backend – AI Financial Copilot

This folder contains the backend services for the **AI Financial Copilot** project.

The backend is responsible for data management, decision-making logic, and integration with machine learning models and AI services. It acts as the central orchestration layer between the frontend and the intelligence components.

---

## 🧩 Responsibilities

- User authentication and authorization
- Transaction ingestion and validation
- Financial decision engine (rules + ML models)
- Insight generation and orchestration
- API layer for frontend communication
- Data persistence and aggregation

---

## 🏗️ Architecture Overview

The backend follows a modular, layered architecture:

- **API Layer** – Request handling and routing
- **Service Layer** – Business logic and orchestration
- **Decision Engine** – Rules, ML models, and metrics
- **Data Layer** – Persistent storage and caching
- **AI Explanation Layer** – Converts decisions into user-friendly explanations

---

## 🛠️ Tech Stack

- **Framework**: FastAPI
- **Language**: Python
- **Authentication**: JWT (planned)
- **Database**: PostgreSQL (planned)
- **Caching**: Redis (optional)
- **Machine Learning**: Scikit-learn, Pandas, NumPy
- **AI Integration**: LLM (used only for explanation)

---

## 📁 Folder Structure

```text
backend/
├── app/
│ ├── api/ # API routes
│ ├── core/ # Configurations and security
│ ├── models/ # Database models
│ ├── services/ # Business logic
│ ├── rules/ # Rule-based decision logic
│ ├── ml/ # Machine learning models
│ └── main.py # FastAPI app entry point
│
├── requirements.txt
└── README.md


---

## 🔁 Request Flow (High Level)

1. Frontend sends request to backend API
2. API layer validates and routes the request
3. Services process business logic
4. Decision engine evaluates rules and ML signals
5. Insights are generated and optionally explained using AI
6. Response is sent back to the frontend

---

## 🔐 Security & Data Handling

- Sensitive financial data is never exposed to AI models
- Only aggregated data is passed to the explanation layer
- Input validation is enforced at API boundaries
- User data deletion will be supported
