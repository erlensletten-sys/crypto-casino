# 💎 Diamond Casinos — Built for operators who move fast - By R4ke.

> **A production-ready, self-hosted crypto casino with plug-and-play game integrations, provably fair original games, and a full-featured admin dashboard.**

[![DemoWebsite](https://img.shields.io/badge/DemoWebsite-demo.notogreed.com-00ff88?logo=googlechrome&logoColor=white)](https://demo.notogreed.com)
[![Telegram](https://img.shields.io/badge/Telegram-@rakestake-26A5E4?logo=telegram&logoColor=white)](https://t.me/rakestake)
[![Website](https://img.shields.io/badge/Website-notogreed.com-00ff88?logo=googlechrome&logoColor=white)](https://notogreed.com)
[![License](https://img.shields.io/badge/License-Proprietary-d4af37)](#license)

---

## Overview

Diamond Casinos is a turnkey crypto casino platform designed for operators who want to launch fast without compromising on quality. The platform ships with a modern frontend, a high-performance backend, and a pre-configured game aggregator integration that gives you instant access to **1,500+ slots and live casino games** from top-tier providers.

Whether you're deploying your own casino or licensing a white-label instance — you get a battle-tested product, not a starter template.

---

## What's Included

### 🎰 Game Aggregator

Pre-integrated game aggregator providing access to major providers out of the box:

- **Pragmatic Play** — Slots & Live Casino
- **PG Soft** — Mobile-first slots
- **Hacksaw Gaming** — High-volatility slots
- **Spribe** — Mini-games (Aviator, Mines, etc.)
- **Habanero** — Classic & video slots
- **Evoplay** — 3D slots & instant games
- **60+ additional providers** — Full catalog available on request

Game lobby includes provider filtering, search, category tabs, and demo mode support. All API credentials and provider configurations are included with your license.

### 🎲 Provably Fair Originals

Custom-built house games with full cryptographic verification:

| Game | Type | Multiplayer |
|------|------|-------------|
| Dice | House | No |
| Limbo | House | No |
| Crash | House | Yes |
| Mines | House | No |
| Keno | House | No |
| HiLo | House | No |
| Plinko | House | No |
| Chicken Road | House | No |
| Skipper | House | No |
| Blackjack | House | No |
| Roulette | House | No |

All games use **HMAC-SHA256** with server seed, client seed, and nonce. Every bet is independently verifiable by your players.

### 💰 Crypto Payments

- 100+ supported cryptocurrencies
- Automatic deposit detection via webhook verification
- Configurable minimum deposit/withdrawal thresholds
- Payment processor credentials provided separately upon licensing

### 👤 User System

- Registration & login with JWT authentication
- Multi-currency user wallets
- Full bet history with unique, verifiable bet IDs
- Provably fair verification page per bet
- Profile settings and session management

### 🛡️ Admin Dashboard

- Agent balance monitoring
- User management (view, edit, suspend)
- Game performance analytics
- Deposit/withdrawal oversight
- Provider status and health checks
- System configuration panel

---

## Deployment

Diamond Casinos is delivered as a **ready-to-deploy package**. You don't need to configure infrastructure from scratch — our automated setup handles everything.

### What You Need

- A VPS (Ubuntu recommended)
- A domain pointed to your server
- Your payment processor API keys (provided with license)

### How It Works

1. **Receive your license key** — tied to your domain
2. **Run the setup script** — configures the full environment automatically
3. **Add your API keys** — payment processor and branding preferences
4. **Go live** — SSL, services, and game connections are handled for you

From zero to a running casino in minutes, not days.

> *Detailed setup documentation is included in the licensed package.*

---

## Architecture

```
┌──────────────────────────────────────────┐
│           Reverse Proxy (Auto-SSL)       │
└────────────────────┬─────────────────────┘
                     │
       ┌─────────────┼──────────────┐
       │             │              │
  ┌────▼───┐   ┌────▼────┐   ┌────▼─────┐
  │Frontend│   │ Backend │   │WebSocket │
  │  (SPA) │   │  (API)  │   │ (Live)   │
  └────┬───┘   └────┬────┘   └────┬─────┘
       │            │              │
       │   ┌────────┼────────┐    │
       │   │        │        │    │
  ┌────▼───▼┐  ┌────▼──┐  ┌─▼────▼────┐
  │ Primary │  │ Relay  │  │   Cache   │
  │   DB    │  │  DB    │  │  (Fast)   │
  └─────────┘  └───────┘  └───────────┘
       │            │
  ┌────▼────┐  ┌────▼──────┐
  │  Game   │  │  Payment  │
  │Aggregator│ │ Processor │
  └─────────┘  └───────────┘
```

---

## Source Code Protection

Diamond Casinos source code is delivered with a dual-layer protection system to prevent unauthorized distribution and deployment.

### 🔒 Code Encryption (PyArmor)

Core backend modules — including game logic, API integrations, wallet services, and licensing enforcement — are encrypted and obfuscated using **PyArmor**. This means:

- Source code cannot be read, decompiled, or reverse-engineered
- Protected modules run natively with no performance impact
- Encryption is tied to your deployment environment

### 🔑 License Key Validation

Every deployment requires a valid license key issued by Diamond Casinos. The license system enforces:

- **Domain locking** — your key only works on your authorized domain(s)
- **Runtime validation** — the platform checks license status on boot and at intervals
- **Tamper detection** — attempts to bypass or modify the license layer will halt the application
- **Expiry support** — licenses can be time-bound or perpetual based on your agreement

Operators receive full access to the **frontend source code** (React) for custom branding and UI modifications. Backend service modules that handle core business logic are delivered in encrypted form.

### What's Open vs. Protected

| Layer | Access |
|-------|--------|
| Frontend (UI, styling, branding) | ✅ Full source — customize freely |
| API routes & endpoints | ✅ Full source — extend as needed |
| Admin dashboard | ✅ Full source |
| Game engines (provably fair) | 🔒 Encrypted |
| API integration layer | 🔒 Encrypted |
| Wallet & payment services | 🔒 Encrypted |
| License enforcement | 🔒 Encrypted |

---

## White-Label Licensing

### What You Get

- Complete casino platform ready to deploy
- Pre-configured game aggregator with 1,500+ games
- All original provably fair games
- Admin dashboard
- Crypto payment integration
- Automated setup script
- Dedicated support via Telegram

### Pricing

| Package | What's Included | Cost |
|---------|----------------|------|
| **Self-Deploy** | Full platform + license key | Free |
| **API Suite** | Slots + Live Casino + Sportsbook | From 5% GGR |
| **Custom Originals** | Bespoke provably fair game development | Custom quote |

---

## Provably Fair

Every bet on an original game produces a verifiable result:

```
result = HMAC-SHA256(server_seed, client_seed:nonce)
```

Players can verify any bet using the server seed (revealed after rotation), their client seed, and the nonce. The platform uses the same cryptographic standard trusted across the industry.

---

## Security

- JWT authentication with refresh token rotation
- HMAC-verified payment webhooks
- Rate limiting and abuse prevention
- CORS whitelisting
- Domain-locked license enforcement
- Input validation on all endpoints
- Network isolation between services
- Encrypted core modules

---

## Contact

| Channel | Link |
|---------|------|
| **Telegram** | [@rakestake](https://t.me/rakestake) |
| **Website** | [notogreed.com](https://notogreed.com) |
| **Demo Website** | [demo.notogreed.com](https://demo.notogreed.com) |

Demos available on request. White-label inquiries welcome aswell as redesigns.

---

## License

This project is proprietary software. Core modules are encrypted and require a valid license key for deployment. Unauthorized distribution, modification of protected modules, or deployment without a valid license is prohibited.

Contact [@rakestake](https://t.me/rakestake) for licensing.

---

<p align="center">💎 Diamond Casinos — Built for operators who move fast - By R4ke.</p>
