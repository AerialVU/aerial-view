# 🚁 Aerial View - Drone Footage Sales Platform

A modern, full-stack web application for selling drone footage and aerial photography. Built with Next.js, Express, PostgreSQL, and Stripe integration.

## 🌟 Features

- 📹 **Product Showcase** - Beautiful gallery of drone footage
- 🛒 **E-Commerce** - Shopping cart and checkout
- 💳 **Payments** - Stripe integration for secure transactions
- 👤 **User Accounts** - Customer registration and order history
- 🔐 **Authentication** - JWT-based auth system
- 📱 **Responsive Design** - Mobile, tablet, and desktop support
- 🌙 **Dark Theme** - Modern UI with Tailwind CSS
- 🐳 **Docker Ready** - Easy setup with Docker Compose

## 🏗️ Tech Stack

### Frontend
- **Next.js 14** - React framework
- **Tailwind CSS** - Styling
- **Stripe.js** - Payment integration

### Backend
- **Express.js** - Node.js API framework
- **PostgreSQL** - Database
- **Prisma** - ORM for database
- **JWT** - Authentication
- **Stripe API** - Payment processing

### DevOps
- **Docker & Docker Compose** - Containerization

## 🚀 Quick Start

### Prerequisites
- Node.js 18+
- Docker & Docker Compose
- Git

### 1. Clone Repository
```bash
git clone https://github.com/AerialVU/aerial-view.git
cd aerial-view
```

### 2. Start Docker Services
```bash
docker-compose up -d
```

### 3. Setup Backend
```bash
cd backend
npm install
cp .env.example .env
```

Update `.env`:
```env
DATABASE_URL="postgresql://aerial:aerial123@localhost:5432/aerial_view"
JWT_SECRET="your-secret-key-here"
STRIPE_SECRET_KEY="sk_test_..."
STRIPE_WEBHOOK_SECRET="whsec_..."
PORT=5000
```

Run migrations:
```bash
npx prisma migrate dev --name init
```

Start backend:
```bash
npm run dev
```

### 4. Setup Frontend
```bash
cd ../frontend
npm install
cp .env.example .env.local
```

Update `.env.local`:
```env
NEXT_PUBLIC_API_URL="http://localhost:5000"
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY="pk_test_..."
```

Start frontend:
```bash
npm run dev
```

Visit `http://localhost:3000` 🎉

## 💳 Stripe Setup

1. Create account at [stripe.com](https://stripe.com)
2. Get API keys from [Developers → API Keys](https://dashboard.stripe.com/apikeys)
3. Add to `.env` files
4. Setup webhooks endpoint: `http://localhost:5000/api/webhooks/stripe`

## 📝 License

MIT License - feel free to use this for your business!

---

**Built with ❤️ for drone pilots and aerial photographers**
