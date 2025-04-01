# Frontend Overview

This document provides a technical overview of the Orikal frontend, designed for seamless interaction with on-chain staking infrastructure and off-chain analytics.

## 🖥 Tech Stack
- **Next.js** (App Router)
- **TypeScript**
- **Tailwind CSS** for styling
- **ShadCN UI** for reusable UI components
- **Wagmi** and **Viem** for wallet interactions
- **Recharts** for basic data visualizations (subject to evolve)
- **WalletConnect** for broader wallet compatibility

## 🌐 Application Features
- Wallet connection and signature-based auth
- Dashboard with portfolio overview and staking pool insights
- Responsive UI designed for both desktop and mobile
- Integration with Orikal’s backend for pool and wallet data

## 📁 Structure Highlights
```
/app           → Next.js App Router structure
/components    → Reusable UI components (ShadCN-based)
/hooks         → Custom React hooks (wallets, effects, etc.)
/lib           → Web3 clients, utils, validation helpers
/public        → Assets (logos, images)
/styles        → Tailwind config and globals
```

## 🧪 Testing (Planned)
We aim to implement E2E and component-level testing using:
- **Playwright** or **Cypress**
- **Jest** + **React Testing Library**

## 🚀 Deployment
The frontend is deployed using **Vercel** with environment variables set securely through their dashboard.

## 🔐 Security Practices
- Only public, non-sensitive data is fetched client-side
- Environment variables use the `NEXT_PUBLIC_` prefix when needed
- Wallet interactions are read-only unless explicitly signed by the user

---
For environment setup, see the [`getting-started.md`](./getting-started.md) documentation.
