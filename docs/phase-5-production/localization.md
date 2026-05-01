# Task 9: Localization Handoff

**Output files:**

```
handoff/localization-brief.md
handoff/localization-strings.csv
```

**Languages:** ES-ES · PT-BR · DE-DE · FR-FR · EN-IN · NL-NL

!!! note "Scope"
    UX delivers English designs and strings. The localization team handles all language adaptation. No RTL languages are in scope — layout adaptation is not required.

---

## Step 1: Write the Localization Brief

- [ ] Write `handoff/localization-brief.md`

```markdown
# LMS Ads Ecosystem — Localization Brief

## Scope
3 pages: [Ad Type] Product, Tips & Best Practices, Specs
Languages: ES-ES, PT-BR, DE-DE, FR-FR, EN-IN, NL-NL

## What's Being Localized
- All new/updated body copy on the 3 pages
- Related content card titles and descriptions (new)
- Breadcrumb node labels (if not already localized)
- Any updated H1s or section headings per content optimization brief

## Character Length Guidelines
- DE-DE and NL-NL copy can expand 30%+ vs. English
- Max character counts per string are specified in the strings spreadsheet
- Do not shorten meaning to fit — flag any strings that exceed max chars
- No RTL languages in scope; no layout adaptation required

## Reference Files
- Final English Figma designs: [link to designs/lms-ads-ecosystem-hifi.fig]
- Content optimization brief: [link to content/content-optimization-brief.md]
- Strings spreadsheet: [link to handoff/localization-strings.csv]
```

---

## Step 2: Extract and Format Localizable Strings

- [ ] Create `handoff/localization-strings.csv`

Working with the LEM production team, identify all new and updated strings. Use this format:

```csv
String ID,Page,Element,English text,Context / instructions,Max chars
breadcrumb_ad_type_name,[Ad Type] Product,Breadcrumb node,[Ad Type Name],Breadcrumb node linking to product overview page. Clickable link.,30
breadcrumb_tips,[Ad Type] Tips,Breadcrumb node,Tips & Best Practices,Breadcrumb — current page (non-linked plain text),30
breadcrumb_specs,[Ad Type] Specs,Breadcrumb node,Specs,Breadcrumb — current page (non-linked plain text),15
card_tips_title,[Ad Type] Product,Related content card 1 title,Tips & Best Practices,Card linking to tips sibling page,30
card_tips_desc,[Ad Type] Product,Related content card 1 description,[Ad Type]-specific tips and best practices for campaign performance,Card subtitle — 1 line max. Appears below card title.,80
card_specs_title,[Ad Type] Product,Related content card 2 title,[Ad Type] Specs,Card linking to specs sibling page,30
card_specs_desc,[Ad Type] Product,Related content card 2 description,Technical requirements for [Ad Type] creative assets,Card subtitle — 1 line max.,80
```

Continue extracting strings for all new/updated elements across all 3 pages.

---

## Step 3: Send Localization Handoff

- [ ] Send the following to the localization team:

| Item | File |
|------|------|
| Localization brief | `handoff/localization-brief.md` |
| Strings spreadsheet | `handoff/localization-strings.csv` |
| Figma designs (view-only) | `designs/lms-ads-ecosystem-hifi.fig` |

**Confirm with the loc team:**

- [ ] Turnaround timeline — aligned with production build schedule
- [ ] Process for flagging strings that exceed max character counts
- [ ] Whether any of the 6 languages have existing translations for unchanged strings (to avoid redundant retranslation)
