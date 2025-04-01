# Contribution Guide

We welcome contributions to Orikal’s open-source repositories under the [NXT-Block](https://github.com/NXT-Block) organization.

## ✅ Where You Can Contribute
- [`orikal-frontend`](https://github.com/NXT-Block/orikal-frontend): UI, wallet flows, dashboards
- [`orikal-smartcontracts`](https://github.com/NXT-Block/orikal-smartcontracts): Smart contract logic, tests, and deployment

> 🛑 The backend repository is private. Contributions are restricted to authorized collaborators.

---

## 🧰 Local Setup
1. Clone the repo:
   ```bash
   git clone https://github.com/NXT-Block/orikal-frontend.git
   cd orikal-frontend
   pnpm install
   ```
2. Copy the `.env.example` and set up your environment:
   ```bash
   cp .env.example .env.local
   ```
3. Start the development server:
   ```bash
   pnpm dev
   ```

---

## ✍️ Code Style
- Use [ESLint](https://eslint.org/) and [Prettier](https://prettier.io/)
- TypeScript is enforced across all codebases
- Comment public functions and components
- Keep pull requests focused and well-described

## 🔀 Branch Strategy
- `main`: stable production code
- `dev`: current development branch
- `feature/<name>` or `fix/<name>`: for specific tasks

## 🧪 Testing
If contributing new features or contracts, please include relevant test cases.
- Use `hardhat test` for smart contracts
- Use `Jest` or `Playwright` for frontend (coming soon)

## 📦 Commit Format (Optional but Recommended)
Use [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/):
```
feat: add new staking pool card UI
fix: correct APY formatting logic
refactor: improve hook structure for wallet tracking
```

## 🤝 Pull Requests
- Always open PRs against the `dev` branch
- Include screenshots (if UI changes)
- Reference related issues or discussions

## 🧠 Code of Conduct
We follow a friendly, inclusive, and constructive tone in all interactions.

---
Thanks for contributing to Orikal 🧡
