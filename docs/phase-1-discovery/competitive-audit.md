# Task 1: Discovery & Competitive Audit

**Output files:**

```
research/competitive-audit-lms-ads-ecosystem.md
research/current-state-audit.md
```

---

## Step 1: Audit the Current LinkedIn Ads Ecosystem

- [ ] Visit and document each page in the current ecosystem

For each page, capture: URL, page title, existing breadcrumbs (Y/N + what they show), which sibling pages it links to (if any), and the most likely exit path for a search-entry user.

**Pages to audit:**

```
Product page:       https://business.linkedin.com/advertise/ads/sponsored-content/video-ads
Tips page:          https://business.linkedin.com/advertise/ads/sponsored-content/video-ads/tips
Specs page:         https://business.linkedin.com/advertise/ads/sponsored-content/video-ads/specs
Ads Guide hub:      https://business.linkedin.com/advertise/ads/ads-guide
OBA hub:            https://business.linkedin.com/advertise/ads/objective-based-advertising
Best Practices hub: https://business.linkedin.com/advertise/ads/best-practices
Ads main:           https://business.linkedin.com/advertise/ads
```

**For each page, answer:**

- Does it have breadcrumbs? What hierarchy do they show?
- Does it link to its sibling pages (product ↔ tips ↔ specs)?
- Is there a visible link back to a hub page?
- What is the likely exit path for a user who landed from search?

!!! warning "Flag dead-end pages"
    A **dead-end page** = a page where a search-entry user has no visible path to a related page.
    These are the primary pain points this project solves. Mark each dead-end clearly in your audit table.

---

## Step 2: Competitive Audit — Facebook Ads Guide

- [ ] Visit and document the Facebook model

URL: `https://www.facebook.com/business/ads-guide/update`

Document:

- Left-sidebar nav structure: what hierarchy? How are ad types organized?
- How does it handle the product overview → specs → best practices relationship? (same page vs. linked pages)
- **Simulate search entry:** land directly on a deep sub-page — is the full sidebar nav still visible? Can you find the broader ecosystem?
- Note specifically what makes this model search-friendly (or not) — this is the preferred competitor reference

!!! tip "Why Facebook?"
    The Facebook Ads Guide model is the preferred reference pattern for this project. The audit should focus on whether the sidebar navigation survives a search-entry experience — i.e., whether a user landing deep from Google can still orient themselves using the left nav.

---

## Step 3: Competitive Audit — Amazon Ad Specs

- [ ] Visit and document the Amazon model

URL: `https://advertising.amazon.com/resources/ad-specs`

Document:

- How is specs content structured? (filterable table vs. individual per-ad-type pages)
- How does Amazon handle the product overview / best practices / specs distinction?
- What is the primary navigation pattern for cross-spec discovery?

---

## Step 4: Synthesize Findings

- [ ] Write `research/competitive-audit-lms-ads-ecosystem.md`

Use the following structure:

```markdown
# LMS Ads Ecosystem — Competitive Audit

## Current State: Dead-End Analysis

| Page | Has breadcrumbs? | Links to siblings? | Dead end? |
|------|-----------------|-------------------|-----------|
| Product page | | | |
| Tips page | | | |
| Specs page | | | |
| Ads Guide hub | | | |
| OBA hub | | | |
| Best Practices hub | | | |

## Competitor Analysis

### Facebook Ads Guide
- Navigation pattern:
- Search-entry experience:
- What LinkedIn should adopt:
- What to avoid:

### Amazon Ad Specs
- Navigation pattern:
- What LinkedIn should adopt:
- What to avoid:

## Recommendation
[1 paragraph: which pattern best fits LinkedIn's search-entry use case and why]

## Decisions Made
[Document stakeholder decisions from Step 5 here]
```

!!! note "Format tip"
    Write all findings as short bullets — this content feeds directly into FigJam sticky note annotations in Task 2.

---

## Step 5: Stakeholder Alignment Session

- [ ] Present findings to: **Mariam Jameel, Jane Suh, Nora Sanchez**

Collect alignment on:

- Which competitor pattern resonates with the team
- Any constraints not captured in the brief (brand, legal, AEM component availability)
- Confirm that 3 in-scope pages will be selected **after** the IA phase

Document all decisions in the audit doc under **"Decisions Made."**
