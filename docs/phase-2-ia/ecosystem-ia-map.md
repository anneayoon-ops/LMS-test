# Task 2: Ecosystem IA Map

**Output file:** `ia/lms-ads-ecosystem-ia-map.fig` (FigJam)

---

## Step 1: Set Up FigJam Workspace

- [ ] Create a new FigJam file with three labeled sections

| Section | Purpose |
|---------|---------|
| **Current State** | Existing page structure, as-is |
| **Proposed State** | Redesigned ecosystem architecture |
| **Delta / Changes** | What's new, what changes, what stays |

---

## Step 2: Map the Current State

- [ ] Map every page in the ecosystem as a node

Connect nodes with **directional arrows** showing existing links.

**Color coding:**

| Color | Page type |
|-------|-----------|
| 🔵 Blue | Hub pages (ads-guide, OBA, best-practices, ads main) |
| 🟢 Green | Product pages (e.g. sponsored-content/video-ads) |
| 🟠 Orange | Tips pages |
| 🟣 Purple | Specs pages |
| 🔴 Red | Dead-end pages (no outbound link to a sibling) |

**Label each node with:**

- Page name
- Abbreviated URL
- Breadcrumbs present (Y/N)
- Primary CTA

!!! warning "Flag dead ends"
    For every red node, add a sticky note: **"Pain point: [describe what a search-entry user cannot find from here]."**

---

## Step 3: Design the Proposed Architecture

- [ ] Redesign the node map in the Proposed State section

Apply all 6 interlinking patterns to the proposed architecture:

| # | Pattern | How to show in FigJam |
|---|---------|----------------------|
| 1 | **Triad linking (must-have)** — every product, tips, and specs page for the same ad type links to its two siblings | Thick bidirectional arrows |
| 2 | **Hub links** — every leaf page links back to its relevant hub | Thin arrows to hub nodes |
| 3 | **Persistent nav module** — shared component on all 3 sibling pages | Box labeled "Ad Type Nav Module" on each node |
| 4 | **Breadcrumbs** — full hierarchy path on each page | Annotate each node: e.g. `Advertise > Ads > Video Ads > Specs` |
| 5 | **Related content cards** — module at bottom of each page pointing to siblings | "Related" module box on each node |
| 6 | **Inline contextual links** — links within body copy at point of relevance | Sticky note on product pages: "Body copy links to Specs and Tips pages inline" |

---

## Step 4: Select the 3 In-Scope Pages

- [ ] Identify the 3 pages that will serve as the design case study

The 3 pages should form **one complete ad-type triad:** Product + Tips + Specs for a single ad format.

**Decision criteria:**

1. Select the ad type with the **highest organic search traffic** (coordinate with SEO team for data)
2. Prefer an ad type where all 3 pages currently exist and have substantial content
3. Document the rationale on the selected FigJam nodes: *"In scope because: [reason]"*

!!! note "Page selection is deferred"
    The specific 3 pages are intentionally not locked in during the brief phase. The IA mapping work (Steps 2–3) will surface which ad-type triad has the most fragmented ecosystem and the highest SEO opportunity — that becomes the design target.

---

## Step 5: IA Review Checkpoint

- [ ] Present the FigJam map to the **full stakeholder group**

Collect alignment on:

- [ ] Proposed IA is approved
- [ ] 3 in-scope pages are confirmed
- [ ] AEM/LEM engineering team has reviewed which proposed components are buildable vs. require new development

!!! warning "Capture AEM constraints"
    Document every AEM component limitation as a **red sticky note** in FigJam.
    These red stickies become the design constraints that inform wireframing in Task 4.
