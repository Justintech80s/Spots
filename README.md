# SPOTS

Original interactive digital-city application for Netlify.

## Current build
- Responsive city explorer
- Original buildings and property tiers
- Base property values and Spot Asset Wealth
- Searchable properties
- World Editor foundation
- Individual/group ownership architecture foundation
- Netlify SPA configuration

Purchasing and bidding remain disabled until secure authentication, persistent ownership records, payment verification, and server-enforced transaction rules are implemented. Spot Asset Wealth is an in-platform metric, not real-world net worth or an investment return.

## Run
`npm install` then `npm run dev`.

## Netlify
Build command: `npm run build`; publish directory: `dist`.


## Backend foundation
PostgreSQL/Supabase schema, RLS policies, ownership shares, verified credential records, listings, bids and transfer audit records are now included under `supabase/` and `src/lib/`. See `docs/BACKEND.md`.
