A production-ready Next.js 16 SaaS starter with auth, payments, file storage, and i18n — built to ship fast.

---

## What's included

| Area | Stack |
|---|---|
| Framework | Next.js 16 (App Router) |
| Auth | Better Auth — email/password, GitHub, Google |
| Payments | Stripe — subscriptions + credits billing |
| Database | PostgreSQL + Drizzle ORM |
| File Storage | AWS S3 / Cloudflare R2 |
| UI | Radix UI + Tailwind CSS v4 |
| i18n | next-intl (EN / ZH) |
| Docs | Fumadocs |
| Deployment | Vercel / Cloudflare Workers (OpenNext) |

---

## Getting started

**Prerequisites:** Node.js 18+, pnpm, PostgreSQL

```bash
git clone https://github.com/ZaMc83/modern-full-stack-saas-app
cd modern-full-stack-saas-app
pnpm install
cp env.example .env
```

Fill in `.env` — the required keys are:

```
DATABASE_URL=
BETTER_AUTH_SECRET=
GITHUB_CLIENT_ID= / GITHUB_CLIENT_SECRET=
GOOGLE_CLIENT_ID= / GOOGLE_CLIENT_SECRET=
STRIPE_SECRET_KEY= / STRIPE_WEBHOOK_SECRET=
NEXT_PUBLIC_STRIPE_PRICE_PRO_MONTHLY= / NEXT_PUBLIC_STRIPE_PRICE_PRO_YEARLY=
R2_ACCOUNT_ID= / R2_ACCESS_KEY_ID= / R2_SECRET_ACCESS_KEY= / R2_BUCKET_NAME=
NEXT_PUBLIC_APP_URL=
ADMIN_EMAILS=
```

```bash
pnpm db:push      # push schema to database
pnpm dev          # start dev server → http://localhost:3000
```

---

## Scripts

| Command | Description |
|---|---|
| `pnpm dev` | Start development server |
| `pnpm build` | Production build |
| `pnpm db:push` | Push schema changes |
| `pnpm db:studio` | Open Drizzle Studio |
| `pnpm db:generate` | Generate migrations |
| `pnpm check` | Lint + format with Biome |
| `pnpm typecheck` | TypeScript check |
| `pnpm admin:setup` | Promote a user to admin |
| `pnpm cf:deploy` | Deploy to Cloudflare Workers |

---

## Configuration

All feature flags and settings live in `src/config/`:

- `app.config.ts` — app name, URL, metadata
- `features.config.ts` — toggle features on/off
- `payment.config.ts` — subscription plans and credits per plan
- `credits.config.ts` — per-action credit costs
- `navbar.config.ts` — navigation links
- `appearance.config.ts` — theme defaults

---

## License

MIT
