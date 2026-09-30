# The Slay Lady — Live Voting
Routes: /admin, /vote, /result.
1. Create a dedicated Supabase project.
2. Run supabase/schema.sql.
3. Add five candidates with hosted image URLs.
4. Copy .env.example to .env.local and fill project URL, publishable key, secret key.
5. npm install && npm run build.
6. Deploy to Vercel and point QR to /vote.
Security: public clients can only read event/candidate data. Votes are written through server route using the secret key. Unique(event_id,device_token) blocks repeat votes per browser/device token.
