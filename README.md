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

The existing Pages project is `agentb-app`. Deploy production after verification:

```powershell
npx wrangler pages deploy public --project-name agentb-app --branch main
```

The project already owns the `agentb.app` custom domain.
