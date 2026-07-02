# Risk by Current CMS

Most CMS evaluations obsess over the destination and ignore the departure point. That is backwards. The hardest, most expensive, and most dangerous parts of a website rebuild are determined by the platform you are leaving: what it lets you export, what it did to your URLs, what implicit structure it let you accumulate, and which integrations quietly depend on it.

> The CMS a company is leaving tells you what kind of risk it is carrying into the rebuild.

This chapter maps that risk for the nine platforms mid-market B2B companies most commonly migrate away from. The risks described are about the *move itself*, largely independent of the target — though the target changes the picture (WordPress-to-Webflow is a different project than WordPress-to-headless).

One framing note before the details: the website rebuild is also a CMS, content, SEO, workflow, and integration migration. Teams that scope it as "a new website" systematically under-budget the other four migrations riding along with it.

## The migration risk matrix

Ratings: **L** low · **M** medium · **H** high · **VH** very high. Cost and timeline figures are indicative mid-market B2B ranges drawn from 2026 agency benchmarks — use them to sense-check proposals, not as quotes.

| Risk dimension | Wix | Squarespace | WordPress | Webflow | Drupal | AEM | Contentful | Sanity | Strapi |
|---|---|---|---|---|---|---|---|---|---|
| Overall migration difficulty | H | M–H | M–H | M–H | H–VH | VH | H | H | M–H |
| Content export limitations | H | M–H | L–M | M | M (technical) | VH | L (good tooling) | L–M | M |
| SEO / redirect risk | H | M–H | M–H | M | M–H | H | H | H | M–H |
| Media migration risk | H | M–H | M | M | M | H | M–H | M–H | M |
| Content modeling risk | L–M | L–M | M–H | M | H | H | M–H | M–H | M–H |
| Workflow / governance risk | L–M | L–M | M–H | L–M | H | VH | M–H | M–H | M–H |
| Integration risk | H | M–H | M–H | M | M–H | VH | M–H | M–H | M–H |
| Indicative cost | $10k–30k | $12k–40k | $20k–80k+ | $15k–60k | $30k–120k+ | $150k–500k+ | $40k–150k+ | $40k–150k+ | $30k–120k+ |
| Indicative timeline | 6–12 wks | 8–14 wks | 10–28 wks | 8–16 wks | 12–28 wks | 6–18+ months | 10–20 wks | 10–20 wks | 10–20 wks |

Two patterns are worth noticing before the platform detail. First, the *simplest* platforms (Wix, Squarespace) carry surprisingly high export and SEO risk — locked-in simplicity is still lock-in. Second, the headless platforms (Contentful, Sanity, Strapi) export content easily but concentrate risk in the front end, where URLs, redirects, and SEO now live.

## Wix

**Typical profile.** Early-stage B2B; non-technical marketing team; simple site plus blog.

**Why companies outgrow it.** Performance ceilings, rigid templates, limited design and code control, and app-based integrations that become expensive and brittle.

**Migration difficulty.** High relative to site complexity, because there is no true "export my site." Moving off Wix is explicitly a rebuild, not a transfer. Blog content exports via RSS/XML; pages and images have no canonical export path.

**SEO/redirect risk.** High. Moving off Wix almost always changes URLs, and Wix's own redirect handling does not travel with you. Every URL must be inventoried and mapped 1:1 or traffic drops.

**Content modeling and media.** Modeling risk is low (the model is flat), but don't underestimate how much *implicit* structure — repeated page patterns — must be modeled explicitly in the new CMS. Images generally must be scraped or re-uploaded; variants and optimizations are lost.

**Workflow and integrations.** Roles are simple, so governance risk is low. Integrations are proprietary Wix apps; each needs an API-based replacement. Any custom Velo code is effectively unportable.

**Audit before rebuilding:** full URL inventory with traffic data; list of Wix apps and what each does; catalogue of recurring page patterns to inform the new content model.

## Squarespace

**Typical profile.** Design-led B2B — agencies, consultancies — with pages, blog, and light commerce.

**Why companies outgrow it.** Layout rigidity, limited developer access, constrained commerce, and no realistic path to multi-site or advanced personalization.

**Migration difficulty.** Medium-high. Blogs export as XML and products as CSV, but layouts, styles, and code do not export; templates are rebuilt. Version 7.1 removed some legacy export paths.

**SEO/redirect risk.** Medium-high. Squarespace does not export redirect rules; the redirect map must be built by hand from a URL inventory before anything else happens.

**Media and modeling.** Focal crops and responsive variants are typically lost. Modeling risk is low — the bigger danger is the opposite: a richer target CMS invites over-engineering. Constrain the new model to what the business actually needs.

**Audit before rebuilding:** URL inventory and redirect spreadsheet; product/image relationship map if commerce is involved; decision on which page layouts are worth recreating versus retiring.

## WordPress

**Typical profile.** Hybrid marketing/engineering teams; 50–500 pages; heavy plugin use; custom post types via ACF or page builders; several integrations.

**Why companies outgrow it.** Security and maintenance overhead, plugin conflicts, performance at scale, and the monolith coupling that blocks headless or multi-channel ambitions.

**Migration difficulty.** Deceptive. Core exports (XML/CSV) are the best in this list — but the *site* is usually a tangle of plugins, shortcodes, and serialized data that core exports don't capture. ACF fields and page-builder layouts are implicit content models that must be disentangled and redesigned. This is the single largest source of WordPress migration scope creep.

**SEO/redirect risk.** Medium-high. Theme and plugin changes can silently alter URLs, meta, and schema. Redirect plugins store rules in custom tables that must be exported, deduplicated, and reimplemented. Hardcoded internal links and embedded media URLs break when domains or paths change — plan for database-level search-and-replace.

**Workflow and integrations.** Custom roles and editorial plugins may have no equivalent in the target; each plugin integration becomes an API project.

**Audit before rebuilding:** plugin inventory split into must-replace / can-retire; explicit documentation of the implicit content model (every ACF group, post type, and builder pattern); redirect table export; media reference scan.

## Webflow

**Typical profile.** Design-first B2B — SaaS marketing sites, agencies — valuing visual editing and clean output.

**Why companies outgrow it.** CMS scale limits, per-site pricing across multiple properties, and needs Webflow can't host: programmatic SEO, user portals, complex personalization, backend logic.

**Migration difficulty.** Medium-high. Code export exists but does not include the CMS or runtime; collections export as CSV with rich text as HTML. Leaving Webflow means rebuilding the CMS layer and usually the front end.

**SEO/redirect risk.** Medium — the best in the builder class. Webflow's structure is explicit and its redirect tooling good, but those redirects live in Webflow; off-platform you must implement your own redirect layer (CDN/edge rules) and avoid chains.

**Media and modeling.** Assets export, but Webflow's responsive image pipeline (srcset variants) doesn't transfer. Collections and references are explicit — a genuine advantage — but cross-collection logic and conditional visibility need rethinking in the target.

**Audit before rebuilding:** collection schema export and reference map; inventory of custom code embeds and interactions; redirect list export; plan for reproducing image handling.

## Drupal

**Typical profile.** Technical B2B — SaaS, publishers, associations — with complex roles, multi-language content, and high security or performance requirements.

**Why companies outgrow it.** High development cost for changes, specialist talent scarcity, upgrade fatigue (D7→D10 era), and authoring UX that non-technical teams resist.

**Migration difficulty.** High to very high. Drupal data is deeply structured — nodes, fields, paragraphs, views, taxonomies — and richly relational. The Migrate API is powerful but technical; every entity and field must be mapped, and Drupal-specific concepts have no direct equivalent elsewhere.

**SEO/redirect risk.** Medium-high. Path aliases, taxonomy hierarchies, and module-dependent schema and sitemaps break easily in migration; Redirect module data must be recreated.

**Workflow and governance risk.** High — in an unusual direction. Drupal's granular permissions and workflows often *exceed* what the target platform offers. Migrating to a simpler CMS means consciously deciding which governance capabilities to give up; replicating them all is costly.

**Audit before rebuilding:** entity/field inventory with usage counts (much Drupal structure turns out to be unused); permission and workflow map with a keep/simplify decision per item; custom module and integration list; alias and redirect export.

## Adobe Experience Manager (AEM)

**Typical profile.** Large or upper-mid-market global B2B — manufacturing, tech, pharma — multi-brand, multi-region, invested in the Adobe ecosystem.

**Why companies outgrow it.** License and talent cost, slow release cycles, and platform overhead disproportionate to marketing-site needs. Many mid-market AEM installations were bought for a scale that never materialized.

**Migration difficulty.** Very high — the highest in this report. AEM's page/component model, workflows, permissions, and asset management are deeply proprietary. Adobe's Content Transfer Tool handles AEM-to-AEM-Cloud moves, not AEM-to-anything-else; outbound export is a custom engineering project.

**SEO/redirect risk.** High. Complex rendering, personalization, and multi-site, multi-language URL rules mean redirect governance is a project of its own — especially where previous migrations left redirect chains.

**Media, modeling, workflow.** Assets carry metadata, renditions, and Dynamic Media configuration that risk being lost outbound. Templates, components, and policies must be decomposed into the target's abstractions. Approval workflows and permissions — often the very reason AEM was bought — must be consciously re-engineered or simplified.

**Cost and timeline.** Enterprise-class: typically 6–18+ months and $150k–$500k+ including content and integrations; partner-reported three-year TCO for the platform itself often exceeds $1M for mid-size deployments.

**Audit before rebuilding:** integration map across the Adobe stack and legacy systems (usually the critical path); workflow/permission inventory with an explicit "what do we actually still need" review; asset metadata and rendition audit; a phased migration plan — big-bang AEM exits rarely go well.

## Contentful

**Typical profile.** Content-led, developer-heavy B2B with omnichannel delivery, multiple languages, and a composable stack.

**Why companies outgrow it.** Cost at scale, a sense of over-engineering for primarily-web use cases, and editor friction around preview and visual editing.

**Migration difficulty.** High — but for front-end reasons, not export reasons. Contentful's CLI/API export of content, assets, and content model is strong. The work is in reconciling years of content-model drift (types, validations, reference graphs) and rebuilding everything the CMS didn't own.

**SEO/redirect risk.** High, and this is the headless pattern worth internalizing: in a headless architecture, URLs, redirects, meta, schema, and sitemaps live in the *front end*. Migrating means rebuilding all of it, and documented headless migrations show 30–60% traffic drops when front-end SEO parity is not treated as a first-class workstream.

**Workflow and integrations.** Workflows are typically custom-built on webhooks and apps — each must be replicated or redesigned. Downstream consumers of the content API can break when data shapes change; coordinate the migration with every consumer.

**Audit before rebuilding:** content model audit and cleanup (migrate the model you want, not the one that accumulated); webhook/app inventory; list of API consumers and their expected payload shapes; front-end SEO parity checklist.

## Sanity

**Typical profile.** Developer-heavy B2B — SaaS, product marketing — where structured content is central and often feeds multiple channels.

**Why companies outgrow it.** Desire for stronger out-of-the-box visual editing, a different cost model, or a simpler stack with less custom front-end and Studio maintenance.

**Migration difficulty.** High. API and CLI tooling is solid, but Portable Text and rich custom schemas require careful migration scripts: nested objects, references, and images embedded inside Portable Text must be mapped precisely and validated in rendering.

**SEO/redirect risk.** High — the same headless pattern as Contentful. Routing and redirects are front-end responsibilities that must be rebuilt and tested.

**Workflow and integrations.** Custom Studio workflows must be redesigned; GROQ queries and response shapes consumed by other systems can break downstream apps.

**Audit before rebuilding:** schema inventory with a simplification pass (migration is the cheapest moment to reduce over-modeled complexity); Portable Text usage analysis; consumer/API dependency list.

## Strapi

**Typical profile.** Developer-heavy B2B startups and scale-ups; self-hosted headless; custom front ends; sometimes improvised multi-brand setups.

**Why companies outgrow it.** Need for more enterprise-grade permissions, more turnkey localization, less self-hosted maintenance burden, or stronger governance than the setup was built with.

**Migration difficulty.** Medium-high. There is no universal export; the standard path is custom ETL — scripting content out to JSON/CSV and into the target's APIs. The import-export plugin requires identical content types between environments, which rarely helps in a real migration.

**SEO/redirect risk.** Medium-high: standard headless front-end risks, plus a twist — because the stack was self-hosted, the CDN, caching, and redirect layers are also yours, and their migration must be planned alongside the CMS.

**Modeling, workflow, integrations.** Schema drift is common where governance was loose; roles and permissions are often customized and won't port cleanly; audit trails may be lost entirely. REST/GraphQL consumers break if response shapes change.

**Audit before rebuilding:** schema reconciliation between environments; infrastructure inventory (hosting, CDN, redirect rules, backups); permission policy documentation; API consumer list.

## What every migration has in common

Regardless of source platform, the same patterns recur:

- **SEO is the single biggest migration risk.** Broken links and lost 301s are the leading cause of post-migration ranking loss. Dedicate 15–20% of project effort to SEO preservation: redirect mapping, metadata and schema parity, sitemaps, and pre-cutover testing.
- **Content export is never complete.** You will lose template styling and behavior, responsive image variants, and plugin- or module-specific metadata. Budget for the rebuild, not the transfer.
- **Content model drift is universal.** Every mature CMS accumulates ad-hoc fields and relationships. Migration forces a reckoning: reconcile the drift or deliberately simplify. A good migration decides what should not move.
- **Integrations are chronically underestimated.** Everything that was "just a plugin" becomes an API project. List every system that reads from or writes to the CMS before scoping anything.
- **Workflow mismatches cause organizational friction.** Moving from flat permissions to granular ones stalls adoption; moving the other way silently removes governance.

## The pre-rebuild checklist

Before selecting a target platform — not after — complete these:

1. **Full URL, content, and asset inventory.** Crawl everything; capture status codes, backlinks, and top-traffic pages. This becomes the redirect map and the QA baseline.
2. **SEO baseline and protection plan.** Current rankings, traffic by page, internal linking, sitemaps, schema. Require 1:1 redirects (or explicit, mapped consolidations) and front-end parity for meta, canonicals, hreflang, and structured data.
3. **Integration and data-flow audit.** Every system reading from or writing to the CMS, with payload shapes and a keep/replace/retire decision each.
4. **Deliberate content model.** Design the target model from the audit, simplified on purpose. Validate it with the editors who will live in it.
5. **Legacy retirement plan.** Keep the old platform running with 301s and monitoring for 60–90 days post-launch; use log analysis to catch missed redirects.
6. **Scope fences.** The classic overrun drivers are locales added mid-project, "one more" integration, and content-model creep. Define a minimum viable launch and defer the rest.
7. **A neutral platform-fit check.** If you are leaving because of cost or complexity, verify the target actually fixes that for your volumes, locales, and team skills — otherwise you are financing a lateral move.

With the departure risk understood, the next two chapters turn to the destination: first the CMS categories, then the platform-by-platform comparison.
