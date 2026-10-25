# SW-Heartbeat

Free 24/7 heartbeat for the ScamWatch Ghana SW-SENTINEL bot.

This public repo exists for one reason: GitHub Actions on **public** repos
run with UNLIMITED free minutes, while private-repo minutes are quota-limited.
The workflow here simply pings the sentinel sweep endpoint every 15 minutes,
so the bot watches both wolves (gwill003 + vaazat + the elder's network)
without using any private Actions minutes, any Vercel cron beyond the daily
safety net, or any Base44 credits.

- The sweep URL lives in the encrypted repo secret `SWEEP_URL` (never in code).
- The sentinel itself, its state, and all credentials live in the Vercel
  deployment and the private case vault - nothing sensitive is in this repo.
- If GitHub emails you that scheduled runs were disabled due to repo
  inactivity (60-day rule), just push any commit here or re-enable the
  workflow: it is a known maintenance tap, one click.

Case log: SWG-2026-049 (25 Oct 2026).
