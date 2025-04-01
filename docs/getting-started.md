# Getting Started

This guide will help developers get up and running with Orikal's open-source components. Private backend access is restricted to team members of [NXT-Block](https://github.com/NXT-Block).

## ✅ Prerequisites
- [Node.js](https://nodejs.org/) >= 18
- [pnpm](https://pnpm.io/) installed
- Git access to the NXT-Block organization

## 📦 Clone the Repositories
```bash
git clone https://github.com/NXT-Block/orikal-frontend.git
cd orikal-frontend
pnpm install

# Optional (if working on smart contracts)
git clone https://github.com/NXT-Block/orikal-smartcontracts.git
cd orikal-smartcontracts
pnpm install
```

> 🔒 The `orikal-backend` repository is private. Request access if you're a team member.

## ⚙️ Environment Variables
Each repo includes a `.env.example` file.
Create a `.env.local` file and populate it with the necessary values.

```bash
cp .env.example .env.local
```

You’ll typically need:
- NEXT_PUBLIC_PROJECT_NAME (frontend)
- WALLETCONNECT_PROJECT_ID (frontend)
- ALCHEMY / INFURA key (frontend)
- RPC URLs (frontend/contracts)
- API keys (backend/private only)

## 🧪 Run the Projects
### Frontend (Next.js)
```bash
pnpm dev
```

### Smart Contracts (Hardhat)
```bash
npx hardhat test
```

## 🧠 Tips for Contributors
- Use consistent naming for branches: `feature/<name>`, `fix/<name>`
- Lint and format code before committing (`pnpm lint`, `pnpm format`)
- Open issues or discussions for bigger changes

For more details on contributing, see [`docs/contribution.md`](./contribution.md).
