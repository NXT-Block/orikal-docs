# Backend Overview (Public Summary)

This document provides a general overview of the Orikal backend for transparency and integration context. Sensitive components are not described here and remain within the private [`orikal-backend`](https://github.com/NXT-Block/orikal-backend) repository.

## 🛠 Purpose
The backend powers:
- Public API endpoints for the frontend
- Data aggregation from external staking APIs
- Wallet metadata parsing and basic caching
- Role-based access and signature verification

## 🔧 Stack Summary
- **Node.js** with **Fastify** (or NestJS)
- **PostgreSQL** via Supabase
- **Redis** for temporary caching
- **REST API** with secure authentication and scoped endpoints

## 🔄 Key Functionalities
- Serve pool data to the frontend (non-sensitive metrics only)
- Validate user identity via wallet signature
- Manage public wallet profiles and associated metadata

## 🚧 Not Included in Public Docs
> The following sensitive elements are **not** documented here:
- Proprietary scoring and ranking logic
- Integration with paid or restricted APIs
- Secure webhook endpoints and notification logic
- Vault interactions and private account mappings

These elements are managed in the private backend repo and available only to authorized NXT-Block team members.

---

For contribution to the public components of Orikal, please refer to the [getting started guide](./getting-started.md) or contact the team.
