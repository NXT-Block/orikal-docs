# Architecture Overview

This document outlines the technical architecture of **Orikal**, a multi-repository Web3 platform developed by [NXT-Block](https://github.com/NXT-Block).

## 🧩 System Components
Orikal follows a modular architecture distributed across multiple repositories:

### 1. `orikal-frontend` (Open-source)
- Built with **Next.js** (App Router)
- Wallet interactions via **Wagmi** and **Viem**
- Styled with **TailwindCSS** and **ShadCN UI**
- Deployed on **Vercel**

### 2. `orikal-smartcontracts` (Open-source)
- Written in **Solidity**
- Managed with **Hardhat**
- Designed for transparency and auditability
- Tracks staking pools, wallet whitelisting, and treasury linkage

### 3. `orikal-backend` (Private)
- Built with **Fastify** or **NestJS** on **Node.js**
- Uses **PostgreSQL**, **Supabase**, and **Redis**
- Contains API endpoints, staking data aggregation, and partner integrations
- Sensitive logic (e.g., scoring engine, secret API calls) remains internal

## 🌐 Communication Flows
```
[User Wallet] ←→ [Frontend] ←→ [Backend APIs] ←→ [Smart Contracts / External APIs]
```

## 🔒 Security Principles
- All secrets and credentials managed via environment variables and GitHub Actions secrets
- Contracts are public and auditable
- Backend enforces rate-limiting and signature validation

## 📈 Scalability
- CI/CD per repo (GitHub Actions)
- SSR-enabled frontend
- Modular backend with potential for microservices

## ⚠️ Private Architecture Notes
Sensitive backend components (scoring algorithms, business rules, proprietary integrations) are documented in the private `orikal-backend` repository.