# Stakeholder Intelligence Map

**An AI-powered tool for mapping and navigating stakeholder resistance in enterprise AI transformation programs.**

Built for pharma commercial analytics and go-to-market AI rollouts, but applicable to any large-scale AI change management initiative.

🔗 **[Live demo →](https://your-site.netlify.app)**

---

## What it does

Enterprise AI programs fail not because the technology is wrong, but because the people aren't brought along. This tool helps transformation leads and analytics directors:

- **Map stakeholders** by organizational influence and AI readiness on an interactive matrix
- **Profile resistance** — capture primary objections, secondary fears, and political dynamics for each group
- **Generate engagement strategies** — AI analyzes each stakeholder's resistance profile and produces a tailored four-part plan: engagement strategy, 30-60 day quick win, measurable KPIs, and risk watch
- **Export** the full map as a structured text file for program documentation

---

## Resistance archetypes

| Archetype | Profile |
|---|---|
| **Strategic skeptic** | High influence, questions AI's ability to match domain nuance |
| **Cautious champion** | Technically ready, but worried about data quality or role displacement |
| **Compliance gatekeeper** | Risk-averse, needs governance frameworks before proceeding |
| **Data purist** | Demands auditability and explainability before trusting outputs |
| **Workflow defender** | Resistant to process change; sees AI as a threat to established methods |
| **Active blocker** | Organizational or political incentive to slow or stop adoption |

---

## AI strategy generation

Each stakeholder's profile is analyzed by Claude (Anthropic) to produce:

- **Engagement strategy** — sequenced, archetype-specific approach with named tactics
- **Quick win** — one concrete 30-60 day pilot to build trust with that group
- **Success metrics** — leading and lagging KPIs for adoption tracking
- **Risk watch** — two specific derailment risks with mitigation moves

---

## Deployment (Netlify — recommended)

The AI generation routes through a Netlify serverless function so your API key stays secure server-side.

### Step 1 — Fork and clone this repo

```bash
git clone https://github.com/yourusername/stakeholder-intelligence-map
```

### Step 2 — Deploy to Netlify

1. Go to [app.netlify.com](https://app.netlify.com) → Add new site → Import from Git
2. Connect your GitHub and select this repo
3. Build settings: leave blank (static site + functions, no build step needed)
4. Click **Deploy site**

### Step 3 — Add your API key as an environment variable

In Netlify dashboard → Site configuration → Environment variables → Add variable:

```
Key:   ANTHROPIC_API_KEY
Value: sk-ant-your-key-here
```

Then go to **Deploys → Trigger deploy** to apply the variable.

That's it — the live site will have working AI strategy generation with your key hidden server-side.

### Connect your custom domain

In Netlify → Domain management → Add custom domain → follow the instructions to update your DNS nameservers.

---

## Tech stack

- Vanilla HTML, CSS, JavaScript — zero dependencies, zero build tools
- [Anthropic Messages API](https://docs.anthropic.com/en/api/messages) via Netlify Functions serverless proxy
- [DM Sans + DM Mono + Instrument Serif](https://fonts.google.com) via Google Fonts

---

## Local development

Open `index.html` directly in a browser for UI development. To test AI generation locally:

```bash
npm install -g netlify-cli
netlify dev
```

Then visit `http://localhost:8888`. The function will use your `ANTHROPIC_API_KEY` from a local `.env` file.

---

## License

MIT — use freely, adapt as needed.

---

*Built as part of a portfolio of AI transformation tools.*
