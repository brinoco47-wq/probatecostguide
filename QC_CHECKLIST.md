# Probate Site — 10/10 QC Checklist
**Standing order (Dom 2026-10-16):** "website bilkul 10/10 honi chahiye, koi ghalti ki gunjaish nahi hay."
Run this checklist before EVERY push. Any failure blocks the push.

## Automated checks (python, must all pass)
- [ ] Exactly one `<h1>` per page
- [ ] `<title>` ≤ 60 chars on every page
- [ ] Meta description present and ≤ 160 chars on every page (except 404)
- [ ] Canonical link present on every page (except 404)
- [ ] All JSON-LD blocks parse (Article + BreadcrumbList + FAQPage where applicable)
- [ ] Tag balance: div/section/article/main/header/footer/table/details open == close
- [ ] Every `#anchor` href has a matching `id` target on the page
- [ ] Internal link graph: 0 orphans (homepage excepted), 0 broken (excluding `./` `../` home-links)
- [ ] "not legal advice" disclaimer present on every content page
- [ ] sitemap.xml lists every indexable page, no extras
- [ ] OG tags on homepage + pillar pages

## Manual checks
- [ ] Read the full page text once for typos and grammar
- [ ] Every new section is listed in the page's TOC with a working anchor
- [ ] Every statistic has a source or is labeled as a typical range / planning figure
- [ ] Statute citations verified (e.g. Cal. Probate Code §10810 schedule math re-checked)
- [ ] No contact email published unless its MX is verified (rule: never publish an unverified inbox)
- [ ] "Figures checked {Month Year}" date is current on every edited page
- [ ] Footer disclaimer present: "Informational purposes only — not legal advice, not a law firm."

## Lessons baked in from the 2026-10-16 launch audit
- Contact page shipped with hello@probatecostguide.com before the domain/inbox existed → removed; never publish an email without MX verification.
- 6 title/meta length violations shipped in the first draft → lengths are now in the automated check.
- New sections added without TOC entries or anchor ids → TOC/anchor check is now automated.
- One edit deleted a `<div class="faq">` opening tag → tag-balance check is now automated.
