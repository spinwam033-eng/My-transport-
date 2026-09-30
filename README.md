# MY TRANSPORT V19

Cloud office-data expansion for the MY TRANSPORT SaaS foundation.

## V19 adds
- Customers cloud records
- Vehicles cloud records: Truck, Heavy Machinery, Other Vehicle
- Customer payments cloud records
- Invoices with VAT/tax fields and remaining balance
- Separate Money Transfer records
- Company dashboard summary API
- Company isolation on every business-data query
- Role/module permission checks for write operations
- Audit logging for created/updated financial and operational records

## Run locally
1. Install Node.js 18+ and PostgreSQL.
2. Create a PostgreSQL database.
3. Run `database/schema.sql` against it.
4. Copy `.env.example` to `.env` and set `DATABASE_URL` and a strong `JWT_SECRET`.
5. Run `npm install`.
6. Run `npm start`.
7. Open `http://localhost:3000`.

## Production requirements
This package is not itself a hosted service. Before public customers use it, deploy the API over HTTPS with managed PostgreSQL, automated backups, rate limiting, secure token/cookie handling, monitoring, email verification/password reset, real Google OAuth, and payment/subscription integration.


## V20 — Subscription-ready
V20 adds company subscriptions with a 14-day trial foundation, Basic/Professional/Business plan metadata, owner-only checkout-intent and cancellation endpoints, and a Plans & Subscription dashboard. No payment is processed in this build. Connect a real payment provider and verified webhooks before accepting customer money.

Run:
1. Create PostgreSQL database and run `database/schema.sql`.
2. Copy `.env.example` to `.env` and set `DATABASE_URL` and `JWT_SECRET`.
3. Run `npm install` then `npm start`.
