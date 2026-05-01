# Task 6: Hi-Fi Designs — 3 In-Scope Pages

**Output file:** `designs/lms-ads-ecosystem-hifi.fig`

!!! note "Design system"
    All designs use the **Our Community Design System**:
    [Figma link](https://www.figma.com/design/Ndoy2mlC4QdGMqjTs5yGfD/Our-Community-Design-System_Web-UX?node-id=0-1)

    Enable the library in Figma: **Assets panel → Team Libraries → Our Community Design System.**
    Custom components may be proposed where the system doesn't cover a need.

---

## Step 1: Set Up Figma Hi-Fi File

- [ ] Create the Figma file structure

| Page name | Contents |
|-----------|---------|
| Page 1 — [Ad Type] Product | Desktop + mobile hi-fi frames |
| Page 2 — [Ad Type] Tips | Desktop + mobile hi-fi frames |
| Page 3 — [Ad Type] Specs | Desktop + mobile hi-fi frames |
| Component Proposals | Custom components not covered by the system |

- Import the existing LMS site shell (header, footer, global nav) from an existing LMS Figma file — **do not recreate from scratch.**

---

## Step 2: Product Page (Desktop 1440px + Mobile 375px)

- [ ] Apply Community Design System tokens throughout

**Token map:**

| Element | Token / Component |
|---------|------------------|
| Page background | `color/surface/default` |
| Page title (H1) | `text/heading-xl` |
| Subtitle | `text/body-lg` |
| Primary CTA | `component/button/primary` |
| Breadcrumb — linked nodes | `color/text/link` + `text/body-sm` |
| Breadcrumb — current page | `color/text/secondary` + `text/body-sm` |
| Body copy | `text/body-md` |
| Inline links | `color/text/link` (underlined on hover) |
| Section dividers | `color/border/subtle` |
| Related content card | Ecosystem Card (see Component Proposals page) |
| Card hover shadow | `shadow/md` |

**Frame specs:**

- Desktop: 1440px wide, 12-column grid, 120px margins
- Mobile: 375px wide, 4-column grid, 16px margins

Apply **real content** from the in-scope ad type's Product page (selected in Task 2). Place inline links per placement rules from [Task 5, Step 3](breadcrumbs-spec.md#step-3-inline-link-placement-rules).

---

## Step 3: Tips & Best Practices Page (Desktop + Mobile)

- [ ] Apply same system tokens

**Additional design decisions for this page:**

| Condition | Decision |
|-----------|---------|
| 5 or fewer tips | Use numbered list (`text/heading-sm` for title, `text/body-md` for body) |
| 6 or more tips | Use system accordion component to reduce scroll length |
| Inline link to Specs | Style as `color/text/link` inline within body copy — **not** a standalone CTA button |
| Related cards | "Product overview" + "Specs" (per Task 5 card spec) |

---

## Step 4: Specs Page (Desktop + Mobile)

- [ ] Design the specs table

The Specs page requires the most design attention due to the table structure.

**Specs table design:**

=== "If system table component exists"

    Use it. Adapt to the 3-column structure (Spec | Requirement | Notes).

=== "If no system table component"

    Propose a **Specs Table** component on the Component Proposals page (see Step 5).

**Table visual spec:**

```
┌──────────────────┬─────────────────┬──────────────────┐
│ Spec             │ Requirement     │ Notes            │
├──────────────────┼─────────────────┼──────────────────┤
│ File type        │ MP4, MOV        │ H.264 encoding   │
│ Max file size    │ 200 MB          │                  │
│ Aspect ratio     │ 16:9, 1:1, 9:16 │ Varies by format │
└──────────────────┴─────────────────┴──────────────────┘
```

**Layout rules:**

- Each row = one discrete, complete spec (name + full value + notes in same row — no sub-rows)
- Section grouping: "Image Specs," "Copy Specs," "Technical Specs" as `text/heading-sm` headers
- **Desktop:** in-page jump nav above the table (anchor links to each section header)
- **Mobile:** table horizontally scrollable; section headers collapse to accordion

!!! tip "LLM readability annotation"
    Add this annotation in Figma: *"Each row is designed as a self-contained unit — spec name + full value in one row — to maximize readability for both users scanning and LLM/AI systems parsing the page."*

---

## Step 5: Custom Component Proposals

- [ ] Document each custom component on the Component Proposals Figma page

### Ecosystem Card (Related Content Module)

| Property | Value |
|----------|-------|
| Description | 2-up card layout linking to sibling pages in the same ad-type family |
| Variants | 2-card layout / 3-card layout (for potential future hub page use) |
| Properties | `cardTitle` (string), `cardDescription` (string, 1 line max), `destinationURL` |
| Default state | Flat; border: `color/border/subtle` |
| Hover state | `shadow/md`; arrow icon translates 4px right |
| Active state | Shadow reduces to `shadow/sm` |

!!! warning "AEM assessment needed"
    Annotation: *"Can this be implemented by extending the existing card component with a 2-up layout, or does it require a new component? Engineering assessment required before committing to this approach."*

### Specs Table *(if not in system)*

| Property | Value |
|----------|-------|
| Description | 3-column table (Spec \| Requirement \| Notes) with named section headers |
| Properties | `sectionTitle` (string), `rows` (array of `spec`, `requirement`, `notes`) |

!!! warning "AEM assessment needed"
    Annotation: *"Required only if AEM does not have a suitable table component. Flag for engineering estimate."*

---

## Step 6: Hi-Fi Design Review

- [ ] Share Figma link (view-only) for **async review**
- [ ] Run a **synchronous design review session**

Collect feedback from:

| Reviewer | Focus area |
|----------|-----------|
| Stakeholders | Visual design alignment |
| AEM/LEM Engineering | Custom component feasibility |
| SEO team | H1s, section headings, and CTAs keyword-aligned |

**Resolving feedback:**

- Every Figma comment must be resolved with either a design change or a written rationale for keeping the current design
- Log changes in Figma version history with a descriptive name: `v2 — post-design-review [date]`
