# Prospecting Workflow for Draft Client Sites

## Goal

Use fast, low-risk draft websites as a sales tool for businesses that do not yet have a website or are reluctant to invest in one.

The draft should feel:
- real enough to create momentum
- simple enough to produce in under 30-60 minutes
- generic enough to reuse across businesses in the same niche

## Core Idea

Instead of selling a website abstractly, show a business owner a believable first draft tailored to their industry.

This lowers resistance because:
- they can see what they are buying
- they do not need to imagine the result
- the conversation shifts from "Do I need a website?" to "Can we adjust this draft for my business?"

## Best Fit Use Cases

This workflow works best for:
- local service businesses
- firms with weak or no online presence
- businesses that mainly need trust, visibility, and lead capture
- industries where a 3-5 section site is enough to create value quickly

Examples:
- jewelers
- auto leasing brokers
- law firms
- med spas
- contractors
- roofers
- accountants
- dentists

## Offer Structure

Position the draft as:
- a no-pressure concept preview
- a sample homepage tailored to their business type
- a conversation starter, not a finished product

Avoid positioning it as:
- a free full build
- custom strategy work
- a complete brand identity exercise

## The 7-Step Workflow

### 1. Build an Industry Template Library

Create reusable starter templates for common niches you target.

Each template should include:
- hero section
- services or practice areas
- social proof or trust markers
- simple lead form or CTA
- FAQ
- footer with contact details

Keep the copy mostly placeholder-driven so you can swap in:
- business name
- city or service area
- phone number
- headline
- primary offer

### 2. Qualify the Prospect Fast

Before building the draft, gather:
- business name
- industry
- city
- whether they already have branding
- whether they already have a site
- key service categories
- one clear CTA: call, book, quote, consultation

This should take 3-5 minutes max.

### 3. Generate a Draft Homepage

Use the matching vertical template and customize only the high-signal parts:
- business name
- headline
- subheadline
- top 3 services
- CTA
- trust section
- contact details

Do not over-customize. The goal is speed, not perfection.

### 4. Publish a Private Preview

Host the draft on:
- a subdomain
- a hidden preview URL
- a local screenshot/PDF if you do not want to publish publicly yet

Recommended naming:
- `businessname-preview.yourdomain.com`
- `yourdomain.com/previews/businessname`

### 5. Outreach With the Preview

Best message style:
- short
- direct
- low-pressure
- visual

Example structure:
- noticed your business does not have a strong website presence
- created a quick sample homepage to show what one could look like
- no obligation, just thought it might help visualize the opportunity
- send preview link

### 6. Convert the Conversation

Once they respond, do not jump into technical details. Focus on:
- credibility
- business outcomes
- ease of getting started

Good next-step questions:
- "Would you want something simple like this, or something with booking/quotes?"
- "Should the main goal be calls, quote requests, or showroom visits?"
- "Do you want us to keep this lightweight or build something more custom?"

### 7. Move Into Your Standard Delivery Lane

After interest is confirmed:
- use `Vite + DreamHost` for brochure sites and simple forms
- use `Next.js + Vercel` for anything with auth, payments, dashboards, or richer application logic

## Speed Rules

To keep this profitable, follow these rules:
- spend no more than 30-60 minutes on the first draft
- never design from scratch for a cold lead
- reuse the same layout per niche
- customize only the copy blocks that create relevance
- do not add complex forms, auth, or CMS to prospect drafts

## Suggested Folder System

```text
prospecting/
  templates/
    jeweler.html
    auto-leasing.html
    law-firm.html
  prospects/
    2026-03-12-acme-jewelers/
      notes.md
      draft.html
      screenshot.png
```

## Copy Formula for Draft Sites

Use this structure across most industries:

1. Hero
   Clear benefit + trust + CTA
2. Core Services
   3 cards max
3. Why Choose Us
   3-4 trust bullets
4. Reviews or trust indicators
5. Process
   3 simple steps
6. Lead CTA
   Call / book / request quote
7. FAQ
8. Footer

## Recommended Business Categories

Start with categories that are:
- easy to template
- trust-based
- geographically local
- not operationally complex

Strong categories:
- law firms
- jewelers
- auto leasing brokers
- contractors
- med spas
- dentists
- accountants

Harder categories:
- marketplaces
- restaurants with heavy ordering logic
- multi-role SaaS platforms
- businesses that need deep backend workflows from day one

## Sales Framing

The draft-site offer should sound like:

"I put together a sample homepage for your business so you can see what a stronger online presence could look like. If you like the direction, I can turn it into a real site quickly."

That framing is simple, concrete, and low-friction.

## Next Evolution

Once this workflow is working, create:
- one reusable HTML starter per niche
- one screenshot generator flow
- one outreach template per niche
- one conversion checklist for moving from draft to paid project
