<div align="center">

# ✈️ TraviqueYou

**AI-powered travel planning platform with an intelligent assistant, RAG-based recommendations, and full async infrastructure — built solo, end to end.**

[![Live Backend](https://img.shields.io/badge/Backend-Railway-6366f1?style=flat-square&logo=railway)](https://railway.app)
[![Live Frontend](https://img.shields.io/badge/Frontend-Netlify-00C7B7?style=flat-square&logo=netlify)](https://netlify.com)
[![Django](https://img.shields.io/badge/Django-5.x-092E20?style=flat-square&logo=django)](https://djangoproject.com)
[![React](https://img.shields.io/badge/React-18-61DAFB?style=flat-square&logo=react)](https://reactjs.org)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL+pgvector-blue?style=flat-square&logo=postgresql)](https://postgresql.org)
[![Docker](https://img.shields.io/badge/Docker-Compose-2496ED?style=flat-square&logo=docker)](https://docker.com)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)

[Live Demo](#) · [API Docs](#api-documentation) · [Report Bug](https://github.com/monikanimmana/traviqueyou/issues)

</div>

---

## About

TraviqueYou is a full-stack AI travel planning platform I built from scratch as a solo project. The core feature is **Shiro** — an AI assistant powered by Google Gemini and Retrieval-Augmented Generation (RAG) via pgvector — which gives personalised travel recommendations based on user preferences and conversation history.

The platform covers the full lifecycle of trip planning: destination discovery, itinerary building, bookings, reviews, and async notifications — across 9 modules and 12 database tables, with a containerised deployment on Railway (backend) and Netlify (frontend).

---

## Features

- **Shiro AI Assistant** — Gemini-powered conversational travel assistant with RAG via pgvector for context-aware, personalised recommendations
- **JWT Authentication** — Secure access and refresh token flow using Django SimpleJWT
- **Async Task Processing** — Celery + Redis for background jobs: email notifications, embedding generation, scheduled tasks
- **Trip & Itinerary Builder** — Day-by-day itinerary planning with destinations, activities, and notes
- **Bookings & Reviews** — End-to-end booking management and review system
- **Destination Discovery** — Searchable destination catalogue with tags and filters
- **Notifications** — Real-time and async notification delivery
- **Docker Compose** — Full local dev environment with one command
- **Production Deployment** — Railway (API) + Netlify (frontend), environment-split Django settings

---

## Tech Stack

| Layer | Technology |
|---|---|
| **Backend** | Django 5, Django REST Framework, Gunicorn |
| **Frontend** | React 18, Tailwind CSS, Vite |
| **AI / RAG** | Google Gemini API, pgvector, custom embedding pipeline |
| **Database** | PostgreSQL + pgvector extension |
| **Async** | Celery, Redis, Celery Beat |
| **Auth** | JWT (djangorestframework-simplejwt) |
| **Containerisation** | Docker, Docker Compose |
| **Deployment** | Railway (backend), Netlify (frontend) |
| **Dev Tools** | Postman, GitHub, python-decouple |

---

## Project Structure

```
traviqueyou-backend/
├── config/
│   ├── settings/
│   │   ├── base.py
│   │   ├── development.py
│   │   └── production.py
│   ├── urls.py
│   └── wsgi.py
├── apps/
│   ├── accounts/          # User registration, login, JWT
│   ├── trips/             # Trip creation and management
│   ├── shiro/             # AI assistant: RAG engine, embeddings, Gemini client
│   ├── itinerary/         # Day-by-day itinerary builder
│   ├── destinations/      # Destination catalogue
│   ├── bookings/          # Booking management
│   ├── reviews/           # Reviews and ratings
│   ├── payments/          # Payment records
│   └── notifications/     # Async notification delivery
├── core/                  # Shared: permissions, pagination, exceptions, utils
├── celery/                # Celery config and beat schedule
├── tests/
├── manage.py
├── Dockerfile
├── docker-compose.yml
└── requirements.txt

traviqueyou-frontend/
├── src/
│   ├── components/
│   │   ├── ui/            # Button, Card, Modal, Input
│   │   ├── layout/        # Navbar, Footer, Sidebar
│   │   └── shiro/         # AI chat widget
│   ├── pages/             # Home, Explore, TripDetail, Itinerary, Profile, Bookings
│   ├── hooks/             # useAuth, useTrips, useShiro
│   ├── services/          # API layer: api.js, auth.js, shiro.js
│   ├── store/             # State management
│   └── utils/
├── tailwind.config.js
└── vite.config.js
```

---

## Database Schema (12 tables)

`users` · `profiles` · `destinations` · `trips` · `itinerary_days` · `bookings` · `reviews` · `payments` · `notifications` · `shiro_chats` · `embeddings` · `tags`

---

## How Shiro Works (RAG Pipeline)

```
User message
     │
     ▼
Embed query (Gemini embedding model)
     │
     ▼
pgvector similarity search → retrieve top-K relevant documents
     │
     ▼
Build prompt: [system context] + [retrieved docs] + [user message]
     │
     ▼
Gemini generates personalised response
     │
     ▼
Response + conversation saved to shiro_chats
```

---

## Getting Started

### Prerequisites

- Python 3.11+
- Node.js 18+
- Docker & Docker Compose
- PostgreSQL with pgvector extension (or use Docker Compose — included)

### 1. Clone the repo

```bash
git clone https://github.com/monikanimmana/traviqueyou.git
cd traviqueyou
```

### 2. Backend setup

```bash
cd traviqueyou-backend
cp .env.example .env
# Fill in your values: SECRET_KEY, DATABASE_URL, GEMINI_API_KEY, REDIS_URL
```

**With Docker Compose (recommended):**

```bash
docker-compose up --build
```

This starts: Django API · PostgreSQL + pgvector · Redis · Celery worker · Celery Beat

**Without Docker:**

```bash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

### 3. Frontend setup

```bash
cd traviqueyou-frontend
npm install
cp .env.example .env.local
# Set VITE_API_URL=http://localhost:8000
npm run dev
```

### 4. Run Celery (if not using Docker)

```bash
celery -A config worker --loglevel=info
celery -A config beat --loglevel=info
```

---

## Environment Variables

```env
# Django
SECRET_KEY=your-secret-key
DEBUG=True
ALLOWED_HOSTS=localhost,127.0.0.1

# Database
DATABASE_URL=postgresql://user:password@localhost:5432/traviqueyou

# Redis
REDIS_URL=redis://localhost:6379/0

# Gemini AI
GEMINI_API_KEY=your-gemini-api-key

# JWT
ACCESS_TOKEN_LIFETIME=60        # minutes
REFRESH_TOKEN_LIFETIME=7        # days
```

---

## API Documentation

Base URL: `https://your-railway-url.up.railway.app/api/`

| Endpoint | Method | Description |
|---|---|---|
| `/auth/register/` | POST | User registration |
| `/auth/login/` | POST | JWT token obtain |
| `/auth/refresh/` | POST | Refresh access token |
| `/trips/` | GET, POST | List / create trips |
| `/trips/<id>/` | GET, PUT, DELETE | Trip detail |
| `/itinerary/<trip_id>/` | GET, POST | Itinerary for a trip |
| `/destinations/` | GET | Browse destinations |
| `/bookings/` | GET, POST | Bookings |
| `/reviews/` | GET, POST | Reviews |
| `/shiro/chat/` | POST | Chat with Shiro AI |
| `/notifications/` | GET | User notifications |

> Full Postman collection available on request.

---

## Deployment

| Service | Platform | Notes |
|---|---|---|
| Django API | Railway | `Procfile`: `web: gunicorn config.wsgi` |
| PostgreSQL | Railway | pgvector extension enabled |
| Redis | Railway | Shared instance for cache + Celery |
| React Frontend | Netlify | Build: `npm run build`, publish: `dist/` |

---

## What I Learned

- Designing and implementing a full RAG pipeline from scratch (embedding → vector search → prompt construction → LLM response)
- Managing async task queues with Celery + Redis across multiple worker types
- Structuring a production-grade Django project with environment-split settings and DRF serializers
- Containerising a multi-service backend with Docker Compose
- Building a React frontend with a clean service layer and custom hooks

---

## Author

**Monika Nimmana**
Final-year B.Tech CSE · Parul University, Vadodara

[![GitHub](https://img.shields.io/badge/GitHub-monikanimmana-181717?style=flat-square&logo=github)](https://github.com/monikanimmana)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-monika--nimmana-0A66C2?style=flat-square&logo=linkedin)](https://linkedin.com/in/monika-nimmana)

---

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
