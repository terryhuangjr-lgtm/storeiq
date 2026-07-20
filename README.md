<h1 align="center">🏪 StoreIQ</h1>
<p align="center">
  <b>AI-Powered Inventory Intelligence for Multi-Location Shopify Brands</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Node.js-18.x-339933?logo=node.js" alt="Node.js"/>
  <img src="https://img.shields.io/badge/React-18-61DAFB?logo=react" alt="React"/>
  <img src="https://img.shields.io/badge/Supabase-FF4438?logo=supabase" alt="Supabase"/>
  <img src="https://img.shields.io/badge/Python-3.12-3776AB?logo=python" alt="Python"/>
  <img src="https://img.shields.io/badge/Vercel-000000?logo=vercel" alt="Vercel"/>
  <img src="https://img.shields.io/badge/Status-Production_Deployed-22c55e" alt="Status"/>
</p>

---

## 📋 The Problem

Multi-location Shopify brands struggle with inventory fragmentation. Each location operates independently, leading to:

- **Stockouts** at one store while another has excess
- **Manual transfer management** — slow, error-prone, costly
- **No real-time visibility** into inventory health across locations
- **Reactive ordering** — POs placed after stock is already gone

## 💡 The Solution

StoreIQ connects all locations into a single inventory intelligence layer. It monitors stock in real time across every variant, every location, and triggers automated actions before problems reach your customers.

**Built for a NYC fight gear brand** managing inventory across multiple retail locations.

---

## ✨ Key Features

| Feature | Description |
|---------|-------------|
| **Real-Time Threshold Monitoring** | Stock levels checked every cycle — alerts when configurable thresholds are breached |
| **Multi-Location Dashboard** | Web dashboard showing inventory health across all storefronts |
| **Automated Transfer Management** | Detects surplus at one location and deficit at another — generates transfer recommendations |
| **PO Generation** | Auto-creates purchase orders when inventory drops below reorder point |
| **Daily Telegram Digest** | Morning summary sent via Telegram — top inventory concerns, transfer recommendations, low-stock alerts |
| **Telegram AI Agent** | Ask about inventory, request reports, adjust thresholds — all via chat |

## 🧱 Architecture

```
┌──────────────┐     ┌──────────────┐     ┌──────────────┐
│  Shopify API  │────▶│  StoreIQ     │────▶│  Supabase    │
│  (REST)       │     │  Backend     │     │  (Postgres)  │
└──────────────┘     └──────┬───────┘     └──────────────┘
                            │
                    ┌───────┴────────┐
                    │                │
            ┌───────▼────┐   ┌──────▼──────┐
            │  Telegram   │   │  Vercel     │
            │  Agent+Bot  │   │  Dashboard  │
            └────────────┘   └─────────────┘
```

## 🛠 Tech Stack

- **Backend:** Node.js + Python
- **Database:** Supabase (PostgreSQL)
- **Frontend:** React + Tailwind CSS
- **Hosting:** Vercel
- **API Layer:** Shopify REST API
- **Notifications:** Telegram Bot API
- **Deployment:** DigitalOcean VPS

## 🚀 Status

**🟢 Production deployed** — actively monitoring inventory for a multi-location NYC apparel brand.

## 📸 Screenshots

*Screenshots coming soon — dashboard currently running in production.*

---

## 🏁 Getting Started

```bash
# Clone the repo
git clone https://github.com/terryhuangjr-lgtm/storeiq.git

# Install backend dependencies
npm install

# Set up your environment
cp .env.example .env
# Add your Shopify API keys, Supabase URL, Telegram token

# Run the worker
npm run worker
```
