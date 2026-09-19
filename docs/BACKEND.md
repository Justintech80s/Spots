# SPOTS backend

The schema is designed for Supabase/PostgreSQL with Row Level Security. It separates public profiles from credentials, ownership shares, listings, bids, and immutable transfer history.

## Security boundary
Browser clients may read public city data and create their own bids/listings under RLS. They cannot directly transfer ownership. Payment confirmation and final ownership transfers must be performed by authenticated server-side code after verifying the payment and current ownership state.

Raw credit reports, account numbers, private financial statements, government IDs, and unredacted resumes/certificates should not be stored in public tables. Production verification documents should use a private encrypted storage bucket and expose only verification status/badges.

## Setup
1. Create a Supabase project.
2. Run `supabase/schema.sql` in its SQL editor.
3. Copy `.env.example` to `.env` and add the public project URL and anon key.
4. Never put a Supabase service-role key in Vite/Netlify frontend environment variables.
