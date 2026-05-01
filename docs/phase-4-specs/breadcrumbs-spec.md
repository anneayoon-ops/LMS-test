# Task 5: Breadcrumbs + Interlinking Annotated Spec

**Output file:** `specs/breadcrumbs-interlinking-spec.fig` (Figma annotated spec doc)

This task produces the definitive specification for all breadcrumb hierarchy, card interlinking rules, and inline link placement. It becomes the source of truth for content authors, AEM engineers, and the localization team.

---

## Step 1: Breadcrumb Hierarchy — All Page Types

- [ ] Create a spec table in Figma

| Page Type | Breadcrumb Trail | Behavior Notes |
|-----------|-----------------|----------------|
| Ads main | *(none — top-level page)* | No breadcrumb needed |
| Hub — Ads Guide | `Advertise > Ads > Ad Specs Guide` | |
| Hub — OBA | `Advertise > Ads > Objective-Based Advertising` | |
| Hub — Best Practices | `Advertise > Ads > Best Practices` | |
| [Ad Type] Product page | `Advertise > Ads > [Ad Type Name]` | Rightmost node is non-linked (current page) |
| [Ad Type] Tips page | `Advertise > Ads > [Ad Type Name] > Tips & Best Practices` | [Ad Type Name] links to product page |
| [Ad Type] Specs page | `Advertise > Ads > [Ad Type Name] > Specs` | [Ad Type Name] links to product page |

**Annotation to include in spec:**

- "Each breadcrumb node is a text link **except** the rightmost (current page), which is plain text"
- "'Advertise' → `business.linkedin.com/advertise`"
- "'Ads' → `business.linkedin.com/advertise/ads`"
- "[Ad Type Name] on Tips/Specs pages → links to the Product page for that ad type"

!!! warning "AEM validation required"
    Add a red callout annotation: *"AEM: Confirm whether a breadcrumb component exists in the current LEM component library. If it does, confirm it supports dynamic path injection. If not, flag as a new component requirement for engineering estimate."*

---

## Step 2: Card Interlinking Rules

- [ ] Create the card interlinking spec table

| Source Page | Card 1 Destination | Card 1 Title | Card 2 Destination | Card 2 Title |
|------------|-------------------|-------------|-------------------|-------------|
| [Ad Type] Product page | [Ad Type] Tips page | "Tips & Best Practices" | [Ad Type] Specs page | "[Ad Type] Specs" |
| [Ad Type] Tips page | [Ad Type] Product page | "[Ad Type] Overview" | [Ad Type] Specs page | "[Ad Type] Specs" |
| [Ad Type] Specs page | [Ad Type] Product page | "[Ad Type] Overview" | [Ad Type] Tips page | "Tips & Best Practices" |

**Card component spec:**

```
┌──────────────────────────────────┐
│  [Card title]                    │
│  [One-line description of what   │
│   user will find on this page]   │
│                              →   │
└──────────────────────────────────┘

States:
- Default:        flat; border-color: border/subtle
- Hover:          elevated (shadow/md); arrow translates 4px right
- Active/pressed: shadow reduces to shadow/sm
```

---

## Step 3: Inline Link Placement Rules

- [ ] Create placement guidelines for content authors

These rules must also appear in the content guidelines handed off in Task 7.

=== "Product Pages"

    | Placement | Link text | Destination |
    |-----------|-----------|-------------|
    | End of "technical requirements" or "creative specs" section | "[Ad Type] Specs" | Specs page |
    | End of "best practices" teaser or "tips" mention | "Tips & Best Practices for [Ad Type]" | Tips page |

=== "Tips Pages"

    | Placement | Link text | Destination |
    |-----------|-----------|-------------|
    | Any mention of character limits, file sizes, or technical constraints | "see [Ad Type] Specs" | Specs page |
    | End-of-page CTA section | "Learn more about [Ad Type]" | Product page |

=== "Specs Pages"

    | Placement | Link text | Destination |
    |-----------|-----------|-------------|
    | Intro paragraph (first sentence) | "[Ad Type] overview" | Product page |
    | After the specs table(s) | "Tips & Best Practices for [Ad Type]" | Tips page |

!!! note "Authoring note"
    Inline links are authored directly in CMS body copy. Include these rules verbatim in the content guidelines doc (Task 7, Step 2).

---

## Step 4: Breadcrumb Component Design Spec

- [ ] Annotate the breadcrumb component in Figma with full measurements

```
Typography:    body-sm  (Community Design System text style)
Linked nodes:  color/text/link
Current page:  color/text/secondary  (non-linked)
Separator ">": color/text/tertiary
Spacing:       8px between nodes
Container:     No background, no border; flush below global nav
```

**Mobile behavior:**

```
4+ node breadcrumb → truncate to: [First node] > ... > [n-1 node] > [Current page]
Example: "Advertise > ... > Video Ads > Specs"
Ellipsis "..." = tappable; expands to show full trail on tap
```
