1) Full matrix (ratings only)
=============================

Legend: Strong | Medium | Weak (no fake numerical scores)

Notes
- Marketing autonomy = can non‑technical marketing staff independently build/adjust pages, campaigns, redirects, A/B, personalization without a developer ticket.
- Developer control = ability to shape data model, APIs, auth, and infrastructure with minimal constraints.
- Multi‑brand support = can manage multiple distinct brands/properties from one platform or installation without major hacks.
- Multi‑locale support = mature i18n/l10n (content and often UI) for several markets/languages.
- SEO control = fine‑grained control over URLs, metadata, redirects, sitemaps, hreflang, and structured data.
- Self‑hosting/data ownership = option to run on your own infra; you can export your data.
- Security/governance = enterprise‑ready auth (SSO/SAML), RBAC, audit logging, compliance artifacts, and admin workflows.
- Integration flexibility = API‑first/webhooks, marketplace/apps, and ability to connect to CRMs/MAPs/ERPs/etc.
- Implementation cost = typical one‑off build cost (relative to mid‑market B2B).
- Maintenance cost = typical ongoing run cost (relative to mid‑market B2B).
- Migration complexity = how hard it is to migrate from something else (or to something else later).
- Long‑term flexibility = how future‑proof the architecture is (headless, multi‑channel, composability).
- Best‑fit company type = typical mid‑market org profile where it shines.
- Where it becomes limiting = first signs of strain or deal‑breakers.

Matrix
Platform | Marketing autonomy | Developer control | Multi‑brand | Multi‑locale | SEO control | Self‑hosting/data ownership | Security/governance | Integration flexibility | Implementation cost | Maintenance cost | Migration complexity | Long‑term flexibility | Best‑fit company type | Where it becomes limiting
--- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | ---
WordPress | Strong | Strong | Medium | Medium | Strong | Strong | Medium | Strong | Medium | Medium | Medium | Strong | Marketing‑led B2B with internal dev capacity; multi‑site corporate blog/microsites | Governance at scale needs custom tooling; multisite upgrades and plugin conflicts become expensive; plugin security requires ongoing discipline.
Webflow | Strong | Medium | Medium | Medium | Strong | Weak | Medium | Medium | Low–Medium | Medium | Medium–High | Medium | Marketing‑led teams wanting speed and clean output; fewer dev resources; campaign/microsites, regional sites with moderate complexity | No self‑hosting; coupling to Webflow hosting and rendering limits very custom front‑ends or embedded app‑like experiences; at very high scale or complex workflows, you hit platform limits.
Drupal | Weak | Strong | Strong | Strong | Strong | Strong | Strong | Strong | Medium–High | Medium | Medium–High | Strong | Dev‑centric B2B with complex content models, multi‑brand/locale, strong governance and compliance needs; often public sector or regulated industries | High upfront cost and specialized talent needed; authoring UX is weaker; upgrades and multisite management require care; smaller teams will feel the maintenance burden.
AEM (Adobe Experience Manager) | Medium | Medium | Strong | Strong | Strong | Medium | Strong | Strong | High | High | High | Strong | Large, complex B2B enterprises needing deep Adobe ecosystem integration, multi‑brand/multi‑locale, and formal governance; often already in Adobe stack | High cost and long timelines; vendor lock‑in to Adobe licensing and cloud model; overkill for mid‑market that isn’t heavily multi‑brand; upgrades/migrations are non‑trivial and AEM 6.5 support is closing in 2026.
Contentful | Medium | Strong | Strong | Strong | Medium | Weak | Strong | Strong | Medium–High | Medium–High | Medium | Strong | B2B with multiple brands/regions and a dedicated dev team wanting headless composability; marketing wants some self‑service via apps but leans on dev | Cloud‑only; marketing autonomy depends on apps/custom studio widgets; cost can scale steeply with usage and spaces; heavy reliance on devs for anything non‑standard.
Sanity | Weak | Strong | Medium | Strong | Medium | Weak | Medium | Strong | Medium–High | Medium | Medium | Strong | Dev‑heavy B2B building bespoke digital products, complex content models, or AI‑driven workflows; content often feeds non‑web channels | Studio is a React app you maintain; marketing autonomy is low without heavy custom UI; localization is flexible but requires modeling work; no self‑hosted backend.
Storyblok | Medium | Strong | Medium | Strong | Medium | Weak | Medium | Strong | Medium | Medium | Medium | Strong | Marketing+dev B2B teams wanting visual editing with headless flexibility; multi‑locale and component‑driven sites | Cloud‑only; scaling many brands/tenants can become costly and complex; advanced governance requires implementation work.
Strapi | Weak | Strong | Weak | Medium | Medium | Strong | Medium | Strong | Medium | Medium | Medium | Strong | B2B teams with strong dev capacity that want a self‑hosted, API‑first CMS and plan to build most UI/SEO/preview themselves | No visual page building out of the box; multi‑brand typically means multiple projects; marketing autonomy is low; upgrades/maintenance of self‑hosted stack consume dev time.
Directus | Weak | Strong | Medium | Medium | Medium | Strong | Medium | Strong | Medium | Medium | Medium | Strong | B2B with existing databases or data‑heavy products needing an instant admin/API layer; dev‑centric | Limited visual page editing; SEO is mostly a frontend concern; marketing autonomy is low; multi‑brand/tenancy architecture needs design (Hub can help but adds complexity).
Payload CMS | Weak | Strong | Strong | Strong | Medium | Strong | Medium | Strong | Medium | Medium | Medium | Strong | B2B dev teams that want code‑first, TypeScript‑native CMS with strong multi‑tenancy and headless flexibility | No GUI schema builder—admins can’t add fields without dev deployment; marketing autonomy is low; preview/visual editing must be built; smaller teams may find ongoing maintenance heavy.

2) Notes explaining each rating
==============================

WordPress
- Marketing autonomy: Strong. Classic editor or Gutenberg + page builders give marketing broad control over layouts and campaign pages; plugins like Rank Math give SEO fields directly in‑editor. Core is open source and free to self‑host anywhere【turn5search19】.
- Developer control: Strong. Full filesystem access, custom plugins, REST API, and a large ecosystem; multisite networks provide centralized control with per‑site flexibility【turn5search0】【turn5search3】.
- Multi‑brand: Medium. Multisite supports multiple domains and separate sites from one install, but there’s no built‑in brand‑level governance UI; it’s often used for multi‑brand, but setup and customization are on you【turn5search0】【turn5search3】.
- Multi‑locale: Medium. Multilingual is plugin‑driven (e.g., WPML, Polylang, Weglot). WPML integrates with popular SEO plugins like Yoast and Rank Math for multilingual SEO fields, but features and costs vary by plugin and scale【turn2search10】【turn2search13】【turn5search8】【turn5search9】.
- SEO control: Strong. Mature ecosystem with tools like Rank Math that provide per‑page metadata, sitemaps, schema, redirects, and import from other SEO plugins【turn2search14】.
- Self‑hosting/data ownership: Strong. WordPress.org is GPL‑licensed and can be hosted anywhere; you own the DB and can export at any time【turn5search19】.
- Security/governance: Medium. Secure when properly managed, but security depends on hosting, plugin choices, and ops discipline; enterprise hardening requires WAF, SSO, audit logging, and process controls【turn5search11】【turn5search12】【turn5search14】.
- Integration flexibility: Strong. Huge plugin ecosystem and REST API enable CRM/MAP/ERP integrations; headless builds are also common.
- Implementation cost: Medium. Low software cost but high variability based on custom dev, plugins, and agency rates.
- Maintenance cost: Medium. Requires patching core/plugins, security monitoring, and performance tuning; managed hosts and enterprise platforms (e.g., WordPress VIP) help but add cost【turn0search2】.
- Migration complexity: Medium. Migrating into WordPress is relatively easy; large multisite/plugin stacks make future migrations more involved.
- Long‑term flexibility: Strong. Can run traditional, headless, or hybrid; massive ecosystem and community; multisite and decoupled options keep it adaptable【turn5search3】【turn0search0】.
- Best‑fit company type: Marketing‑led B2B with dev capacity; corporate sites, blogs, and multi‑site microsites.
- Where it becomes limiting: Governance at scale needs custom tooling; plugin conflicts and multisite upgrades; dependence on third‑party plugins for SEO/i18n.

Webflow
- Marketing autonomy: Strong. Visual builder and built‑in CMS, plus localization, allow marketers to launch and iterate pages with minimal dev【turn3search0】【turn3search3】.
- Developer control: Medium. Developers can export code and script within constraints, but you’re ultimately bound to Webflow’s rendering and hosting environment.
- Multi‑brand: Medium. Enterprise tier supports multi‑region/multi‑brand workflows and localization, but it’s not a full multi‑tenant control plane like AEM MSM; at scale you may need multiple projects or workarounds【turn3search5】【turn4search2】.
- Multi‑locale: Medium. Native localization supports multiple locales with per‑element translation and third‑party TMS integrations; however, ecommerce features currently don’t support localization【turn3search0】【turn3search3】.
- SEO control: Strong. SEO fields at page and CMS‑item level, sitemap, and 301 redirects (including wildcards) support solid SEO; Core Web Vitals are often strong due to managed edge hosting【turn3search12】【turn3search9】【turn3search10】【turn0search8】.
- Self‑hosting/data ownership: Weak. Webflow is SaaS with managed hosting; no self‑hosted option. You can export site code/assets, but the CMS runtime is Webflow‑only.
- Security/governance: Medium. SOC 2 Type II and ISO 27001 certifications, SSO, and granular permissions at Enterprise tier increase governance confidence【turn3search14】【turn3search16】.
- Integration flexibility: Medium. Good external integrations via Webflow Apps/APIs, but deep backend hooks are limited compared to API‑first headless.
- Implementation cost: Low–Medium. For standard sites, launch is fast; complex/headless setups add cost.
- Maintenance cost: Medium. Platform handles infra/patching, but large redirect sets and complex localization require ongoing care.
- Migration complexity: Medium–High. Import tools exist, but large Webflow sites with complex logic can be tedious to migrate out due to bespoke interactions and custom code snippets.
- Long‑term flexibility: Medium. Great for web and localized web experiences; less ideal if you need non‑web channels or deeply custom backends.
- Best‑fit company type: Marketing‑heavy B2B that wants speed, clean code, and strong performance with modest dev capacity.
- Where it becomes limiting: No self‑hosting; scaling many brands or deeply interactive app‑like experiences runs into platform constraints.

Drupal
- Marketing autonomy: Weak. Out‑of‑the‑box authoring is more technical; layout and UX often require dev or site‑builder expertise.
- Developer control: Strong. Extremely configurable content models, workflows, and multisite architecture; supports headless via JSON:API/REST【turn0search11】【turn0search14】.
- Multi‑brand: Strong. Multisite lets separate sites share a codebase while having separate databases and configs—good for multi‑brand portfolios【turn9search0】.
- Multi‑locale: Strong. Core multilingual features (Content Translation, Configuration Translation, interface translation) and modules like Metatag support robust i18n and hreflang SEO【turn2search15】【turn9search6】.
- SEO control: Strong. Modules like Pathauto, Metatag, Redirect, and Simple XML Sitemap give precise control over URLs, metadata, redirects, and sitemaps【turn2search15】【turn2search17】【turn2search19】.
- Self‑hosting/data ownership: Strong. Open source; self‑hosted by default; you control the database and infra.
- Security/governance: Strong. Strong security community and advisories; supports SSO, granular RBAC, and workflow/content moderation; often used by government/regulated orgs【turn9search10】【turn0search12】.
- Integration flexibility: Strong. REST/JSON:API and wide module ecosystem support deep integrations with CRMs, ERPs, etc【turn0search14】.
- Implementation cost: Medium–High. Cheaper software, but specialized talent and configuration drive up cost.
- Maintenance cost: Medium. Core/module updates and security patches are manageable but require Drupal expertise; hosting/platforms help.
- Migration complexity: Medium–High. Importing from other CMS is doable, but complex data/feature sets and custom code make migrations non‑trivial.
- Long‑term flexibility: Strong. Proven at scale in government and enterprise; supports headless and composable architectures【turn0search10】【turn0search12】.
- Best‑fit company type: Dev‑centric B2B with complex content, governance, and multi‑brand/multi‑locale; public sector and regulated industries.
- Where it becomes limiting: Authoring UX and talent scarcity; higher setup/maintenance overhead for smaller teams.

AEM (Adobe Experience Manager)
- Marketing autonomy: Medium. The authoring environment is powerful once configured, but governance rules, templates, and workflows usually require implementation partners to set up.
- Developer control: Medium. You can extend AEM extensively (OSGi, Sling, HTL, APIs), but within the boundaries of Adobe’s architecture and, increasingly, cloud cadence.
- Multi‑brand: Strong. Multi Site Manager (MSM) and Live Copy let you centralize blueprints and roll out changes across brands and regions from one authoring source【turn8search1】【turn8search3】.
- Multi‑locale: Strong. MSM and translation workflows support multinational and multilingual sites, including automation and TMS integration【turn0search15】【turn8search1】.
- SEO control: Strong. Detailed SEO guidance and URL management practices; custom components can emit any needed metadata and structured data【turn0search16】.
- Self‑hosting/data ownership: Medium. AEM 6.5 on‑prem remains available for some use cases, but Adobe is pushing AEM as a Cloud Service; data exportability is good, but you don’t “own” the SaaS platform【turn4search14】【turn4search17】.
- Security/governance: Strong. Enterprise features (SSO, detailed audit logging, permissions) and hardening checklists reflect enterprise expectations【turn8search4】【turn8search5】【turn8search6】.
- Integration flexibility: Strong. Deep integration into Adobe Experience Cloud (Assets, AEP); APIs and App Builder/AEM Extensions enable custom integrations.
- Implementation cost: High. Licensing, SI costs, and timeline are substantial; benchmarks show six‑figure annual costs are common【turn4search18】.
- Maintenance cost: High. Cloud subscription scales with usage (page views, API calls); upgrades are continuous but require change management【turn8search9】【turn4search17】.
- Migration complexity: High. Large AEM programs (e.g., 180 sites) require careful planning; AEM 6.5 support windows are closing, making migrations pressing【turn8search16】【turn8search15】【turn8search17】.
- Long‑term flexibility: Strong. Designed for large, global, multi‑brand deployments and composable experiences when used headless/hybrid.
- Best‑fit company type: Large, complex B2B with Adobe stack investments and formal governance needs; heavy multi‑brand/multi‑locale.
- Where it becomes limiting: Cost and complexity; overkill for mid‑market without multi‑brand scale or Adobe ecosystem dependency.

Contentful
- Marketing autonomy: Medium. Non‑technical users can manage content; some autonomy via Apps Marketplace, but complex behaviors need dev work.
- Developer control: Strong. Content modeling, APIs, webhooks, and apps provide strong flexibility; schema‑as‑code with CLI supports CI/CD【turn1search2】.
- Multi‑brand: Strong. Multi‑site management and multi‑brand solutions let different brands/regions retain unique identity while sharing infrastructure【turn4search0】【turn4search2】.
- Multi‑locale: Strong. Built‑in localization with per‑field or per‑content‑type locale support; faster to implement than modeling‑your‑own i18n【turn1search3】.
- SEO control: Medium. All SEO metadata is modelable and deliverable, but SEO tooling is mostly via apps/third‑party rather than built‑in.
- Self‑hosting/data ownership: Weak. SaaS only; you can export content, but you can’t self‑host the Contentful platform.
- Security/governance: Strong. SOC 2 Type 1 (working toward Type 2), RBAC, SSO, and a security addendum reflect enterprise controls【turn10search0】【turn10search1】【turn10search2】.
- Integration flexibility: Strong. 250+ apps and an API‑first approach make integrations with MAP/CRM/search robust【turn1search0】.
- Implementation cost: Medium–High. Build is moderate, but enterprise pricing is negotiated and often five/six figures annually; usage‑based costs can add 20–50% at scale【turn4search5】【turn4search8】.
- Maintenance cost: Medium–High. Platform maintenance is handled, but managing multiple spaces, environments, and apps incurs overhead.
- Migration complexity: Medium. Export APIs and CLI help, but complex content models and relationships mean migrations aren’t trivial.
- Long‑term flexibility: Strong. Headless and composable by design; supports multi‑channel delivery and AI personalization via Ninetailed acquisition【turn1search0】.
- Best‑fit company type: Multi‑brand/multi‑region B2B with dev capacity and need for omnichannel content.
- Where it becomes limiting: Cloud‑only; costs can climb with spaces/usage; marketing autonomy is bounded by app/widget dev capacity.

Sanity
- Marketing autonomy: Weak. Studio is a React app you customize; out‑of‑the‑box, editors don’t have visual page building without dev investment.
- Developer control: Strong. Schema‑as‑code, Portable Text, GROQ, and Studio customization offer deep control【turn1search7】.
- Multi‑brand: Medium. You can model multiple brands via datasets/spaces or workspaces, but it’s not a first‑class “brands” concept like AEM MSM; needs design.
- Multi‑locale: Strong. Flexible localization patterns (field‑level or document‑level) via plugins; scales to many languages【turn6search0】【turn6search1】【turn6search2】.
- SEO control: Medium. All SEO fields are modelable, but you must build preview/slug generation and frontend rendering yourself.
- Self‑hosting/data ownership: Weak. Content Lake is SaaS; Studio can be self‑hosted, but the backend is not. No full on‑prem offering【turn6search10】【turn6search11】.
- Security/governance: Medium. SOC 2 Type 1 and GDPR compliance with data retrieval/deletion APIs, plus roles and document‑level permissions【turn6search9】【turn1search5】.
- Integration flexibility: Strong. GROQ webhooks, APIs, and an ecosystem of integrations (e.g., Algolia via webhooks) enable broad connectivity【turn6search14】【turn6search15】.
- Implementation cost: Medium–High. Free tier exists, but serious projects need Studio customization and frontend builds.
- Maintenance cost: Medium. Platform maintenance is handled, but Studio and pipeline maintenance consume dev time.
- Migration complexity: Medium. Content portability is good via APIs; complexity lies in re‑implementing Studio customizations and preview.
- Long‑term flexibility: Strong. Highly composable, strong for AI‑heavy and multi‑channel use cases【turn1search8】.
- Best‑fit company type: Dev‑heavy B2B building custom digital products; AI‑driven workflows or multi‑channel content.
- Where it becomes limiting: Marketing autonomy is low without heavy UI investment; no self‑hosted backend.

Storyblok
- Marketing autonomy: Medium. Visual editor gives marketers wysiwyg, component‑based editing, which is unusual among headless CMS options【turn1search10】.
- Developer control: Strong. API‑first, component schema, and webhook/API integrations support flexible architectures【turn1search10】.
- Multi‑brand: Medium. Multi‑space management enables brand/region separation and component/content staging, but it’s space‑based rather than native multi‑brand with shared blueprints【turn4search9】.
- Multi‑locale: Strong. i18n via field‑level or space‑level translation with AI‑assisted translation and CLI/Management API to sync across spaces【turn4search10】.
- SEO control: Medium. SEO fields are modelable and delivered via API, but SEO tooling is largely in your frontend.
- Self‑hosting/data ownership: Weak. Cloud‑first; you can export content, but there’s no self‑hosted Storyblok server【turn1search13】.
- Security/governance: Medium. Enterprise plan includes roles and basic controls; Storyblok publishes security thought leadership, but detailed compliance artifacts (SOC 2/ISO) aren’t as prominent as larger vendors【turn1search11】【turn1search12】.
- Integration flexibility: Strong. Visual editor, apps, and APIs support common integrations; headless model lets you connect anything.
- Implementation cost: Medium. Free plan available; paid tiers start around $90/month with custom Enterprise pricing; implementations typically 6–16 weeks depending on complexity【turn4search11】.
- Maintenance cost: Medium. Platform maintenance handled; complex multi‑space setups require some operational discipline.
- Migration complexity: Medium. Import/export and APIs help, but component and schema alignment must be rebuilt elsewhere.
- Long‑term flexibility: Strong. Headless, component‑driven, with growing AI features; suits composable stacks.
- Best‑fit company type: Marketing+dev B2B teams wanting visual editing and headless; multi‑locale sites.
- Where it becomes limiting: Cloud‑only; scaling many brands or heavy personalization can increase cost/complexity.

Strapi
- Marketing autonomy: Weak. Admin panel is for structured content; there’s no visual page builder without custom work.
- Developer control: Strong. REST/GraphQL APIs, plugin system, and self‑hosting give devs significant control【turn7search0】.
- Multi‑brand: Weak. No native multi‑tenant; multi‑brand typically means separate projects or custom architectures on top【turn1search15】.
- Multi‑locale: Medium. Built‑in i18n plugin supports per‑content‑type/field localization across many locales【turn7search5】【turn7search6】【turn7search7】.
- SEO control: Medium. SEO fields are modelable, but SEO tooling (slugs, redirects, sitemaps, hreflang) must be built on the frontend.
- Self‑hosting/data ownership: Strong. Open source; self‑hosting or Strapi Cloud; Enterprise Edition for self‑hosted enterprise features【turn7search0】【turn1search16】.
- Security/governance: Medium. RBAC and plugins for SSO exist, but audit/compliance tooling is less mature than enterprise SaaS; you must patch and secure infra yourself【turn1search16】.
- Integration flexibility: Strong. API‑first and marketplace provide strong integration options【turn7search0】.
- Implementation cost: Medium. No license fee for self‑host; main cost is dev time to build admin/UI/preview and integrations.
- Maintenance cost: Medium. Self‑hosting requires dev hours for patching, backups, and scaling; Strapi Cloud reduces this but adds subscription【turn1search16】.
- Migration complexity: Medium. Export/import and APIs ease data moves; logic must be reimplemented.
- Long‑term flexibility: Strong. Self‑hosted, API‑first, and plugin ecosystem suit custom stacks.
- Best‑fit company type: Dev‑centric B2B comfortable building most of the UX and SEO themselves.
- Where it becomes limiting: Marketing can’t self‑serve page composition; multi‑brand requires custom work.

Directus
- Marketing autonomy: Weak. Data Studio is powerful for data, not visual page editing.
- Developer control: Strong. SQL/NoSQL support, schema‑as‑code snapshots, and RBAC/permissions give devs deep control【turn2search1】.
- Multi‑brand: Medium. Multi‑tenant patterns exist (e.g., Directus Hub with shared/DB models and row‑level security), but they require architectural decisions【turn2search0】.
- Multi‑locale: Medium. Content translations are possible via translation strings or extensions (e.g., Localazy plugin), but i18n isn’t as turnkey as some competitors【turn7search15】【turn7search18】.
- SEO control: Medium. All SEO metadata is modelable, but rendering, slugs, and redirects live in your frontend.
- Self‑hosting/data ownership: Strong. Open core; self‑hosting allowed on all tiers; Directus Cloud is optional【turn2search2】.
- Security/governance: Medium. RBAC and fine‑grained permissions exist; enterprise adds SSO, but audit/compliance artifacts depend on your infra.
- Integration flexibility: Strong. API‑first with webhooks and marketplace extensions; can wrap existing DBs instantly【turn2search1】.
- Implementation cost: Medium. No license fee (self‑host); cost is dev time to build frontend/SEO and integrations.
- Maintenance cost: Medium. Self‑hosted needs infra/DB maintenance; Directus Cloud reduces ops burden.
- Migration complexity: Medium. Data portability is good; complexity is in rebuilding the Directus configuration and frontend.
- Long‑term flexibility: Strong. Works well as a headless/API layer over existing DBs; good for product‑like B2B offerings.
- Best‑fit company type: B2B with existing databases needing an instant admin/API layer; dev‑centric.
- Where it becomes limiting: Limited marketing UI; SEO/page composition must be custom; multi‑brand needs careful design.

Payload CMS
- Marketing autonomy: Weak. No GUI schema builder; all changes require code deployment, which limits non‑technical admins【turn2search7】.
- Developer control: Strong. Code‑first, TypeScript config, many field types, and self‑hosting offer high control【turn2search7】【turn2search8】.
- Multi‑brand: Strong. Native multi‑tenancy plugin supports many tenants from one codebase, adapting the admin panel per tenant【turn2search6】【turn2search5】.
- Multi‑locale: Strong. Native localization (field‑level) with no hard limit on locales; API handles locale routing and fallbacks【turn7search10】【turn7search13】.
- SEO control: Medium. SEO fields are modelable; slugs, redirects, and rendering are typically implemented in the Next.js/app layer.
- Self‑hosting/data ownership: Strong. MIT license, free to self‑host anywhere Node runs【turn2search8】.
- Security/governance: Medium. Access control and API‑level security exist; you must supply audit logs/compliance on top.
- Integration flexibility: Strong. REST/GraphQL/Local API and Next.js integration make connecting external services straightforward.
- Implementation cost: Medium. No license fee; cost is dev time to build admin, preview, SEO, and multi‑tenant infrastructure.
- Maintenance cost: Medium. Self‑hosted stack requires dev care; no vendor‑provided hosting/SLA.
- Migration complexity: Medium. Data schemas and relationships must be reimplemented; Payload’s code‑first nature makes tooling less turnkey.
- Long‑term flexibility: Strong. Strong fit for composable, multi‑tenant product platforms; code‑first scales with team.
- Best‑fit company type: Dev‑heavy B2B building multi‑tenant platforms or product‑like sites with strong i18n.
- Where it becomes limiting: No visual page editing out of the box; marketing depends on dev for any structural change; smaller teams will feel maintenance load.

3) Important caveats
====================

- Ratings are qualitative and relative to mid‑market B2B in 2026, not absolute scores. “Medium” doesn’t mean “bad” and “Strong” doesn’t mean “perfect.”
- Security/governance ratings reflect typical enterprise expectations (SSO/SAML, RBAC, audit, compliance). For regulated verticals, always validate with your security team and current certifications (e.g., SOC 2/ISO 27001). For example, Webflow, Contentful, and others publish security/compliance positions, but scope and regional requirements matter【turn3search14】【turn10search0】【turn6search9】.
- Implementation and maintenance cost are highly context‑dependent: agency rates, in‑house capacity, hosting choices, and whether you use a SaaS or self‑host change TCO dramatically【turn4search5】【turn1search16】.
- Migration complexity is directional. Tools exist (export/import, APIs, CLI), but real cost depends on content volume, custom logic, and front‑end coupling.
- Multi‑brand support varies in form: WordPress/Drupal multisite share code but have different governance trade‑offs than AEM MSM or Payload’s multi‑tenant plugin【turn5search0】【turn9search0】【turn8search1】【turn2search6】.
- “Best‑fit company type” and “limiting” are generalized profiles. They’re a starting point, not a verdict. Always test with a small pilot aligned with your workflows.

4) Recommendations by company scenario
======================================

- Marketing‑led B2B, few brands, tight dev capacity
  - Primary pick: WordPress (self‑hosted or managed) if you want SEO breadth and low software cost, or Webflow if you prioritize clean performance, managed hosting, and faster launches with minimal dev【turn0search8】【turn3search5】.
  - Caution: Ensure governance and security practices are in place (plugin curation, updates, SSO, WAF) for WordPress【turn5search11】【turn5search14】.

- Multi‑brand B2B with many regional sites (e.g., divisions, portfolios)
  - Consider: AEM if you have Adobe ecosystem investment and can justify cost; Drupal if you have dev talent and need open‑source multisite with strong i18n and governance【turn0search12】【turn8search3】.
  - Headless alternatives: Contentful or Payload (multi‑tenant) if you’re comfortable building front‑ends and want API‑first composability【turn4search0】【turn2search6】.
  - Caution: AEM’s cost and migration overhead; Drupal’s authoring UX and talent pool.

- Dev‑centric B2B building product‑like experiences or platforms (multi‑tenant)
  - Strong fits: Payload CMS (native multi‑tenancy) and Directus (instant admin over existing DBs)【turn2search6】【turn2search1】.
  - Also good: Strapi or Sanity if you prefer different developer ergonomics or ecosystems.
  - Caution: Accept that marketing autonomy will be low; invest in preview and workflow tooling.

- Composable/multi‑channel B2B (web + apps + AI workflows)
  - Strong fits: Contentful, Sanity, Storyblok, Strapi, Directus, Payload—all are headless/API‑first【turn1search4】【turn1search8】【turn1search10】【turn7search0】【turn2search1】【turn2search8】.
  - If you want some marketer‑friendly editing: Storyblok or Contentful.
  - If you need maximum developer flexibility: Sanity or Payload.

- Highly regulated B2B requiring on‑prem or strict data residency
  - Primary fits: WordPress, Drupal, Strapi, Directus, Payload (all self‑hostable)【turn5search19】【turn0search10】【turn7search0】【turn2search2】【turn2search8】.
  - AEM 6.5 on‑prem is possible but being phased toward cloud; assess support timelines【turn4search14】【turn8search15】.
  - Caution: SaaS options (Webflow, Contentful, Sanity, Storyblok) may not meet on‑prem/residency constraints despite good security postures.

- Cost‑conscious mid‑market B2B wanting to keep TCO down
  - Best leverage: WordPress (self‑hosted with a solid host) or Strapi/Directus/Payload (self‑hosted, no license fee)【turn5search19】【turn7search0】【turn2search2】【turn2search8】.
  - Maintenance overhead is the key variable; budget for dev hours to patch, secure, and upgrade.
  - If you want managed infra with predictable spend: Webflow or Storyblok can be cost‑effective at moderate scale but watch per‑seat/space/asset caps【turn3search6】【turn4search11】.

- Multi‑locale B2B with strong SEO requirements
  - Safe bets: Drupal (core multilingual + SEO modules) and WordPress (with WPML + Rank Math/Yoast)【turn2search15】【turn2search17】【turn2search10】【turn2search13】.
  - Headless with strong i18n: Contentful, Storyblok, Sanity, Payload all support multi‑locale; SEO control depends on your front‑end implementation【turn1search3】【turn4search10】【turn6search0】【turn7search10】.
  - Caution: In headless setups, you must build slugs, redirects, hreflang, and sitemaps yourself; plan for that in implementation cost.