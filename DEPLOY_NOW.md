# MY TRANSPORT — Online Test Deployment

This package is prepared for a public test deployment. It is **not yet deployed** because deployment requires the owner's Git/hosting account authorization.

## Recommended test route
Use Render for the first public test. Render supports Node.js/Express web services and provides an `onrender.com` URL. The included `render.yaml` creates the web service and a test Postgres database.

### 1. Put this folder in a GitHub repository
Repository root should contain:
- `package.json`
- `backend/`
- `frontend/`
- `database/`
- `render.yaml`

### 2. Deploy
In Render: New → Blueprint → select the GitHub repository → apply `render.yaml`.

The web service uses:
- Build: `npm install`
- Start: `npm start`
- Health: `/api/health`

### 3. Initialize the database
After the database is created, run `database/schema.sql` once against the provisioned PostgreSQL database.

### 4. Open the generated public URL
Render provides an `onrender.com` URL. This URL can be opened from any laptop or phone.

## Important
The included Render free database is for testing only; free resources have limitations and should not be treated as production storage. Before public customer use, configure production backups, domain, email verification/password reset, stricter CORS, monitoring, and a production database plan.

No payment gateway is enabled in this test deployment.
