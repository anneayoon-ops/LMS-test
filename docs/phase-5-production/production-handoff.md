# Task 8: LEM / AEM Production Handoff

**Output files:**

```
handoff/lms-ads-ecosystem-handoff-notes.md
designs/lms-ads-ecosystem-hifi.fig  ← updated with annotation layer
```

---

## Step 1: Annotate All Figma Designs for Production

- [ ] Add a dedicated **"Annotations"** layer to the hi-fi Figma file

Every design element that requires an authoring or configuration decision in AEM must have an annotation.

**Annotation coverage by element type:**

| Element | What to annotate |
|---------|-----------------|
| Breadcrumb | AEM component name; how the path is configured; link destination for each node |
| Inline links | Exact destination URL; link text as authored; whether it opens same tab or new tab |
| Related content cards | Card 1: destination URL + title + description; Card 2: destination URL + title + description |
| Specs table | AEM component name, or: "New component required — see Component Proposals page" |
| Any new component | "New component: [name] — see Component Proposals page in Figma for full spec" |
| Responsive behavior | Notes on how the element behaves at 375px mobile breakpoint |

---

## Step 2: Write Handoff Notes Doc

- [ ] Write `handoff/lms-ads-ecosystem-handoff-notes.md`

Use this structure:

```markdown
# LMS Ads Ecosystem — Production Handoff Notes

## Summary of Changes per Page

### Page 1: [Ad Type] Product Page
- [What changed vs. current production]

### Page 2: [Ad Type] Tips & Best Practices
- [What changed]

### Page 3: [Ad Type] Specs
- [What changed]

---

## New Components Required

- Ecosystem Card: [description + link to Component Proposals page in Figma]
- Specs Table (if needed): [description + link to Component Proposals page]

---

## Breadcrumb Configuration

| Page | Breadcrumb trail | AEM config notes |
|------|-----------------|-----------------|
| Product page | Advertise > Ads > [Ad Type] | |
| Tips page | Advertise > Ads > [Ad Type] > Tips & Best Practices | |
| Specs page | Advertise > Ads > [Ad Type] > Specs | |

---

## Related Content Card Configuration

| Source page | Card 1 URL + copy | Card 2 URL + copy |
|------------|------------------|------------------|
| Product page | | |
| Tips page | | |
| Specs page | | |

---

## Inline Link Authoring Instructions

[Copy the placement rules from Task 5 Step 3 here verbatim]

---

## Open Items

[Log any unresolved AEM questions here]

---

## QA Checklist

- [ ] Breadcrumbs display correctly on all 3 pages
- [ ] Breadcrumb nodes link to correct destinations
- [ ] Related content cards show correct sibling pages per page type
- [ ] Inline links in body copy point to correct destinations
- [ ] All 3 pages tested on mobile (375px) — breadcrumbs truncate correctly
- [ ] Localization strings loaded and no text overflow on DE/NL (longest languages)
```

---

## Step 3: Production Kickoff Meeting

- [ ] Schedule and run a kickoff with the LEM production team

**Agenda:**

1. Screen share: walk through annotated Figma designs page by page
2. Review handoff notes doc
3. Review new component requests — confirm engineering estimate timeline for each
4. Work through red stickies from AEM constraints (captured in Task 2 FigJam)
5. Confirm production team has everything needed to begin build

Log any outstanding questions in the handoff doc under **"Open Items."**
