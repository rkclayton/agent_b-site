# Agent B site

Public site for [Agent_b](https://github.com/rkclayton/agent_b), served at `https://agentb.app`.

## Local preview

```powershell
python -m http.server 4173 --directory public
```

Open `http://localhost:4173`. There is no install or build step.

## Cloudflare Pages

- Production branch: `main`
- Build command: leave blank
- Build output directory: `public`
- Custom domain: `agentb.app`

Cloudflare Pages deploys every push to `main`; pull requests receive preview deployments.
