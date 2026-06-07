# Taxonova HF Space keep-alive

A GitHub Actions cron that periodically pings the free-tier Hugging Face Space
[`claessonlab/Taxonova`](https://huggingface.co/spaces/claessonlab/Taxonova)
so it registers activity and doesn't go to sleep.

- Pings `https://claessonlab-taxonova.hf.space/` every 6 hours.
- No tokens or secrets required — it's an unauthenticated public GET.
- A weekly no-op commit keeps GitHub from auto-disabling the schedule after 60 days
  of repo inactivity.

This is a community workaround, not an officially supported HF feature; it could stop
working if HF changes their inactivity policy.

## Manual run
Actions tab → **keep-space-alive** → **Run workflow**.

## Heartbeat
`heartbeat.txt` is updated weekly by the workflow; ignore it.
