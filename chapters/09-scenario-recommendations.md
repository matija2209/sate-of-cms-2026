# Scenario-Based Recommendations

Frameworks are only useful when they land on your actual situation. This chapter works through the eleven scenarios mid-market B2B teams most often bring to a CMS decision. Each follows the same structure: the situation, the key risks, what the CMS must do, which categories to consider, which to be careful with, and — most importantly — the next step to take *before* choosing a platform.

Two reminders frame everything below. The best CMS is not universal: the right answer depends on your content model, workflows, ownership, and operating model. And "categories to be careful with" means exactly that — not "never," but "make this platform prove it fits your case."

## 1. Simple B2B marketing site

**Situation.** A focused site — product pages, a few landing pages, lead-gen forms feeding HubSpot or Marketo. Marketing-led, minimal engineering.

**Key risks.** Over-engineering: buying composable architecture for a brochure-plus site; paying for unused features; slow time-to-market from unnecessary complexity.

**Requirements.** Easy visual editing, native or low-effort CRM/MAP integration, low maintenance, fast setup.

**Consider:** marketing-centric SaaS and visual builders (Webflow, HubSpot-style CMS, well-managed WordPress).
**Careful with:** headless in any flavor (complexity without payoff at this stage), enterprise anything.

**Next step:** audit your CRM/MAP integration requirements and honest marketing headcount before evaluating platforms — those two facts eliminate most of the market.

## 2. Content-heavy SEO website

**Situation.** Hundreds of blog posts, resources, and landing pages; organic search is a primary revenue driver.

**Key risks.** Slow rendering suppressing rankings; messy taxonomy; inability to manage redirects and metadata at scale.

**Requirements.** Fast front-end delivery (static or hybrid rendering), fine-grained control of URLs, structured data, canonical and redirect management, bulk editing, disciplined taxonomy.

**Consider:** API-first headless (Contentful, Sanity, Payload) with a modern front end (Next.js, Astro) for maximum performance control; a well-optimized WordPress or similar remains viable when in-platform SEO tooling and team familiarity outweigh rendering control.
**Careful with:** heavy client-side-rendered stacks, and any headless plan that doesn't explicitly budget the SEO plumbing (Chapter 7's recurring caveat).

**Next step:** run a technical SEO audit and quantify what current page speed and crawl issues cost in traffic — that number sizes the business case and the budget.

## 3. Company outgrowing WordPress

**Situation.** The site is slow, plugins conflict, security is a standing worry, and custom post types strain under scale. The team knows the symptoms from Chapter 5.

**Key risks.** Migration fatigue; losing hard-earned URL equity; underestimating the front-end development a headless move requires; recreating the same plugin sprawl on a new platform.

**Requirements.** Structured content modeling, a stronger security model, component-based architecture, an editorial experience WordPress-trained editors can accept.

**Consider:** visual headless (Storyblok-style) or a structured hybrid CMS for the gentlest editor transition; code-first headless (Payload, Sanity) where engineering capacity is strong. Well-governed enterprise WordPress hosting is also a legitimate answer when the problem is hygiene rather than architecture.
**Careful with:** jumping to another monolith with the same governance gaps, or to raw code-only headless that leaves editors worse off than Gutenberg.

**Next step:** inventory every plugin and split it into must-replace functionality versus habit. That list is your real migration scope — and often shrinks the project by a third.

## 4. Webflow site needing backend or product logic

**Situation.** Webflow served the design-led marketing site well, but the roadmap now includes user logins, gated portals, dynamic filtering, or complex data relationships.

**Key risks.** The workaround trap — Airtable-plus-Zapier chains that get fragile and expensive; data syncing failures; hitting Webflow's CMS scale limits.

**Requirements.** A real relational data model, API extensibility, authentication, custom logic.

**Consider:** application-grade headless — Payload CMS is a natural fit here (content plus auth plus custom backend logic in one self-hosted codebase), as are backend-as-a-service pairings that keep Webflow as the presentation layer.
**Careful with:** pure visual builders (moving sideways), and pretending one more automation tool will hold.

**Next step:** write down the exact data schema and auth requirements. That document reveals whether you need a CMS with application features or a true backend — they are different purchases.

## 5. Multi-locale website

**Situation.** Expanding into EMEA or APAC: localized content, regional translators, hreflang, per-market SEO.

**Key risks.** Translation bottlenecks; cloned content structures that drift; the wrong locale ranking in the wrong market; costs that scale badly past the third locale.

**Requirements.** Native localization workflows (field-level preferred), TMS integration, localized routing and slugs, locale-scoped permissions, fallback logic.

**Consider:** global-ready headless (Contentful, Sanity, Storyblok, Payload) or localization-strong coupled platforms (Drupal; WordPress+WPML; Webflow's native localization for design-led teams).
**Careful with:** basic builders without real i18n, and any platform where localization is a bolted-on plugin you haven't tested at your locale count.

**Next step:** select your translation management approach *before* the CMS, then run the Chapter 8 localization prototype — two locales, one market microsite, full TMS round-trip.

## 6. Multi-brand website portfolio

**Situation.** A holding company or post-M&A group needs distinct sites for three or more brands, ideally sharing components, content, and governance.

**Key risks.** Brand bleed from weak permission scoping; paying for parallel CMS licenses and duplicated dev work; duplicate content damaging SEO across the portfolio; expensive divestiture later.

**Requirements.** Multi-tenant or multi-site architecture, brand-scoped RBAC, shared component libraries with brand theming, per-brand domains and deployment.

**Consider:** multi-tenant headless (Payload's multi-tenant plugin, Contentful spaces, Contentstack-class enterprise SaaS), Drupal multisite/Domain Access; AEM where scale and budget are genuinely enterprise.
**Careful with:** single-tenant monoliths multiplied per brand, and fleets of disconnected builder sites — both recreate the fragmentation you're trying to solve.

**Next step:** map shared versus brand-specific content and components (the Chapter 8 exercise). Your tenant strategy falls out of that map — and it, not the vendor, is the architecture.

## 7. Company leaving AEM or Drupal

**Situation.** A heavy enterprise implementation — often six figures and 18+ months — that is too slow to change and requires scarce, expensive specialists.

**Key risks.** Repeating the mistake by buying another enterprise box; massive content migration cost (Chapter 5 rates AEM exit as the hardest in this report); losing governance capabilities the organization actually relies on.

**Requirements.** Faster time-to-value, materially lower TCO, a modern editor experience, composable architecture — while preserving the workflows and permissions that were the original purchase rationale.

**Consider:** mid-market headless and composable platforms (Contentful, Storyblok, Sanity, Payload) sized to what you actually use; phased migration, never big-bang.
**Careful with:** "enterprise-lite" monoliths that reproduce the cost structure at a discount, and heavily customized open-source that recreates the specialist-dependency problem with different specialists.

**Next step:** calculate the true three-year TCO of the outgoing platform — license, partners, internal time. That number sets a realistic budget and, presented honestly, is usually what unlocks executive support.

## 8. Comparing Contentful, Sanity, and Payload

**Situation.** Engineering has already decided on headless; the shortlist debate has stalled into analysis paralysis.

**Key risks.** Choosing on developer sentiment rather than marketing fit; underestimating the front-end and editorial-UX build cost that all three share.

**How they differ (in one line each).** Contentful: the structured, enterprise-governed option — strongest compliance artifacts and multi-space governance; highest cost trajectory. Sanity: the flexible, schema-as-code option — deepest customization of the editing experience, which you must build and maintain. Payload: the code-native, self-hostable option — full data ownership, Next.js-native, multi-tenant strength; the editorial experience and infrastructure are yours.

**Decision drivers.** Data-residency/self-hosting mandate → Payload. Enterprise compliance and vendor-managed governance → Contentful. Bespoke editorial workflows and content-as-product ambitions → Sanity. Cost shape: Contentful scales with usage/seats; Sanity per-seat with usage add-ons; Payload shifts spend to infrastructure and engineering.

**Next step:** build a working prototype of your *most complex* page type — localized, componentized, previewed — in your actual front-end framework on the top two candidates. Two weeks of prototyping resolves what months of matrix debate cannot.

## 9. Self-hosting and data ownership requirements

**Situation.** Regulated industry (FinServ, HealthTech) or strict data-residency policy; IT mandates no multi-tenant SaaS.

**Key risks.** The infrastructure and patching burden landing on a team that didn't sign up for it; security responsibility fully internalized (Chapter 8's responsibility boundary, entirely on your side).

**Requirements.** Source access, VPC or private-cloud deployment, strict data isolation, exportability by design.

**Consider:** open-source headless (Payload, Strapi, Directus) and self-hosted traditional (Drupal, WordPress) — with managed open-source hosting as the middle path where the mandate allows.
**Careful with:** multi-tenant SaaS of any kind, however good the certifications, if the mandate is hard; and self-hosting without a named owner for patching and incident response.

**Next step:** get the data-residency and isolation requirements from InfoSec *in writing* before evaluating features. Vague mandates produce expensive over-compliance or dangerous under-compliance.

## 10. Strong marketing autonomy needed

**Situation.** Marketing is blocked by a developer ticket backlog for routine landing pages and form changes; shadow pages are appearing in outside tools.

**Key risks.** Solving autonomy with an ungoverned page builder (trading the queue for debt — Chapter 8's failure mode); breaking the design system; shadow IT becoming permanent.

**Requirements.** Visual page building with live preview, drag-and-drop *within* design constraints, publishing workflows that don't route through engineering.

**Consider:** visual headless (Storyblok, Builder.io-class), Webflow, or hybrid marketing SaaS — all structured around component-constrained autonomy.
**Careful with:** code-only headless out of the box (the ticket queue survives the migration), and free-form builders without component governance.

**Next step:** finalize and document the design system and component library *before* handing marketing a visual builder. The guardrails have to exist before the autonomy.

## 11. Custom workflows and heavy integrations

**Situation.** Content requires multi-stage approval (legal, product, compliance, marketing); the site pulls from PIM, ERP, or product systems.

**Key risks.** Buying rigid workflow features that can't model your actual process; brittle hard-coded integrations that become permanent maintenance debt.

**Requirements.** Customizable workflow states, robust webhooks and APIs, an integration framework or marketplace, audit trails across the approval chain.

**Consider:** enterprise-capable headless (Contentful and peers) for orchestrated composable stacks; code-first platforms (Payload) where workflows and integrations are genuinely custom business logic; Drupal where deep workflow needs meet open-source governance.
**Careful with:** basic marketing SaaS and template builders — their workflow ceiling arrives fast — and any platform whose "integration" story is a Zapier link.

**Next step:** map the approval state machine and list every external data source before shortlisting. The platform must fit the map, not the reverse.

## Summary table

| Scenario | Consider | Careful with | Next step before choosing |
|---|---|---|---|
| 1. Simple marketing site | Marketing SaaS, visual builders | All headless, enterprise DXP | Audit CRM/MAP needs and headcount |
| 2. SEO-heavy site | Headless + fast front end; optimized WP | Client-heavy JS; unbudgeted headless SEO | Technical SEO audit with revenue impact |
| 3. Outgrowing WordPress | Visual headless, hybrid; code-first if dev-strong | Another monolith; raw code-only headless | Plugin inventory: must-have vs. habit |
| 4. Webflow + backend needs | Application headless (Payload), BaaS pairing | More visual builders, workaround chains | Write the data schema and auth spec |
| 5. Multi-locale | Global-ready headless; Drupal, WP+WPML, Webflow i18n | Builders without real i18n | Choose TMS first; run 2-locale prototype |
| 6. Multi-brand | Multi-tenant headless, Drupal, AEM (at scale) | Per-brand monoliths, builder fleets | Map shared vs. brand-specific content |
| 7. Leaving AEM/Drupal | Mid-market headless, phased migration | Enterprise-lite boxes, over-customized OSS | Compute the outgoing platform's real 3-yr TCO |
| 8. Contentful vs. Sanity vs. Payload | Prototype the top two | Deciding on sentiment | Build your hardest page type in both |
| 9. Self-hosting mandate | Payload, Strapi, Directus, Drupal, WP | Multi-tenant SaaS; ownerless self-hosting | Written residency requirements from InfoSec |
| 10. Marketing autonomy | Visual headless, Webflow, hybrid SaaS | Ungoverned builders; code-only headless | Component library before the builder |
| 11. Custom workflows/integrations | Enterprise headless, code-first, Drupal | Rigid SaaS workflows, Zapier-grade integration | Map the state machine and data sources |

If several scenarios describe you at once — outgrowing WordPress *and* going multi-locale *and* needing autonomy is a common trio — resolve them in this order: hard constraints first (self-hosting, compliance), then architecture (multi-brand/locale/backend), then experience (autonomy, editor UX). Constraints eliminate categories; architecture picks the category; experience picks the platform. The next chapter provides self-assessment tools to run that sequence on your own numbers.
