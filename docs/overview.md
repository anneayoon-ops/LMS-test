# Project Brief

## Project Overview

| Field | Detail |
|-------|--------|
| **Project name** | LMS Ads Ecosystem |
| **Requested by** | SEO team |
| **UX support type** | Information Architecture, Wireframes, Hi-Fi Design, Content |
| **Production** | LEM in AEM (Adobe Experience Manager) |

### Problem Statement

The SEO team would like UX support to outline the best option for a LinkedIn Ads ecosystem. Currently, specs, tips, and best practices are individual, siloed pages. Visitors can easily find these pages in search, but once they land, it's difficult to navigate between related experiences.

> **User pain point:** Users entering via search encounter isolated Ads pages with no clear pathways to related content, creating dead ends that disrupt their ability to complete tasks efficiently.

---

## Purpose

Create better connective tissue between individual LinkedIn Ads pages. The goal is to answer the question: **what is the best option here from a UX design POV?**

Visitors easily find specs and tips pages through search, but once they land, navigation between the product → tips → specs experience is broken.

---

## Target Audience

**Primary:** Digital marketers and advertisers who discover LinkedIn Ads content via organic search and need quick access to ad specs, best practices, and product information to plan and execute campaigns.

**Entry behavior:** Search-first — users land deep in the content hierarchy (specs or tips pages) and need to discover the broader context or adjacent resources.

---

## Current Page Ecosystem

The ecosystem consists of two levels:

### Leaf pages (ad-type specific)

| Page type | Example URL |
|-----------|-------------|
| Product overview | `/advertise/ads/sponsored-content/video-ads` |
| Tips & Best Practices | `/advertise/ads/sponsored-content/video-ads/tips` |
| Specs | `/advertise/ads/sponsored-content/video-ads/specs` |

### Hub pages (cross-ad-type)

| Hub | URL |
|-----|-----|
| Ads Guide (recently updated for LLM optimization) | `/advertise/ads/ads-guide` |
| Objective-Based Advertising | `/advertise/ads/objective-based-advertising` |
| Ads Best Practices | `/advertise/ads/best-practices` |
| Ads main | `/advertise/ads` |

!!! note "LLM Optimization Context"
    The Ads Guide hub page was recently updated for LLM/AI optimization. Design must support both human navigation and modular, self-contained content units that AI systems can easily parse and connect. This means designing content as discrete, complete units with strong interlinking — not just as part of a visual hierarchy.

---

## Tech Stack

| Layer | Tool |
|-------|------|
| CMS / Production | AEM (Adobe Experience Manager) via LEM |
| Hi-fi design | Figma + Our Community Design System |
| IA mapping | FigJam |
| Research baseline | SEO analytics + competitive benchmarking |

!!! warning "AEM Component Risk"
    The biggest identified risk is AEM component limitations. Any interlinking or navigation pattern we design must be validated against what is buildable in AEM before hi-fi commitment. New components require engineering estimates and may impact timeline.

---

## Services in Scope

- Research (competitive audit + SEO data)
- Wireframes
- Hi-fi Design
- Content Optimizations
- SEO Analysis
- Production (LEM)
- Localization

---

## Competitor References

| Competitor | URL | Model |
|-----------|-----|-------|
| Facebook Ads Guide | `facebook.com/business/ads-guide/update` | Left-sidebar nav with unified guide structure |
| Amazon Ad Specs | `advertising.amazon.com/resources/ad-specs` | Filterable specs table hub |

The Facebook model (sidebar nav across a unified guide) is the preferred reference, though its fit for LinkedIn's search-first entry pattern needs validation.

---

## RAPID Decision Framework

| Role | Owner |
|------|-------|
| **R**ecommend | Program Manager |
| **A**gree | Stakeholders |
| **P**erform | UX Design + Production |
| **I**nput | All |
| **D**ecide | Web Marketer |
