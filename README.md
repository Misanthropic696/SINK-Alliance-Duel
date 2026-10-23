# SINK-Alliance-Duel
SINK Alliance Duel player rankings and weekly AI-readable performance reports.


## Download or refresh all ranking data

On the configured Windows PC, open a **new PowerShell window** and run:

```powershell
sinkdata
```

This one command clones the full repository on the first run and pulls all new Sunday updates on later runs. Local destination: `Documents\SINK-Alliance-Duel`. No screenshots are published.

On any other computer without the command installed, first run `gh repo clone Misanthropic696/SINK-Alliance-Duel`, then use `git -C SINK-Alliance-Duel pull --ff-only` to refresh.

Current midweek data for 19–22 October 2026 is in `data/2026-10-19/` and is provisional pending manual OCR alias verification. Sunday files will be added by week without replacing history.
