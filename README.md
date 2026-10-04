# FinMix uptime

Outage alerts for https://finmix.th3rdgroup.com. When the site stops
answering, an issue titled **"🔴 FinMix is down"** opens here; GitHub emails
it to the owner and pushes it to the GitHub mobile app. It closes by itself,
with the duration, when the site is back.

Two checkers open and close the same issue:

- the FinMix VPS, every minute (`finmix-uptime.timer`; it also restarts the
  app if it stops answering on the server), and
- this repository's GitHub Actions workflow, every 5 minutes, from outside,
  in case the VPS itself is down.

No application code or data lives here.
