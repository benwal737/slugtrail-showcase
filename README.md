# SlugTrail 🐌

**Award:** 🏆 First Place, UCSC Senior Capstone Competition (December 2025)

> **Note:** Source code is private per university policy. This repository contains project documentation, architecture overview, and technical details.

---

## Overview

SlugTrail is a distributed parking management system designed for the UCSC campus. The platform provides real-time parking availability tracking, intelligent route optimization, and AI-powered customer support to solve UCSC's chronic parking congestion problem.

**Problem:** UCSC students waste 15-30 minutes finding parking during peak hours, leading to missed classes and frustration.

**Solution:** Real-time parking availability system with predictive analytics and turn-by-turn navigation to open spots.

---

## Tech Stack

### Frontend
- **Next.js** - React framework for server-side rendering
- **TypeScript** - Type-safe development
- **Tailwind CSS** - Responsive UI styling

### Backend
- **Node.js** - Runtime environment
- **Express** - API routing and middleware
- **TypeScript** - Backend type safety
- **PostgreSQL** - Primary database
- **Docker** - Containerization for all 9 microservices

### AI Integration
- **OpenAI GPT-4** - Natural language processing for chatbot
- **Google Gemini** - Fallback AI service and specialized queries
- **Custom AI orchestration** - Handles response latency and API failover

### Infrastructure
- **9 Microservices Architecture** - Each service handles a specific domain
- **WebSockets** - Real-time parking updates
- **RESTful APIs** - Service-to-service communication

---

## System Architecture

### Microservices Breakdown

1. **Authentication Service** - User login, registration, JWT tokens
2. **Parking Availability Service** - Real-time lot occupancy tracking
3. **Route Optimization Service** - Shortest path calculation to available spots
4. **Notification Service** - Push notifications for spot availability
5. **Payment Processing Service** - Parking permit validation
6. **Admin Dashboard Service** - Management interface for parking operations
7. **Driver Mobile Service** - Mobile-optimized driver interface
8. **AI Chatbot Service** - Customer support automation (OpenAI + Gemini)
9. **Analytics Service** - Usage patterns and parking predictions

### Data Flow
