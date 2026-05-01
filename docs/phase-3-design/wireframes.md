# Task 4: Wireframes — 3 In-Scope Pages

**Output file:** `wireframes/lms-ads-ecosystem-wireframes.fig`  
3 pages × desktop (1440px) + mobile (375px) = **6 frames minimum.**  
Grayscale only. No real content — use placeholder text throughout.

---

## Step 1: Set Up Wireframe Template

- [ ] Build a reusable Figma wireframe template

The template must include:

| Zone | Content |
|------|---------|
| Site shell | LinkedIn Marketing Solutions global header, footer, primary nav (placeholder) |
| Breadcrumb row | `[Level 1] > [Level 2] > [Level 3]` — linked text nodes, grayscale |
| Page hero | H1 placeholder, subtitle placeholder, primary CTA button placeholder |
| Content body | Text block placeholders in 2/3-width column |
| Related module | "You might also need" — 2-card layout (Concept B from Task 3) |
| Mobile variant | Stack everything single-column; breadcrumb shows last 2 nodes only |

---

## Step 2: Wireframe — Product Page

- [ ] Apply template. Desktop (1440px) + Mobile (375px).

**Page structure:**

```
[Global header + nav]
──────────────────────────────────────────────────
Advertise > Ads > [Ad Type]                   ← breadcrumb
──────────────────────────────────────────────────
[Ad Type] — Page Hero
[Subtitle placeholder]
[Primary CTA: "Start advertising"]
──────────────────────────────────────────────────
What is [Ad Type]?     [Body copy block]
                       [Inline link placeholder → Tips page]
                       [Inline link placeholder → Specs page]
──────────────────────────────────────────────────
Why use [Ad Type]?     [Body copy block]
──────────────────────────────────────────────────
Example placements     [Image placeholder × 3]
──────────────────────────────────────────────────
You might also need
[Tips card]            [Specs card]
──────────────────────────────────────────────────
[Global footer]
```

**Annotation layer — annotate every navigation element:**

| Element | Annotation |
|---------|-----------|
| Breadcrumb | "'Advertise' → /advertise; 'Ads' → /advertise/ads; '[Ad Type]' = current page (no link)" |
| Inline link 1 | "Appears at end of creative requirements section → links to [Ad Type] Specs page" |
| Inline link 2 | "Appears after product description → links to Tips & Best Practices page" |
| Related cards | "Always show the other 2 pages in the same ad-type family; never repeat current page" |

---

## Step 3: Wireframe — Tips & Best Practices Page

- [ ] Apply template. Desktop + Mobile.

**Differences from Product page:**

Breadcrumb: `Advertise > Ads > [Ad Type] > Tips & Best Practices`

**Page structure:**

```
[Tips intro: one paragraph explaining what these tips cover]
──────────────────────────────────────────────────
Tip 1: [Title]         [Body copy block]
                       [Inline link → Specs: "see Ad Specs for character limits"]
──────────────────────────────────────────────────
Tip 2: [Title]         [Body copy block]
──────────────────────────────────────────────────
Tip N: [Title]         [Body copy block]
──────────────────────────────────────────────────
You might also need
[Product overview card]  [Specs card]
──────────────────────────────────────────────────
```

**Annotations:**

| Element | Annotation |
|---------|-----------|
| Breadcrumb | "'[Ad Type]' node links to product page — how users navigate back to product overview" |
| Inline link in Tip 1 | "Links to Specs page at the moment a technical constraint is mentioned — contextual linking pattern" |
| Related cards | "Product overview + Specs — never repeat the current page" |

---

## Step 4: Wireframe — Specs Page

- [ ] Apply template. Desktop + Mobile.

Breadcrumb: `Advertise > Ads > [Ad Type] > Specs`

**Page structure:**

```
[Intro: 1–2 sentences + inline link to product overview]
──────────────────────────────────────────────────
Image Specs            [Specs table placeholder]
  Spec name | Value | Notes
──────────────────────────────────────────────────
Copy Specs             [Specs table placeholder]
  Spec name | Value | Notes
──────────────────────────────────────────────────
Technical Specs        [Specs table placeholder]
  Spec name | Value | Notes
──────────────────────────────────────────────────
You might also need
[Product overview card]  [Tips card]
──────────────────────────────────────────────────
```

**Annotations:**

| Element | Annotation |
|---------|-----------|
| Intro inline link | "Links to [Ad Type] product overview page — context for users who landed directly on Specs from search" |
| Specs table | "Each row is self-contained (spec name + value + notes) — modular structure for LLM/AI readability" |
| Section headers | "Anchor links on desktop allow deep-linking and jump navigation to Image/Copy/Technical sections" |
| Mobile tables | "Tables scroll horizontally on mobile; section headers collapse to accordion" |

!!! tip "LLM readability"
    The specs table layout — one complete spec per row — is intentional. It ensures each row is a parseable, standalone unit for both human scanners and AI systems retrieving page content. Do not use multi-row grouped specs or sub-headers that break the row integrity.

---

## Step 5: Wireframe Review + AEM Validation

- [ ] Share Figma wireframe link for async review
- [ ] Present in a live session

**Attendees:**

| Group | Names | Purpose |
|-------|-------|---------|
| Stakeholders | Mariam, Jane, Nora, Walter, Heidi, Cody | UX direction alignment |
| AEM/LEM Engineering | TBD | Component feasibility review |

**Document all AEM constraints as red annotation notes in Figma.**

These constraints determine which custom components need to be proposed in the hi-fi phase (Task 6).
