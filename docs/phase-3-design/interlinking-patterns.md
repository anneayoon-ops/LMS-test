# Task 3: Interlinking Pattern Exploration

**Output file:** `wireframes/interlinking-pattern-explorations.fig`  
4 annotated concept frames — one per pattern. Low-fidelity (grayscale, no real content).

!!! note "Why 4 concepts?"
    The team needs to evaluate all 4 interlinking patterns before committing to a direction. Each concept has different engineering implications in AEM and different discoverability trade-offs. See the [Decision Comparison](#step-5-pattern-decision) at the bottom of this page.

---

## Concept A — Persistent In-Page Tab Nav

- [ ] Design a tab navigation bar below the site header

```
┌──────────────────────────────────────────────────────────────┐
│  [ Overview ]  [ Tips & Best Practices ]  [ Specs ]          │
│  ─────────────                                               │
└──────────────────────────────────────────────────────────────┘
```

Show on all 3 sibling pages (3 separate frames). On each frame, the **active tab is underlined/highlighted**; inactive tabs are linked.

**Annotations to add in Figma:**

- "Tabs appear below the global site nav, above page hero"
- "Active tab = current page; inactive tabs = links to sibling pages for same ad type"
- "Tab labels are fixed: Overview | Tips & Best Practices | Specs"
- "AEM: Requires new tab nav component — must get engineering estimate before committing"

**Pros / Cons:**

| | |
|---|---|
| ✅ Pro | Users immediately understand they're in a 3-page ecosystem on arrival |
| ❌ Con | New AEM component required; URL changes on tab click may confuse users who bookmarked or shared a URL |

---

## Concept B — Related Content Cards at Page Bottom

- [ ] Design a "You might also need" module at the bottom of each page

```
┌──────────────────────────────────────────────────────────────┐
│  You might also need                                         │
│                                                              │
│  ┌──────────────────────┐   ┌──────────────────────┐        │
│  │  Tips & Best         │   │  [Ad Type] Specs      │        │
│  │  Practices           │   │                       │        │
│  │  [description text]  │   │  [description text]   │        │
│  │              →       │   │              →        │        │
│  └──────────────────────┘   └──────────────────────┘        │
└──────────────────────────────────────────────────────────────┘
```

Cards vary per source page — each page shows its 2 sibling pages.

**Annotations:**

- "Module title: 'You might also need'"
- "Each card: sibling page title, 1-line description, directional arrow"
- "AEM: Likely buildable with existing card component + manual URL configuration per page"
- "Cards appear above page footer, below body content"

**Pros / Cons:**

| | |
|---|---|
| ✅ Pro | Low engineering lift; compatible with existing AEM card components |
| ❌ Con | Below the fold — users who don't scroll will miss it |

---

## Concept C — Sticky Sidebar with Page Family Links

- [ ] Design a left sidebar showing the page family structure

```
┌─────────────────┐
│ Video Ads       │
│                 │
│ ├── Overview    │
│ ├── Tips & Best │  ← [active, highlighted]
│ │   Practices   │
│ └── Specs       │
│                 │
│ ─────────────── │
│ [Back to Ad     │
│  Specs Guide]   │
└─────────────────┘
```

Show sidebar as **sticky on desktop** (stays visible while scrolling). Show a **collapsed accordion** state on mobile.

**Annotations:**

- "Sidebar always visible as user scrolls — active page is highlighted"
- "Sidebar also includes link back to parent hub page"
- "Mobile: sidebar collapses into a disclosure accordion above page hero"
- "AEM: New sidebar component required — highest engineering complexity of the 4 options"

**Pros / Cons:**

| | |
|---|---|
| ✅ Pro | Always visible regardless of scroll position; best for users who scan and want to jump |
| ❌ Con | Highest engineering cost; may conflict with existing LMS page layout templates |

---

## Concept D — Breadcrumbs + Inline Contextual Links

- [ ] Design breadcrumb trail + annotated inline links in body copy

**Breadcrumb:**

```
Advertise  >  Ads  >  Video Ads  >  Specs
```

**Inline link example** (highlight in blue on the product page frame):

```
Video Ads allow you to tell your brand story in motion.
Before uploading your creative, review the [Ad Specs →]
to ensure your file meets technical requirements. For
campaign performance guidance, see [Tips & Best Practices →].
```

**Annotations:**

- "Breadcrumb: each node is clickable; current page (rightmost) is non-linked plain text"
- "Inline links appear at the point of relevance in body copy — not in a separate nav element"
- "AEM: Breadcrumbs may exist as a component already; inline links are author-managed in CMS"
- "This pattern requires no new components if breadcrumb component already exists"

**Pros / Cons:**

| | |
|---|---|
| ✅ Pro | Lowest engineering lift; works within existing AEM templates; breadcrumbs also provide an SEO signal |
| ❌ Con | Depends on content authors correctly placing and maintaining inline links; no persistent nav element |

---

## Step 5: Pattern Decision

- [ ] Add a Decision frame to the Figma file comparing all 4 patterns

| Pattern | Engineering lift | User discoverability | SEO impact | Mobile |
|---------|-----------------|---------------------|------------|--------|
| A — Tab nav | High (new component) | High (above fold) | Neutral | Needs careful mobile design |
| B — Cards at bottom | Low (existing component) | Medium (below fold) | Neutral | Works well |
| C — Sticky sidebar | Highest (new component) | Highest (always visible) | Neutral | Complex (accordion) |
| D — Breadcrumbs + inline links | Lowest (may reuse existing) | Lower (inline only) | High (SEO signal) | Works well |

!!! success "Recommended direction"
    **Adopt Concept D (breadcrumbs + inline links) as baseline + Concept B (related content cards) as enhancement.**

    Together they cover:

    - **Above-content:** breadcrumbs show hierarchy on every page
    - **Below-content:** related cards provide discovery after reading

    Combined engineering lift is low — both patterns are compatible with existing AEM components.

    Flag Concepts A and C for future consideration pending AEM component roadmap.

- [ ] Present to stakeholders
- [ ] Capture decision and rationale in FigJam (link back to IA map from Task 2)
