#  Movie Watchlist API & Web Client

A full-stack Movie Watchlist application built using **Go (Gin)** for the backend and **Vanilla JavaScript** for the frontend.

The system integrates with the OMDB API, supports movie search, caching, user watchlists, rating management, and RESTful CRUD operations.

---

## Architecture Overview

Frontend (HTML + JS)
        ↓
Gin REST API (Go)
        ↓
External OMDB API
        ↓
SQLite (Persistent Storage)

---

##  Tech Stack

### Backend
- Go 1.x
- Gin Web Framework
- RESTful API design
- OMDB API integration
- SQLite database
- CORS middleware

### Frontend
- HTML5
- CSS3
- Vanilla JavaScript
- Fetch API

---

## 📦 Core Features

### 1️⃣ Movie Search
- Calls OMDB API
- Returns normalized JSON response
- Handles error states (400, 500)

### 2️⃣ Movie Caching
- Movies stored locally in SQLite
- Reduces repeated external API calls
- Improves performance

### 3️⃣ Watchlist Management
- Add movie to watchlist
- Update status (WATCHLIST / WATCHED)
- Add user rating (1–5)
- Retrieve user watchlist

### 4️⃣ RESTful API Design
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/movies/search?q=` | Search movies |
| GET | `/movies/:imdbID` | Get movie details |
| POST | `/users` | Create user |
| POST | `/watchlist` | Add movie to watchlist |
| GET | `/users/:id/watchlist` | Get user watchlist |
| PUT | `/watchlist/:id` | Update watchlist entry |


