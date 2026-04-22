# SlugTrail 🐌

**🏆 First Place, UCSC Senior Capstone Competition (December 2025)**

Full-stack parking management platform with 9 microservices, 3 client applications, and production deployment. Built for UCSC campus to solve chronic parking congestion through automated permit validation, real-time enforcement, and administrative oversight.

> **Note:** Source code is private per university policy. This repo documents architecture and implementation.

---

## Quick Stats

- **Architecture:** 9 independent microservices + 3 web apps
- **Databases:** 9 PostgreSQL instances (one per service)
- **APIs:** GraphQL for microservices, REST for external integrations
- **Test Coverage:** >99% (Vitest + React Testing Library)
- **Deployment:** Oracle Cloud with Docker + nginx
- **Timeline:** 7 weeks, 6-person team

---

## Tech Stack

**Frontend**
- Next.js, React, TypeScript
- Material-UI (MUI)
- NextAuth.js (Google OAuth)

**Backend**
- Node.js, Express, TypeScript
- GraphQL (microservices), REST (external APIs)
- PostgreSQL (9 databases)
- TSOA for OpenAPI docs

**Infrastructure**
- Docker (multi-stage builds)
- GitLab CI/CD
- Oracle Cloud Infrastructure
- Nginx (reverse proxy)

**Integrations**
- Stripe (payments)
- Brevo SMTP (emails)
- OCR API (license plate recognition)

---

## System Architecture

### 9 Microservices (GraphQL APIs)
1. Authentication - OAuth + JWT sessions
2. Member Management - User profiles
3. Permit Management - Purchase + renewal
4. Ticket Processing - Payment + contestation
5. Vehicle Registration - CRUD operations
6. Zone/Lot Management - Campus zones
7. Email Notifications - Transactional emails
8. Pricing - Dynamic calculations
9. Police/Registrar APIs - External agency integration

### 3 Client Applications
- **Driver** (port 3000) - Permit purchase, vehicle management, ticket payment
- **Enforcement** (port 3002) - Ticket issuance, permit validation, OCR scanning
- **Admin** (port 3001) - Analytics, enforcement management, zone configuration

Each microservice runs independently with its own PostgreSQL database and Docker container.

---

## Key Features

**For Drivers:**
- Google OAuth login with automatic session management
- Purchase and extend parking permits via Stripe
- Manage multiple vehicles
- Pay or contest parking tickets
- Email confirmations for all transactions

**For Enforcement:**
- Real-time permit validation
- Quick ticket issuance with OCR license plate scanning
- Zone-based enforcement workflows

**For Administrators:**
- System-wide analytics and revenue tracking
- Create and manage enforcement accounts
- Configure parking zones and pricing rules

---

## Technical Highlights

### Microservices Architecture
- 9 independent services, each with dedicated PostgreSQL database
- GraphQL APIs for efficient, type-safe data fetching
- Docker containerization for consistent deployment
- Services communicate via internal APIs

### Testing & Quality
- **>99% test coverage** using Vitest and React Testing Library
- MSW (Mock Service Worker) for API mocking
- GitLab CI/CD with automated testing on every commit
- ESLint + Prettier + Husky pre-commit hooks

### Production Deployment
- Docker multi-stage builds for optimized images
- Oracle Cloud Infrastructure hosting
- Nginx reverse proxy for frontend + API routing
- HTTPS termination and load balancing
- Automated deployment via GitLab CI/CD

### Authentication & Payments
- NextAuth.js with Google OAuth provider
- JWT-based session management
- Stripe Checkout integration with webhook handlers
- Automated email confirmations via Brevo SMTP

---

## My Contributions

As technical lead and backend architect:

**Architecture & Infrastructure:**
- Designed 9-microservice architecture with PostgreSQL-per-service pattern
- Built GraphQL APIs for all backend services
- Configured GitLab CI/CD pipeline with automated testing and deployment
- Deployed to Oracle Cloud with Docker + nginx

**Backend Development:**
- Implemented authentication service with NextAuth.js and Google OAuth
- Built permit management service with Stripe payment integration
- Created email notification service with Brevo SMTP relay
- Developed RESTful Police/Registrar APIs with TSOA

**Testing & DevOps:**
- Achieved >99% test coverage using Vitest and React Testing Library
- Set up Docker Compose for local development
- Configured nginx reverse proxy for production
- Implemented CI/CD pipeline with automated deployments

---

## Development

```bash
# Local development
npm run installs        # Install dependencies
npm run build-all       # Build all services
docker compose up       # Start all services

# Access applications
# Driver:      http://localhost:3000
# Admin:       http://localhost:3001  
# Enforcement: http://localhost:3002
```

**Service Ports:** Auth (8080), Member (8081), Permit (8082), Ticket (8083), Vehicle (8084), Zone (8085), Email (8086), Pricing (8087)

---

## Skills Demonstrated

- Full-stack development (Next.js, React, Node.js, PostgreSQL)
- Microservices architecture design
- GraphQL and RESTful API development
- CI/CD pipeline configuration
- Docker containerization
- Cloud deployment (Oracle Cloud)
- Payment processing (Stripe)
- OAuth authentication
- Test-driven development (>99% coverage)
- DevOps and infrastructure management

---

## Contact

**Ben Walderman**
- Portfolio: [benwalderman.vercel.app](https://benwalderman.vercel.app)
- GitHub: [@benwal737](https://github.com/benwal737)
- LinkedIn: [linkedin.com/in/benwalderman](https://linkedin.com/in/benwalderman)

---

*Source code is private per UCSC policy. Full technical documentation available upon request.*
