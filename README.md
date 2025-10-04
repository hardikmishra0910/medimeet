# Full Stack Doctors Appointment Platform — Medimeet 🔥🔥

**Live demo:** https://medimeet-delta.vercel.app/

A full-stack doctors appointment & telemedicine app built with Next.js, Tailwind, shadcn/ui, Neon (Postgres), and Vonage for video/SMS.

## Tech stack
- Next.js, Tailwind CSS, shadcn/ui
- Neon (Postgres), Prisma (optional)
- Vonage (video & SMS)
- Docker (optional), Vercel for deployment

## Features
- Patient & doctor auth
- Doctor profiles & availability
- Appointment booking + calendar
- Video consultations via Vonage
- SMS & email notifications
- Admin dashboard

## Quick start
1. `git clone <repo>`
2. `npm install`
3. Create `.env.local` (see example in repo)
4. `npx prisma migrate dev --name init`
5. `npm run dev`

## Env example
# -----------------------------
# 🔐 Clerk Authentication Keys
# -----------------------------
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=pk_test_XXXXXXXXXXXXXXXXXXXXXXXXXXXX
CLERK_SECRET_KEY=sk_test_XXXXXXXXXXXXXXXXXXXXXXXXXXXX

# Clerk redirect URLs (update based on your routes)
NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up
NEXT_PUBLIC_CLERK_AFTER_SIGN_IN_URL=/dashboard
NEXT_PUBLIC_CLERK_AFTER_SIGN_UP_URL=/dashboard


# -----------------------------
# 🎥 Vonage API Credentials
# -----------------------------
NEXT_PUBLIC_VONAGE_APPLICATION_ID=app-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
VONAGE_PRIVATE_KEY="-----BEGIN PRIVATE KEY-----
YOUR_VONAGE_PRIVATE_KEY_CONTENT
-----END PRIVATE KEY-----"


# -----------------------------
# 🗄️ Database (Neon Postgres)
# -----------------------------
# Example Neon DB connection string
DATABASE_URL=postgresql://<YOUR_DB_USER>:<YOUR_DB_PASSWORD>@ep-icy-dream-123456.us-east-2.aws.neon.tech/medimeet?sslmode=require

## Deployment
- Host on Vercel. Use Neon Postgres and set env vars in Vercel dashboard.
