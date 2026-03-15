# Draft Site Generator Overview

## Purpose

This project direction is about building a system that can quickly generate polished static website drafts for real businesses that do not yet have a website, have a weak website, or are hesitant to commit to paying for one without seeing a concrete example first.

The draft site acts as:
- a sales tool
- a low-pressure proof of concept
- a conversation starter
- a way to shift the discussion from "Do I need a website?" to "Can we turn this into my real site?"

## Business Context

The intended workflow is for a web developer creating websites for clients across multiple categories:
- static marketing and brochure websites
- websites with submission forms
- more complex web applications
- ecommerce or Stripe-integrated sites

Current infrastructure assumptions:
- use DreamHost for simple static websites and lightweight PHP-backed form submissions
- use Vercel for more complex applications such as shops or web apps
- use Vite for simple static sites
- use a Node.js-based framework such as Next.js for more complex app-style projects

## Core Prospecting Idea

Instead of trying to persuade a business owner using only words, create a believable first-draft homepage tailored to their niche and business identity.

The expected input for each prospect is:
- business name
- business category
- scraped Google description
- optional city, phone number, address, CTA, and style direction

The expected output is:
- a polished static HTML draft site
- optional assets folder
- screenshot for outreach
- temporary preview URL

## Recommended Workflow

### 1. Find a business

Gather:
- business title
- business category
- scraped business description

Optional enrichment:
- city
- address
- phone number
- CTA goal such as call, quote, book, or consultation
- visual direction such as luxury, corporate, modern, minimal, or aggressive

### 2. Normalize the input

Convert the raw business details into structured draft inputs:
- business type
- likely service list
- likely trust signals
- most appropriate CTA
- best tone and visual style

### 3. Choose a category blueprint

Use a reusable template family based on business type.

Examples:
- jeweler -> luxury, refined, elegant, consultation-oriented
- law firm -> professional, authoritative, trust-focused
- auto leasing -> fast-moving, conversion-focused, quote-driven

### 4. Generate the page

Assemble the static site from reusable page sections:
- hero
- services or practice areas
- trust section
- testimonials or trust bar
- CTA section
- contact/footer

### 5. Apply visual polish

Use curated components and effects to make the draft feel premium and convincing.

This may include:
- animated hero sections
- higher-end card layouts
- testimonial sections
- FAQ accordions
- CTA bands
- premium typography and gradients

The goal is not random component usage. The goal is a curated internal library of approved building blocks.

### 6. Export and publish

Generate a final static draft with:
- `index.html`
- assets
- metadata
- screenshot

### 7. Send the draft to the business

Use the draft site and screenshot in outreach as a low-pressure preview of what their online presence could become.

## Architecture Recommendation

The recommended v1 architecture is:
- `Node.js + TypeScript`
- static HTML generation
- no runtime backend required for generated draft sites
- `JSON` or `YAML` input files for business data
- `Playwright` for screenshots
- reusable templates and section partials

This should be approached as a draft-site generation pipeline, not just a folder of HTML files.

## Suggested Generation Stages

### 1. Business ingest

Accept raw prospect data and normalize it.

### 2. Category mapper

Map business category to:
- page blueprint
- tone preset
- CTA style
- color direction
- recommended sections

### 3. Draft generator

Build the final static HTML page from templates and curated components.

### 4. Asset polisher

Apply theme, colors, typography, spacing, and visual effects.

### 5. Publisher

Output the generated site into a slug-specific folder and prepare it for hosting.

### 6. Screenshotter

Capture a polished screenshot to use in outreach messages.

## Project Structure Direction

It is reasonable to use this repository as the working directory for the draft-site generator system and the generated sites, at least for v1.

Suggested structure:

```text
project-root/
  docs/
  templates/
  scripts/
  prospecting/
    input/
    output/
      acme-law-group/
        index.html
        assets/
        meta.json
        screenshot.png
      golden-state-jewelers/
        index.html
        assets/
        meta.json
        screenshot.png
```

Recommended separation of responsibilities:
- `templates/` for reusable niche templates and section patterns
- `scripts/` for generation and deployment logic
- `prospecting/input/` for structured business input data
- `prospecting/output/` for generated draft websites

This is a good starting approach. If the system grows significantly, it may later make sense to split the generator itself from the archive of generated sites.

## Hosting Direction

The recommended temporary hosting approach is to use DreamHost-hosted preview URLs under the main domain `bld-systems.com`.

This means:
- generate the static HTML draft
- upload it to DreamHost
- expose it under a branded preview URL
- share that URL with the prospect

Example URL patterns:
- `preview.bld-systems.com/acme-law-group`
- `preview.bld-systems.com/golden-state-jewelers`
- `acme-law-group.bld-systems.com`
- `golden-state-jewelers.bld-systems.com`

Recommended approach for v1:
- use the subfolder pattern first because it is simpler operationally
- move to individual subdomains later if needed for higher-value prospects

## Why This Can Work

This system can be effective because it reduces prospect hesitation:
- the business can see a real example instead of imagining one
- the preview feels personalized
- the conversation becomes concrete quickly
- the draft creates momentum and pseudo-commitment

The key rule is to keep the drafts fast and reusable:
- do not build from scratch for every lead
- customize only the high-signal content
- keep the first draft lightweight
- treat the draft as a sales preview, not free custom consulting

## Summary

The long-term vision is to create a repeatable sales conversion engine for cold prospects:
- ingest business info
- map the business to a niche template
- generate a polished static draft site
- host it temporarily under a branded preview URL
- use the draft plus screenshot in outreach
- convert interested businesses into real paid projects

In short, this is not just a website generator. It is a system for turning cold leads into warmer, more concrete sales conversations through fast, convincing website previews.
