# Stakeholder Intelligence Map

**An AI-powered tool for mapping and navigating stakeholder resistance in enterprise AI transformation programs.**

Built for pharma commercial analytics and go-to-market AI rollouts, but applicable to any large-scale AI change management initiative.

🔗 **[Live demo →](https://Ardal-o.github.io/stakeholder-intelligence-map)**

---

## What it does

Enterprise AI programs fail not because the technology is wrong, but because the people aren't brought along. This tool helps transformation leads and analytics directors:

- **Map stakeholders** by organizational influence and AI readiness on an interactive matrix
- **Profile resistance** — capture primary objections, secondary fears, and political dynamics for each group
- **Generate engagement strategies** — AI analyzes each stakeholder's resistance profile and produces a tailored four-part plan: engagement strategy, 30-60 day quick win, measurable KPIs, and risk watch
- **Export** the full map as a structured text file for program documentation

---

## Resistance archetypes

The tool uses six evidence-based archetypes drawn from pharma commercial AI deployments:

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

The AI prompt is grounded in pharma commercial context: HCP engagement models, field force dynamics, MLR review processes, market access complexity, and regulatory compliance constraints.

---

## Usage

### Option A — Use it directly
Open `index.html` in any modern browser. No server, no build step, no dependencies.

### Option B — Host on GitHub Pages
1. Fork this repo
2. Go to Settings → Pages → Deploy from `main` branch, root folder
3. Your live URL: `https://yourusername.github.io/stakeholder-intelligence-map`

### Option C — Deploy to Netlify
Drag the `index.html` file to [app.netlify.com/drop](https://app.netlify.com/drop). Live in 30 seconds.

---

## API key setup

The AI strategy generation calls the Anthropic API from your browser. You'll need an API key:

1. Get a key at [console.anthropic.com](https://console.anthropic.com)
2. Open any stakeholder's detail panel and paste your key into the API key field
3. Click **Save key** — it's stored in your browser's localStorage only, never sent anywhere except directly to Anthropic

> **Privacy note:** The key is stored client-side in your browser. For a production multi-user deployment, route the API call through a serverless function (Netlify Functions, Vercel Edge, Cloudflare Workers) to keep the key server-side.

---

## Tech stack

- Vanilla HTML, CSS, JavaScript — zero dependencies, zero build tools
- [Anthropic Messages API](https://docs.anthropic.com/en/api/messages) for strategy generation
- [DM Sans + DM Mono + Instrument Serif](https://fonts.google.com) via Google Fonts

---

## Extending it

The tool ships empty — no pre-loaded stakeholders. Add your own program's groups with their actual resistance profiles to get strategies calibrated to your context.

To adapt the AI prompt for a non-pharma context, edit the `prompt` string in the `generateStrategy()` function in `index.html`. The four-section output structure (Engagement Strategy / Quick Win / Success Metrics / Risk Watch) works across industries.

---

## License

MIT — use freely, adapt as needed, attribution appreciated but not required.

---

*Built as part of a portfolio of AI transformation tools. Feedback welcome via Issues.*
