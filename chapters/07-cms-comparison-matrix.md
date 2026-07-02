# CMS Comparison Matrix

This chapter compares ten platforms across the dimensions that decide mid-market B2B projects. Read it after Chapters 4–6: the matrix is a decision aid, not a universal verdict, and it only produces good answers when filtered through your maturity stage, migration risk, and category choice.

## How to read the ratings

Ratings are qualitative — **Strong**, **Medium**, **Weak**, **Variable**, **Depends** — and relative to mid-market B2B needs in 2026. "Medium" does not mean bad, and "Strong" does not mean perfect. We deliberately avoid numerical scores; false precision is how comparison matrices mislead.

Dimension definitions:

- **Marketing autonomy** — can non-technical staff build and adjust pages, campaigns, and SEO settings without a developer ticket?
- **Developer control** — freedom to shape the data model, APIs, and infrastructure.
- **Multi-brand / multi-locale** — managing distinct brands, and mature i18n, without major workarounds.
- **SEO control** — fine-grained control of URLs, metadata, redirects, sitemaps, hreflang, structured data.
- **Self-hosting / data ownership** — can you run it on your infrastructure and export everything?
- **Security / governance** — enterprise auth (SSO), RBAC, audit logging, compliance artifacts, workflows.
- **Integration flexibility** — APIs, webhooks, and ecosystem for connecting CRM/MAP/ERP and the rest of the stack.
- **Implementation / maintenance cost** — typical one-off build and ongoing run cost, relative to this peer group.
- **Migration complexity** — difficulty of moving to (and later from) the platform.
- **Long-term flexibility** — architectural headroom: headless, multi-channel, composability.

## The matrix

### Capability dimensions

| Platform | Marketing autonomy | Developer control | Multi-brand | Multi-locale | SEO control | Self-hosting / data ownership | Security / governance | Integration flexibility |
|---|---|---|---|---|---|---|---|---|
| WordPress | Strong | Strong | Medium | Medium | Strong | Strong | Medium | Strong |
| Webflow | Strong | Medium | Medium | Medium | Strong | Weak | Medium | Medium |
| Drupal | Weak | Strong | Strong | Strong | Strong | Strong | Strong | Strong |
| AEM | Medium | Medium | Strong | Strong | Strong | Medium | Strong | Strong |
| Contentful | Medium | Strong | Strong | Strong | Medium | Weak | Strong | Strong |
| Sanity | Weak | Strong | Medium | Strong | Medium | Weak | Medium | Strong |
| Storyblok | Medium | Strong | Medium | Strong | Medium | Weak | Medium | Strong |
| Strapi | Weak | Strong | Weak | Medium | Medium | Strong | Medium | Strong |
| Directus | Weak | Strong | Medium | Medium | Medium | Strong | Medium | Strong |
| Payload CMS | Weak | Strong | Strong | Strong | Medium | Strong | Medium | Strong |

### Cost, migration, and fit dimensions

| Platform | Implementation cost | Maintenance cost | Migration complexity | Long-term flexibility | Best-fit company type |
|---|---|---|---|---|---|
| WordPress | Medium | Medium | Medium | Strong | Marketing-led B2B with internal dev capacity; corporate site plus microsites |
| Webflow | Low–Medium | Medium | Medium–High | Medium | Marketing-led teams wanting speed and clean output with few dev resources |
| Drupal | Medium–High | Medium | Medium–High | Strong | Dev-centric B2B with complex models, multi-brand/locale, compliance needs |
| AEM | High | High | High | Strong | Large, Adobe-invested enterprises with formal multi-brand governance |
| Contentful | Medium–High | Medium–High | Medium | Strong | Multi-brand/multi-region B2B with a dedicated dev team, composable stack |
| Sanity | Medium–High | Medium | Medium | Strong | Dev-heavy B2B building bespoke digital products and complex content models |
| Storyblok | Medium | Medium | Medium | Strong | Marketing+dev teams wanting visual editing on a headless architecture |
| Strapi | Medium | Medium | Medium | Strong | Dev-centric teams wanting self-hosted API-first, building most UX themselves |
| Directus | Medium | Medium | Medium | Strong | B2B with existing databases needing an instant admin/API layer |
| Payload CMS | Medium | Medium | Medium | Strong | Dev-heavy B2B building multi-tenant platforms or product-like sites |

### Where each platform becomes limiting

| Platform | First signs of strain |
|---|---|
| WordPress | Governance at scale needs custom tooling; multisite upgrades and plugin conflicts get expensive; plugin security demands permanent discipline |
| Webflow | No self-hosting; app-like experiences and very custom front ends hit platform limits; CMS translation at scale becomes manual |
| Drupal | High upfront cost and scarce specialist talent; authoring UX resisted by marketing; maintenance weight on small teams |
| AEM | Cost and timelines; Adobe lock-in; overkill without genuine multi-brand scale; migrations non-trivial in both directions |
| Contentful | Cloud-only; marketing autonomy depends on apps/custom widgets; cost scales steeply with usage and spaces |
| Sanity | Studio is a React app you maintain; marketing autonomy low without heavy UI investment; no self-hosted backend |
| Storyblok | Cloud-only; many brands/tenants get costly and complex; advanced governance requires implementation work |
| Strapi | No visual page building; multi-brand means multiple projects or custom architecture; self-hosted upkeep consumes dev time |
| Directus | Data-first, not page-first: SEO and page composition are front-end concerns; multi-brand needs architectural design |
| Payload CMS | No GUI schema builder — structural changes require code deployment; visual editing and preview must be built; maintenance is yours |

## Notes on the biggest tradeoffs

**The autonomy–control diagonal.** Sort the matrix by marketing autonomy and developer control and a near-perfect inverse relationship appears. WordPress and Webflow give marketing the most independence; Sanity, Strapi, Directus, and Payload give engineering the most control. Nothing in this list is Strong on both out of the box. The platforms that come closest to balancing — Storyblok with its visual editor over a component model, Contentful with its app ecosystem — do so by constraining marketers to developer-defined components, which is precisely the design worth paying for at maturity stage 3 and above. With code-first platforms, autonomy is not absent; it is *deferred* — you can build excellent editorial experiences on Payload or Sanity, but that is a project you must actually fund.

**SEO control means different things in coupled and headless platforms.** WordPress, Webflow, Drupal, and AEM rate Strong because URL management, redirects, sitemaps, and metadata are handled in-platform, with mature tooling. Every headless platform rates Medium — not because SEO outcomes are worse, but because slugs, redirects, hreflang, and structured data become your front end's job. Headless SEO can be excellent; it is simply an engineering deliverable that must appear in the implementation budget, or it silently won't exist.

**Self-hosting and data ownership split the field in two.** WordPress, Drupal, Strapi, Directus, and Payload can run entirely on your infrastructure with full data control. Webflow, Contentful, Sanity, and Storyblok cannot (Sanity's Studio self-hosts; its content backend does not). AEM sits in between — on-prem exists but Adobe is steering toward cloud. If your compliance or IT posture mandates self-hosting, the matrix collapses to five options before any other dimension is considered.

**Multi-brand strength comes in different architectures.** AEM (Multi Site Manager blueprints), Drupal (multisite / Domain Access), Contentful (spaces with cross-space patterns), and Payload (first-party multi-tenant plugin with tenant-scoped access) all rate Strong — but with different governance trade-offs and price tags. WordPress multisite works when brands are similar; Strapi typically means separate projects. The architecture chapter in the deep dives (Chapter 8) matters more than the rating here.

**Cost ratings hide their shape.** Webflow's Low–Medium implementation is real, but its exit cost is among the highest relative to site complexity (front-end rebuild, no runtime export). AEM's High is visible upfront; Contentful's Medium–High creeps via usage and seat scaling. The open-source platforms look cheap on licenses and cost real money in engineering time. Always translate a rating into *whose* budget it hits — subscription line, agency retainer, or internal engineering roadmap.

**"Strong long-term flexibility" is nearly universal — and therefore nearly meaningless alone.** Almost every platform here can, with enough effort, do almost anything. The differentiator is what each platform makes *easy*, *hard*, or *someone else's problem*. That is what the autonomy, governance, and cost columns encode.

## Practical shortlists by situation

These pair with the fuller scenarios in Chapter 9:

- **Marketing-led, few brands, thin dev capacity:** WordPress (well-hosted, plugin-disciplined) or Webflow. Enforce governance from day one.
- **Multi-brand with many regional sites:** AEM if Adobe-invested and budgeted; Drupal for open-source governance depth; Contentful or Payload for API-first multi-tenancy with front-end capacity.
- **Dev-centric product-like platforms and multi-tenant builds:** Payload or Directus first; Strapi or Sanity depending on ecosystem preference. Accept low marketing autonomy or budget to build it.
- **Composable multi-channel with marketer-friendly editing:** Storyblok or Contentful. Maximum developer flexibility instead: Sanity or Payload.
- **Regulated / data-residency constrained:** WordPress, Drupal, Strapi, Directus, Payload — the self-hostable five. Validate SaaS vendors' residency options only if the mandate is soft.
- **Cost-conscious with engineering time available:** self-hosted WordPress or Strapi/Directus/Payload; the trade is dev hours for license fees.
- **Multi-locale with strong SEO requirements:** Drupal or WordPress+WPML for in-platform SEO tooling; Contentful, Storyblok, Sanity, or Payload if you will fund the front-end SEO work properly.

## Caveats

- Ratings reflect typical 2026 mid-market deployments, not every configuration. Enterprise tiers change several cells (Webflow and Storyblok governance, Contentful compliance artifacts, Strapi enterprise features).
- Security and compliance claims must be validated against current certifications (SOC 2, ISO 27001) and your regulators' expectations — vendor postures evolve and tier-gate.
- Implementation and maintenance costs vary more by agency rates, scope discipline, and team skill than by platform. See the TCO deep dive in Chapter 8.
- Migration complexity is directional; real cost depends on content volume, custom logic, and front-end coupling (Chapter 5).

Above all: run a pilot. A two-week proof of concept with your actual content types, your hardest locale case, and your real editors will tell you more than any matrix — including this one.
