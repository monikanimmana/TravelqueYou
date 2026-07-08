<div align="center">

<img src="https://img.shields.io/badge/TraviqueYou-AI%20Travel%20Platform-FF6B35?style=for-the-badge&logoColor=white" alt="TraviqueYou"/>

<br/>
<br/>

**AI-powered travel planning platform — built solo, end to end.**
<br/>
*Plan trips, build itineraries, manage budgets, and chat with Shiro — your personal AI travel companion.*

<br/>

[![Django](https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white)](https://djangoproject.com)
[![DRF](https://img.shields.io/badge/Django_REST_Framework-092E20?style=flat-square&logo=django&logoColor=white)](https://django-rest-framework.org)
[![React](https://img.shields.io/badge/React_18-20232A?style=flat-square&logo=react&logoColor=61DAFB)](https://reactjs.org)
[![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white)](https://tailwindcss.com)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white)](https://postgresql.org)
[![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)](https://redis.io)
[![Celery](https://img.shields.io/badge/Celery-37814A?style=flat-square&logo=celery&logoColor=white)](https://docs.celeryq.dev)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)](https://docker.com)
[![Google Gemini](https://img.shields.io/badge/Google_Gemini-4285F4?style=flat-square&logo=google&logoColor=white)](https://ai.google.dev)
[![Railway](https://img.shields.io/badge/Railway-0B0D0E?style=flat-square&logo=railway&logoColor=white)](https://railway.app)
[![Netlify](https://img.shields.io/badge/Netlify-00C7B7?style=flat-square&logo=netlify&logoColor=white)](https://netlify.com)
[![JWT](https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white)](https://jwt.io)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)

<br/>

[🚀 Live Demo](#) &nbsp;·&nbsp; [📖 API Docs](#api-documentation) &nbsp;·&nbsp; [🐛 Report Bug](https://github.com/monikanimmana/traviqueyou/issues) &nbsp;·&nbsp; [💡 Request Feature](https://github.com/monikanimmana/traviqueyou/issues)

</div>

---

## 📸 Screenshots

### Dashboard
![Dashboard](screenshot_dashboard.png)

### My Trips
![My Trips](screenshot_mytrips.png)

### Destinations — Explore the World
![Destinations](screenshot_destinations.png)

### Itinerary Builder
![Itinerary](screenshot_itinerary.png)

### Budget Tracker
![Budget](screenshot_budget.png)

### Shiro — AI Travel Companion
![Shiro AI](screenshot_shiro.png)

### Packing Checklist
![Packing](screenshot_packing.png)

---

## 🧭 About

**TraviqueYou** is a full-stack AI travel planning platform built from scratch as a solo project. The highlight is **Shiro** — an AI assistant powered by Google Gemini and Retrieval-Augmented Generation (RAG) via `pgvector` — that gives personalised travel recommendations based on your preferences and conversation history.

The platform covers the full lifecycle of trip planning: destination discovery, itinerary building, budget tracking, packing checklists, bookings, and async notifications — across **9 modules** and **12 database tables**, containerised with Docker Compose and deployed on Railway (backend) + Netlify (frontend).

> Built entirely solo. No team. No boilerplate starter kits. Every layer — from the RAG pipeline to the React frontend — was designed, coded, and deployed by me.

---

## ✨ Features

| Module | What it does |
|---|---|
| 🤖 **Shiro AI** | Gemini-powered assistant with RAG via pgvector for context-aware trip recommendations |
| ✈️ **My Trips** | Create and manage trips with status tracking (Planned / Ongoing / Completed) |
| 🗺️ **Destinations** | Browse 500+ destinations by category with AI-curated suggestions |
| 📅 **Itinerary Builder** | Day-by-day itinerary with activities, times, and location stops |
| 💰 **Budget Tracker** | Real-time budget tracking with category breakdown and currency converter |
| 🎒 **Packing Checklist** | Smart packing lists with progress tracking by category |
| 🔔 **Notifications** | Async notification delivery via Celery + Redis |
| 🔐 **JWT Auth** | Secure access/refresh token flow (Django SimpleJWT) |
| 🐳 **Docker Compose** | Full local dev environment with one command |

---

## 🛠️ Tech Stack

### Backend
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white)
![DRF](https://img.shields.io/badge/DRF-ff1709?style=flat-square&logo=django&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Celery](https://img.shields.io/badge/Celery-37814A?style=flat-square&logo=celery&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)

### Frontend
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Tailwind](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)

### Database & AI
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white)
![pgvector](https://img.shields.io/badge/pgvector-316192?style=flat-square&logo=postgresql&logoColor=white)
![Gemini](https://img.shields.io/badge/Google_Gemini-4285F4?style=flat-square&logo=google&logoColor=white)

### DevOps & Deployment
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Railway](https://img.shields.io/badge/Railway-0B0D0E?style=flat-square&logo=railway&logoColor=white)
![Netlify](https://img.shields.io/badge/Netlify-00C7B7?style=flat-square&logo=netlify&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white)

---

## 🤖 How Shiro Works (RAG Pipeline)

```
User message
     │
     ▼
Embed query  ──────────────────────────  Gemini Embedding Model
     │
     ▼
pgvector similarity search  ──────────  Top-K relevant docs retrieved
     │
     ▼
Prompt builder  ───────────────────────  [System context] + [Retrieved docs] + [User message]
     │
     ▼
Gemini generates response  ────────────  Personalised, context-aware answer
     │
     ▼
Save to shiro_chats  ──────────────────  Conversation history persisted
```

---

## 📁 Project Structure

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
│   ├── accounts/          # User auth, JWT, profiles
│   ├── trips/             # Trip creation & management
│   ├── shiro/             # RAG engine, embeddings, Gemini client
│   ├── itinerary/         # Day-by-day itinerary builder
│   ├── destinations/      # Destination catalogue & search
│   ├── bookings/          # Booking management
│   ├── reviews/           # Reviews & ratings
│   ├── payments/          # Payment records
│   └── notifications/     # Async notifications
├── core/                  # Shared: permissions, pagination, exceptions
├── celery/                # Celery config & beat schedule
├── tests/
├── Dockerfile
├── docker-compose.yml
└── requirements.txt

traviqueyou-frontend/
├── src/
│   ├── components/
│   │   ├── ui/            # Button, Card, Modal, Input
│   │   ├── layout/        # Navbar, Sidebar, Footer
│   │   └── shiro/         # AI chat widget
│   ├── pages/             # Dashboard, Trips, Destinations, Itinerary, Budget, Shiro, Packing
│   ├── hooks/             # useAuth, useTrips, useShiro
│   ├── services/          # api.js, auth.js, shiro.js
│   ├── store/             # State management
│   └── utils/
├── tailwind.config.js
└── vite.config.js
```

---

## 🗃️ Database Schema (12 tables)

`users` · `profiles` · `destinations` · `trips` · `itinerary_days` · `bookings` · `reviews` · `payments` · `notifications` · `shiro_chats` · `embeddings` · `tags`

---

## 🚀 Getting Started

### Prerequisites

- Python 3.11+
- Node.js 18+
- Docker & Docker Compose
- Google Gemini API key

### 1. Clone the repo

```bash
git clone https://github.com/monikanimmana/traviqueyou.git
cd traviqueyou
```

### 2. Backend — with Docker (recommended)

```bash
cd traviqueyou-backend
cp .env.example .env
# Fill in: SECRET_KEY, DATABASE_URL, GEMINI_API_KEY, REDIS_URL

docker-compose up --build
```

This starts: Django API · PostgreSQL + pgvector · Redis · Celery worker · Celery Beat

### 3. Backend — without Docker

```bash
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

### 4. Frontend

```bash
cd traviqueyou-frontend
npm install
cp .env.example .env.local
# Set: VITE_API_URL=http://localhost:8000
npm run dev
```

### 5. Celery (if not using Docker)

```bash
celery -A config worker --loglevel=info
celery -A config beat --loglevel=info
```

---

## 🔑 Environment Variables

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

## 📡 API Documentation

Base URL: `https://your-railway-url.up.railway.app/api/`

| Endpoint | Method | Description |
|---|---|---|
| `/auth/register/` | POST | User registration |
| `/auth/login/` | POST | Obtain JWT tokens |
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

## ☁️ Deployment

| Service | Platform | Notes |
|---|---|---|
| Django API | Railway | `Procfile`: `web: gunicorn config.wsgi` |
| PostgreSQL + pgvector | Railway | pgvector extension enabled |
| Redis | Railway | Shared instance for cache + Celery |
| React Frontend | Netlify | Build: `npm run build`, publish: `dist/` |

---

## 🧠 What I Learned

- Designing and implementing a full RAG pipeline from scratch — embedding → vector search → prompt construction → LLM response
- Managing async task queues with Celery + Redis across multiple worker types
- Structuring a production-grade Django project with environment-split settings and DRF serializers
- Containerising a multi-service backend with Docker Compose
- Building a React frontend with a clean service layer and custom hooks
- Solo ownership of the complete product lifecycle: design → build → integrate AI → deploy

---

## 👩‍💻 Author

**Monika Nimmana**
*Final-year B.Tech CSE · Parul University, Vadodara*

[![GitHub](https://img.shields.io/badge/GitHub-monikanimmana-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/monikanimmana)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-monika--nimmana-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/monika-nimmana)

---

## 📄 License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

---

<div align="center">

*If this project helped you or you found it interesting, consider giving it a ⭐*

</div>
