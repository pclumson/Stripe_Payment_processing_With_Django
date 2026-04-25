# Stripe_Payment_processing_With_Django
 implementing a Payment Gateway like Stripe that accepts debit or credit card payments with Django

# Secure Django E-Commerce Platform with Stripe Integration

A production-ready demonstration of a scalable e-commerce backend built with Django, featuring secure payment processing, inventory management, and event-driven architecture.

## 🚀 Key Features
- **Secure Payments:** Full integration with Stripe Checkout and Webhooks (handling `session.completed`, `payment_intent.succeeded`).
- **Inventory Safety:** Atomic database updates using Django ORM `F()` expressions to prevent race conditions during high-concurrency sales.
- **Session-Based Cart:** Efficient cart management with automatic merging upon user login.
- **Order Lifecycle:** Complete state machine for orders (Pending -> Paid -> Shipped).
- **DevOps Ready:** Dockerized environment with PostgreSQL and Redis; includes GitHub Actions for automated testing.
- **Security:** CSRF protection, Stripe signature verification, and environment variable management.

## 🛠 Tech Stack
- **Backend:** Python 3.11, Django 5.0
- **Database:** PostgreSQL
- **Payments:** Stripe API (Checkout & Webhooks)
- **Infrastructure:** Docker, Docker Compose
- **Testing:** Pytest, Coverage.py

## 📂 Architecture Highlights
1. **Microservice-Ready:** Modular app structure (`products`, `cart`, `checkout`, `orders`) allows for easy separation into microservices.
2. **Event-Driven:** Webhook listeners trigger downstream actions (email notifications, inventory deduction) asynchronously.
3. **Scalability:** Stateless design allows for horizontal scaling behind a load balancer.

## 🏃 Quick Start
```bash
# Clone and setup
git clone https://github.com/pclumson/Stripe_Payment_processing_With_Django.git
cd Stripe_Payment_processing_With_Django

# Run with Docker
docker-compose up --build

# Access the app
# Frontend/Admin: http://localhost:8000/admin
# API Docs: http://localhost:8000/api/docs
