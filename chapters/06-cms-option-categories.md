# CMS Option Categories

Most bad CMS choices are category errors, not product errors. A team that agonizes over Contentful vs. Sanity has usually already made the important decision — headless, SaaS, developer-operated — without noticing. This chapter compares the six CMS categories relevant to mid-market B2B in 2026, so you can make the category decision deliberately before comparing products (Chapter 7 does that).

Each category embodies an operating model: who builds, who publishes, who maintains, who is responsible when something breaks, and what you pay for versus what you own. Choose the operating model first.

## Website builders — Wix, Squarespace

**What they are.** All-in-one, template-driven site builders with integrated hosting, a basic CMS, and built-in marketing tools. Designed for speed-to-launch.

**Best-fit use cases.** Early-stage brochure sites, small service firms, event microsites, satellite pilots. In mid-market contexts, they appear legitimately as *satellite* properties — microsites and pilots — rather than the main corporate site.

**Typical buyer.** Marketing-led companies with little or no development capacity, usually under ~25 people, one primary site.

**Strengths.** Very fast time to value; hosting, security basics, and core marketing tools included; no code required. Wix brings a broad app ecosystem and a capable multilingual app; Squarespace brings design polish and simple commerce.

**Weaknesses.** Template constraints shape brand expression; you don't control the stack, so advanced schema, edge logic, or experimentation infrastructure is out of reach; multi-brand and governance capability is minimal. Squarespace has no built-in i18n — multilingual requires third-party tooling.

**Cost model.** Per-site SaaS tiers with published pricing; add-ons (apps, multilingual tools, transaction fees) accumulate.

**Implementation complexity.** Low — hours to days, largely DIY.

**Marketing autonomy / developer control.** Autonomy high; developer control low (Wix's Velo scripting is the ceiling).

**Localization / multi-brand.** Wix: workable via its Multilingual app. Squarespace: weak. Multi-brand: weak in both — each site is an island.

**Governance/security.** Solid at the platform level (Wix maintains SOC 2, PCI, ISO and GDPR-class compliance), but governance features are coarse: limited roles, minimal audit logging.

**Migration risk.** Low risk to adopt, moderate-to-high lock-in to leave: content partially exports, design and integrated features don't (see Chapter 5).

**Where this category becomes limiting:** the moment you need structured content, real workflow, multiple sites, or any locale/brand architecture.

## Visual builders — Webflow

**What it is.** A design-led visual canvas that generates clean front-end code, coupled with a structured CMS and managed hosting. It bridges design and development.

**Best-fit use cases.** Mid-market brand sites and marketing hubs where design fidelity and performance matter but the team doesn't want a custom codebase.

**Typical buyer.** 20–200-person B2B companies with in-house or agency design talent and modest engineering availability.

**Strengths.** Real design control with semantic output; a genuine CMS with structured collections and references; reusable components approaching design-system discipline; Enterprise tier adds SSO, SOC 2 Type II, advanced permissions, and native localization.

**Weaknesses.** Closed SaaS runtime — you don't own hosting or delivery; complex personalization, app-like experiences, and very large content volumes hit platform limits; CMS-item translation at scale can become manual bottleneck work; ecommerce and localization currently can't be combined.

**Cost model.** Per-site tiers; Enterprise is custom. Localization is an add-on priced per locale.

**Implementation complexity.** Moderate — fast for design-led sites, developer help needed for integrations.

**Marketing autonomy / developer control.** Autonomy high — this is the category's reason to exist. Developer control moderate: front-end code can be exported, but the CMS runtime cannot.

**Localization / multi-brand.** Localization: genuinely native now (locale routing, per-locale SEO fields, auto hreflang), strongest on Enterprise. Multi-brand: limited — separate sites, with Enterprise Shared Libraries syncing components across them.

**Governance/security.** Enterprise tier is credible (SSO, SCIM, audit log API, publishing workflows, no plugin attack surface); lower tiers are not suited to regulated contexts.

**Migration risk.** Moderate: content and code export exist, but interactions and design are coupled to the canvas; leaving usually means a front-end rebuild.

**Where this category becomes limiting:** backend logic, user portals, programmatic SEO at scale, many brands, or any requirement to own the runtime.

## Traditional CMS — WordPress, Drupal

**What they are.** Open-source monolithic CMS where backend and front end are coupled (though both can run headless). WordPress powers a large share of the web and has the largest ecosystem in this report; Drupal is the governance-heavy, structured-content specialist.

**Best-fit use cases.** WordPress: corporate sites, blogs, resource centers where ecosystem breadth and agency availability matter. Drupal: complex multi-site ecosystems, granular permissions, regulated industries, government and public sector.

**Typical buyer.** WordPress: broad mid-market, marketing-led with dev or agency support — often the default by inertia. Drupal: organizations with strong dev teams or Drupal agency partners and five-plus governed sites.

**Strengths.** Free software with full data ownership; enormous talent pools (especially WordPress); genuine multi-site from one codebase; enterprise-grade managed options (WordPress VIP adds hardened security and compliance; managed Drupal platforms similar). Drupal's core multilingual and permission systems are among the strongest anywhere.

**Weaknesses.** WordPress security and performance depend heavily on hosting discipline and plugin curation — the plugin ecosystem is both its superpower and its main risk. Drupal carries a steep learning curve, weaker authoring UX, and a shrinking specialist talent pool.

**Cost model.** Software is free; money goes to hosting, plugins/modules, agencies, and enterprise tiers. Costs are people-shaped, not license-shaped.

**Implementation complexity.** WordPress: low to moderate, rising sharply at scale. Drupal: high — experienced developers or agencies required.

**Marketing autonomy / developer control.** WordPress: autonomy high (Gutenberg, builders — with governance caveats covered in Chapter 8); Drupal: autonomy moderate-to-low out of the box. Developer control: very high in both — full open-source access.

**Localization / multi-brand.** Both capable: WordPress via mature plugins (WPML, Polylang), Drupal via core i18n that global organizations rely on. Multi-site architectures support multi-brand in both, with governance overhead growing per site.

**Governance/security.** Drupal: strong security ethos, dedicated security team, granular RBAC and content moderation in core. WordPress: strong *when paired with enterprise hosting and process*; risky when plugin hygiene lapses.

**Migration risk.** Moderate to high on exit — deep customization and plugin/module dependencies (Chapter 5).

**Where this category becomes limiting:** WordPress — governance at scale and plugin-security discipline; Drupal — cost of change and authoring experience for marketing-led teams.

## Enterprise DXP — AEM, Sitecore

**What they are.** Full-suite digital experience platforms: CMS plus DAM, personalization, analytics/CDP integration, delivered as cloud services with system-integrator implementations.

**Best-fit use cases.** Global multi-brand, multi-channel operations with heavy personalization and mature marketing ops — manufacturing, life sciences, financial services at the upper end of mid-market and beyond.

**Typical buyer.** Organizations (often $100M+ revenue) with dedicated digital teams, SI partners, and existing investment in the vendor's ecosystem (Adobe stack for AEM).

**Strengths.** The most complete out-of-the-box story for multi-brand, multi-locale governance: blueprint/rollout models (AEM Multi Site Manager), approval workflows, audit logs, enterprise compliance, deep integration with the vendor's marketing suite.

**Weaknesses.** Highest TCO in this report; 6–18+ month implementations; specialized talent; and severe overkill for companies that don't need cross-channel orchestration. Vendor lock-in is structural — Chapter 5 rates AEM exit risk as the highest of any platform.

**Cost model.** Contractual, unpublished, negotiated per customer; partner benchmarks put licensing in the low six figures annually with implementations frequently $250k–$1M.

**Implementation complexity / autonomy / control.** Complexity: high, SI-driven. Marketing autonomy: moderate once configured — powerful, but heavy lifting needs partners. Developer control: high *within* the platform's opinionated architecture.

**Localization / multi-brand.** The category benchmark. If you genuinely operate dozens of brand/locale permutations with formal governance, this is what the machinery was built for.

**Governance/security.** Very strong: enterprise certifications, granular ACLs, mature workflows, compliance tooling.

**Migration risk.** High in both directions — expensive to adopt, more expensive to leave.

**Where this category becomes limiting:** the budget line. For most mid-market B2B teams, the honest question is not "is it capable?" but "will we use a tenth of it?"

## SaaS headless CMS — Contentful, Sanity, Storyblok

**What they are.** API-first, cloud-native content platforms that decouple content from presentation: editors work in the vendor's UI, developers deliver content to any front end via APIs.

**Best-fit use cases.** Composable stacks: modern front ends (Next.js, Astro), omnichannel content reuse, multi-brand portals, campaign micro-frontends.

**Typical buyer.** Product- or engineering-led mid-market with front-end capacity, or agencies building multi-client platforms. Marketing wants clean editing; engineering wants to own the stack.

**Strengths.** Excellent developer experience (schemas, webhooks, CLI, environments); genuine multi-brand mechanisms (spaces, datasets, multi-space pipelines); strong native localization (Contentful field-level locales with fallback chains; Sanity's flexible i18n patterns; Storyblok's field/folder/space strategies); large integration ecosystems; vendor-managed infrastructure with SOC 2/ISO-class compliance.

**Weaknesses.** The front end is your responsibility — you build and maintain the presentation layer, and with it all SEO plumbing (slugs, redirects, hreflang, sitemaps). Composability means assembling your own stack for search, personalization, and preview. Costs scale with seats, spaces, locales, and API usage — enterprise tiers land in five to six figures annually.

**Cost model.** Tiered SaaS scaling with usage; enterprise custom. Budget for overages as you grow.

**Implementation complexity.** Moderate to high: faster than DXP, but real front-end engineering.

**Marketing autonomy / developer control.** Autonomy: high *after* the models and front end are built — and varies by product (Storyblok's visual editor is the marketer-friendliest; Sanity requires the most custom investment). Developer control: very high.

**Localization / multi-brand.** Strong across the category — this is one of its core selling points.

**Governance/security.** Good: vendor-managed infra, RBAC, SSO and audit on higher tiers. Fine-grained governance often requires enterprise plans.

**Migration risk.** Moderate: content is genuinely portable via APIs; the cost of leaving is front-end re-implementation and integration re-plumbing (Chapter 5).

**Where this category becomes limiting:** cost growth at scale, cloud-only deployment (a hard stop for strict data-residency mandates), and marketing autonomy that depends on how much editorial UX your team builds.

## Open-source / self-hosted headless CMS — Payload CMS, Strapi, Directus

**What they are.** Open-source, API-first CMS you run on your own infrastructure (or the vendor's optional cloud). Full code, database, and API access.

**Best-fit use cases.** Custom portals, multi-tenant and multi-brand platforms, data-residency-constrained deployments, and websites that are really products — needing custom backend logic, authentication, or workflows alongside content.

**Typical buyer.** Tech-forward mid-market with an in-house dev team or a long-term agency partner; comfortable owning infrastructure.

**Strengths.** Full control and data ownership: MIT/GPL-class licensing, deployable anywhere, no per-seat costs when self-hosted. Multi-brand via first-party multi-tenancy (Payload's multi-tenant plugin with tenant-scoped access control; Directus's schema-as-code patterns; Strapi via multi-project patterns). Built-in localization (Payload's native field-level i18n with fallback; Strapi's i18n plugin). Cost efficiency at scale — spend shifts from licenses to infrastructure and development.

**Weaknesses.** You own deployment, patching, scaling, backups, and security hardening. Ecosystems are smaller than SaaS headless; more is custom-built, including editorial UX and preview. Time to value is longer — this is not the "site live in two weeks" category.

**Cost model.** Free software; costs are hosting, DevOps, and development time, plus optional paid cloud or enterprise editions.

**Implementation complexity.** High — you build and maintain CMS configuration, front end, and infrastructure.

**Marketing autonomy / developer control.** Autonomy: moderate — admin UIs are usable, but structural changes and workflow customization need developers. Developer control: the maximum available in any category.

**Localization / multi-brand.** Good to strong, with the caveat that routing, hreflang, and SEO tooling live in your application layer.

**Governance/security.** Exactly as strong as your team makes it. Code-defined access control (Payload's field-level model is notable) is powerful; audit trails and compliance artifacts are yours to implement or buy via enterprise editions.

**Migration risk.** Low from the CMS side — you own the database and APIs — but a tightly coupled custom stack can still make change expensive.

**Where this category becomes limiting:** teams without sustained engineering capacity. If developer time is scarce or contested, the maintenance burden lands on nobody, and security debt follows.

## Category comparison table

| | Website builders | Visual builders (Webflow) | Traditional (WP/Drupal) | Enterprise DXP | SaaS headless | OSS/self-hosted headless |
|---|---|---|---|---|---|---|
| Best fit | Microsites, pilots | Design-led brand sites | Corporate sites; governed multi-site (Drupal) | Global multi-brand, personalization | Composable, omnichannel | Custom platforms, data-sensitive |
| Cost model | Per-site SaaS | Per-site tiers + Enterprise | Free software; people costs | Contractual, high | Usage-scaling SaaS | Free software; infra + dev |
| Implementation | Low | Moderate | Low–Mod (WP) / High (Drupal) | High | Moderate–High | High |
| Marketing autonomy | High | High | High (WP) / Moderate (Drupal) | Moderate | High once built (varies) | Moderate |
| Developer control | Low | Moderate | Very high | High (in-platform) | Very high | Maximum |
| Localization | Weak–OK | Strong (Enterprise) | Strong (plugins/core) | Strongest OOTB | Strong | Good (app-layer SEO) |
| Multi-brand | Weak | Limited | Multi-site capable | Strongest OOTB | Strong (spaces/datasets) | Strong (multi-tenant) |
| Governance/security | Coarse | Strong on Enterprise | Discipline-dependent (WP) / Strong (Drupal) | Very strong | Good; enterprise tiers | As strong as you build |
| Exit risk | Mod–High | Moderate | Mod–High | High | Moderate | Low (CMS side) |

## Choosing a category: the decision logic

Work through these questions in order — each eliminates categories:

1. **Do you have (and will you keep) real engineering capacity for the website?** No → website builders, Webflow, or managed WordPress. Yes → everything remains open.
2. **Do you have a hard data-residency or self-hosting mandate?** Yes → traditional CMS or open-source headless only. This single constraint eliminates all SaaS categories, including Webflow and SaaS headless.
3. **Do you need content on channels beyond the website, or a website with product-like backend logic?** Yes → headless (SaaS or open-source). No → coupled platforms remain viable and simpler.
4. **Is your multi-brand/multi-locale scale genuinely enterprise (dozens of governed properties)?** Yes → enterprise DXP earns consideration — alongside Drupal and multi-tenant headless at lower cost. No → DXP is almost certainly overkill.
5. **Where must marketing autonomy come from?** Built-in (Webflow, WordPress, Storyblok-style visual headless) or built-for-you (code-first headless with custom editorial UX)? Be honest about whether your engineering team will actually invest in the latter.
6. **What is your three-year budget shape?** Predictable subscriptions (SaaS) versus people and infrastructure (open source)? Neither is inherently cheaper — they are different risk profiles.

A final calibration note: the maturity stages of Chapter 4 map roughly onto categories — builders and Webflow serve stages 1–3, traditional CMS and SaaS headless serve stages 2–5, open-source headless serves stages 3–6, and DXP earns its cost only at stages 5–6 with enterprise scale. If your category choice implies jumping more than one stage, treat that as a warning sign, not ambition.

The next chapter descends from categories to products, comparing ten platforms across fourteen dimensions.
