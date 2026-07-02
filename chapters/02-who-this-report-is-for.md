# Who This Report Is For

This report is written for people who have to make — or defend — a CMS decision at a mid-market B2B company. That includes the marketing leader who cannot ship campaign pages fast enough, the technical leader who inherited a plugin-heavy website nobody wants to touch, and the founder who suspects the next website rebuild will cost far more than the last one.

## What "mid-market B2B" means here

We use mid-market in practical terms rather than as a strict revenue band. As a rough orientation, the companies this report describes typically sit in the $10M–$500M revenue range with marketing teams of five to thirty people and lean-to-moderate developer capacity. But the defining traits are operational, not financial:

- The website is a **primary lead-generation and sales-enablement channel**, not a brochure.
- Content is produced by **multiple authors across teams**, often including regional teams or agencies.
- The website **integrates with business systems** — CRM (HubSpot, Salesforce), marketing automation, analytics, sometimes product or partner data.
- The company operates, or is about to operate, in **multiple languages, regions, or brands**.
- There is **some engineering capacity**, but no dedicated web platform team — the website competes with the product for developer time.
- Security, compliance, and governance are real obligations, but there is no full-time person who owns them for the website.

If most of these describe your company, the tradeoffs in this report are your tradeoffs. Enterprises with dedicated digital platform teams and startups with a five-page site will find parts useful, but the calibration is for the middle.

## Types of companies this applies to

The patterns in this report recur across B2B SaaS companies, manufacturers with distributor and regional networks, professional services and consulting firms, technology and IT services providers, healthcare and financial technology companies with compliance constraints, and holding companies or post-M&A groups managing several brand sites. What they share is a website that has quietly become operational infrastructure while still being managed like a marketing asset.

## Signs you have outgrown your current CMS

You do not need a formal audit to recognize the symptoms:

- Publishing a landing page requires a developer ticket, and the backlog is measured in weeks.
- Marketing has started building "shadow" pages in outside tools because the main CMS is too slow to work with.
- Plugin updates, security patches, or platform upgrades regularly break things — so the team avoids updating.
- Adding a language or a brand site triggers an architectural debate rather than a configuration task.
- Nobody can say with confidence who is allowed to change what, or what would happen if a page were published without review.
- The last redesign is less than three years old, and people are already talking about the next one.
- Your integration setup depends on a chain of workarounds (spreadsheets, Zapier chains, duplicate data entry) that one person understands.

Any two of these are a signal. Four or more usually means the question is no longer *whether* to replatform but *how to do it without destroying what works* — which is the subject of Chapter 5.

## What this report helps you decide

- Whether your current CMS is genuinely the problem, or whether the problem is content model, governance, or team structure.
- Which **category** of CMS fits your operating model, before you compare individual products.
- What risk you carry into a rebuild based on the platform you are leaving.
- How to budget for total cost of ownership rather than launch cost.
- How to structure localization, multi-brand architecture, security, and governance requirements before talking to vendors.
- What to test in a proof of concept, and what questions to ask before signing anything.

## Who should be involved in the decision

CMS selection fails most often when a single function makes the call alone. Marketing-only decisions produce platforms engineering refuses to maintain; engineering-only decisions produce platforms marketing routes around. The decision needs a small cross-functional group: whoever owns pipeline and content operations, whoever owns the technical stack and security, and whoever owns the budget over a three-to-five-year horizon. Legal or compliance should be consulted where regulated data or data-residency rules apply.

### For marketing leaders (VP Marketing, Head of Growth, Marketing Director)

Your stake is speed and autonomy: campaign velocity, landing pages, SEO control, localization workflow, and the ability to work without a developer queue. This report will help you articulate those needs as platform requirements — and understand which of engineering's constraints are legitimate guardrails rather than obstruction. Chapters 3, 8 (marketing autonomy vs. engineering control), and 9 are written most directly for you.

### For technical leaders (CTO, Head of Engineering, Digital Lead)

Your stake is maintainability: structured content, version-controlled schemas, clean deployments, security posture, and integrations that don't rot. This report treats those as first-class decision criteria, not as friction. Chapters 5, 6, 7, and the security/governance and SaaS-vs-self-hosted deep dives in Chapter 8 carry the most weight for you.

### For founders and operators (CEO, COO, GM)

Your stake is cost, risk, and optionality. You will be asked to approve a budget whose largest components — maintenance, integrations, migration — are the ones least visible in vendor proposals. The executive summary, the TCO deep dive in Chapter 8, and the scenario recommendations in Chapter 9 will let you pressure-test what you are being asked to sign.

### For multi-brand and multi-region teams

If you manage several brands, domains, or country sites, your CMS decision is mostly a governance and architecture decision: one instance or many, shared content models or separate, central control or local autonomy. Chapters 4 (stages 4–5), 8 (multi-brand and localization deep dives), and the multi-brand scenarios in Chapter 9 address this directly.

### For teams planning a rebuild or migration

If a rebuild is already scheduled, start with Chapter 5. The website rebuild is also a CMS, content, SEO, workflow, and integration migration, and the platform you are leaving defines the risk you carry into it. Do the audits described there *before* selecting a target platform — the audit findings should shape the selection, not the other way around.

One caution before you continue: this report will not name a single best CMS, because there isn't one. It will instead give you the framework to identify the best CMS *for your content model, team, and operating reality* — which is a more defensible decision and a much cheaper one to live with.
