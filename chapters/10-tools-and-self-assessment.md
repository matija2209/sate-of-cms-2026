# Tools and Self-Assessment

Reports inform; tools decide. The chapters so far have given you frameworks — maturity stages, migration risk profiles, category logic, TCO structure. This chapter is about turning them into numbers and shortlists for *your* company, using interactive self-assessment tools. Used well, they convert a vague "we should probably replatform" into a scoped decision with a budget, a risk register, and a defensible shortlist.

The reason to use tools rather than intuition is simple: they make assumptions explicit. A cost calculator forces you to state your page count, locale count, and integration list. A risk assessment forces you to name what you'd lose in a bad migration. Executives can argue with assumptions; they can't argue productively with vibes. B2B buying research consistently finds that decision-makers engage more deeply with interactive content than static documents — but the real value is internal: the outputs become the working documents your buying group aligns around.

## The five tool types and what each decides

### CMS picker (selection tool)

**What it helps decide:** which CMS categories and platforms belong on your shortlist.

A structured questionnaire — team composition, engineering capacity, locale and brand count, integration needs, hosting constraints, budget shape — that maps your answers to the category logic of Chapter 6 and the platform profiles of Chapter 7. A good picker returns a shortlist of two to four options with the reasoning visible, not a single "winner": if you can't see *why* it recommended something, don't trust the recommendation.

**Gather first:** honest engineering availability (hours per month, not aspiration), locale and brand counts for the next 18 months, your integration list, and any hard constraints (self-hosting, compliance).

### CMS migration risk assessment

**What it helps decide:** how risky your specific migration is, and where the risk concentrates.

This operationalizes Chapter 5: you identify your current platform, content volume, template count, locale count, and integration criticality; it returns a risk profile across the dimensions that matter — SEO/redirects, content export, content modeling, media, workflow, integrations — with mitigations per category. The output should look like a heat map, not a single score: "your SEO risk is high and your workflow risk is low" is actionable; "your migration risk is 62/100" is not.

**Gather first:** a URL inventory (or at least top-traffic pages from analytics), your plugin/integration list, locale count, and whether a redesign is bundled with the migration (it usually is, and it changes the risk profile).

### Website redesign cost calculator

**What it helps decide:** a realistic budget envelope for the rebuild, before vendor proposals anchor you.

A useful calculator returns a *range* (low/mid/high) with line items — design, content migration, integrations, localization, QA, and ongoing costs — mapped to the TCO stack from Chapter 8. Treat its output as a sense-check against proposals: if a quote is half the calculator's low end, something big is missing from the quote; if it's double the high end, ask exactly which of your inputs drives it.

**Gather first:** page and template counts, content volume, locale count, integration list, and whether SEO preservation is in scope (it must be — Chapter 5).

### Payload CMS cost estimator

**What it helps decide:** project scope and cost *if* Payload is already on your shortlist.

Platform-specific estimators are useful precisely because they price what generic calculators can't: the self-hosted trade. For Payload that means no license fees but real engineering line items — infrastructure setup, admin/editorial UX configuration, front-end build, multi-tenant architecture if you're multi-brand. Use it to compare Payload's cost *shape* (engineering-heavy, subscription-light) against SaaS alternatives on a three-year horizon, not just year one. The same logic applies to any platform-specific estimator: it's a scoping tool, not a commitment.

**Gather first:** your hosting posture (own infra vs. managed), engineering capacity for build and ongoing ownership, and the collection/content-type inventory from your content model work.

### Website growth opportunity review

**What it helps decide:** whether replatforming is even the right project — and what the website could return if it were fixed.

This is the widest-aperture tool: an assessment of your website's current performance (traffic, conversion, SEO health, publishing velocity) against its opportunity. Sometimes the honest output is "your CMS is fine; your content operation is the constraint" — which is a cheaper problem to solve. When it does point at the platform, it produces the business case: what growth is being left on the table by slow publishing, poor SEO infrastructure, or missing localization.

**Gather first:** analytics access, Search Console data, current publishing cadence, and your conversion baseline.

## How to interpret tool results

- **Ranges beat point estimates.** Any tool that returns a single precise number is projecting false confidence. Costs, timelines, and risk are distributions; plan against the range.
- **Check the assumptions before the answer.** Good tools show their inputs back to you and expose their logic. If a default doesn't match your reality (agency rates, locale count), fix it and re-run — bad defaults are the fastest way to a wrong conclusion.
- **Tools narrow; they don't decide.** A shortlist from a CMS picker is the *start* of evaluation — the proof-of-concept, reference calls, and governance-fit checks from earlier chapters still apply. No questionnaire knows your team's actual dynamics.
- **Discrepancies are information.** If the cost calculator and a vendor proposal disagree wildly, or the risk assessment contradicts your gut, the gap itself is the finding — investigate it before proceeding.
- **Re-run at decision gates.** Inputs change: a locale gets added, an integration gets cut. Tools are cheap to re-run; stale outputs quietly mislead.

## Sequencing: which tool, when

1. **Start with the growth opportunity review** — it establishes whether there is a business case and its size.
2. **Run the migration risk assessment** once a rebuild is plausible — its findings shape platform requirements (Chapter 5's principle: audit before selection).
3. **Use the CMS picker** with those requirements loaded — constraints first, then architecture, then experience, per Chapter 9's ordering.
4. **Run the cost calculator** against the shortlist to set the budget envelope before proposals arrive.
5. **Run platform-specific estimators** (such as the Payload estimator) only for shortlisted platforms, to compare cost shapes on a three-year horizon.

The outputs, assembled, are effectively an internal decision brief: opportunity size, risk register, requirements, shortlist, and budget. That is the document a buying group — marketing, engineering, finance — can actually align on, and it is far more useful than any vendor's RFP template.

One caution to close: no tool replaces the two irreplaceable steps from earlier chapters — the content and URL audit (Chapter 5) and the working proof of concept (Chapters 7–9). Tools tell you where to look and what to budget. The audit and the pilot tell you the truth.
