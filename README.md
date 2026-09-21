# Wildseed — website concept mockup

**This is an unapproved design concept, produced by Dispenza, for a prospective redesign of wildseedextracts.com.**
**It is not affiliated with, endorsed by, or published by Wildseed, LLC, and it is not their live website.**

---

## What this is

A single-page design concept for a licensed California cannabis contract manufacturer based in
Arcata, Humboldt County. It is a visual and structural proposal for client review, not a
production website. Nothing here is transactional: there is no cart, no checkout, no account,
and no price is published anywhere.

## Live preview

**https://nicoledreo.github.io/wildseed-web-mockup/**

## Running it locally

It is a static page with no build step and no dependencies. Any static file server works:

```bash
python -m http.server 8000
# then open http://localhost:8000
```

Opening `index.html` directly from the filesystem mostly works, but the self-hosted fonts and
a few assets are more reliable over `http://`.

## What is in here

```
index.html                 the whole page — 11 sections, anchor navigation
design-system/
  tokens.css               the --ds-* design tokens (colour, type, space, radius, motion)
  structural.css           the shared component layer
  overrides.css            this build's layout and art direction
  fonts.css + fonts/       self-hosted Koulen and Karla (no third-party font CDN)
  site.js                  nav drawer, scroll reveals, count-ups
assets/                    the images the page and stylesheets actually reference
```

## Design direction

- **Palette** measured off the client's existing site: navy `#051E37` and `#1E4884`,
  lime `#E2FB5B`, cream `#E8E1DF`, pale blue `#D2EDFF`.
- **Type**: Koulen for display, Karla for body. Both self-hosted.
- **Rhythm**: alternating navy and cream full-width bands, uppercase display type, generous
  vertical air, and one band per viewport height on desktop.
- **Navigation**: transparent over the hero, solidifying on scroll via a scroll-driven
  animation, with a class-toggle fallback where that is unsupported.
- Responsive at 1440 / 1024 / 768 / 375. Verified: no horizontal overflow, no console errors,
  and text contrast meeting WCAG AA at every breakpoint.

## Imagery provenance

This matters, and the three categories are not interchangeable:

| Category | Files | Notes |
|---|---|---|
| **Real client photographs** | `cart-filling-hero`, `lab-process-floor`, `lab-benches`, `extraction-bench-detail`, `facility-texture` | Supplied by the client. Show their actual Arcata facility. |
| **From the client's own website** | `wildseed-logo-white`, `about-tile-1/2/3` | Their logo and the photographs from their existing About section. The About copy is theirs too. |
| **AI-generated placeholder** | `gen-rosin-jar`, `gen-cart-wood`, `gen-cart-closeup`, `gen-manufacturing`, `gen-lab-interior`, `gen-field-walk`, `svc-cart-filling`, `svc-rosin-press`, and all `coast-*` / `redwood-*` / `humboldt-*` / `river-*` / `bluff-*` / `dawn-*` landscape frames | Illustrative stock only. The product frames are **generic, unbranded objects — not the client's actual goods**, and every one says so in its `alt` text. The landscape frames are atmosphere, not the client's premises. |

The two product packaging photographs (`product-live-sauce-*`) are from the client's public
wholesale listing and show real retail packaging.
> **Note on `gen-field-walk`:** the field photograph on the Arcata band is a *generated restage* of a
> photograph on the client's site, made at higher resolution to survive full-bleed display. It shows
> different people on a different farm and is not the client's photograph.

## Not ready to publish

This concept is not production-ready. Open items, in rough order of importance:

1. **AI-generated product imagery must be replaced** with real product photography before this
   could ever go live. It is placeholder art standing in for a real licensee's goods.
2. **A sourcing figure on this page is UNVERIFIED.** The "100% Humboldt sourced" statistic in
   the counts band has not been confirmed by the client, whose own brief marks it "confirm
   before publishing". It is shown here because this preview is meant to mirror the review
   build exactly, **not because it has been substantiated**. It must be verified or removed
   before any of this becomes a real site.
3. **OCal certification is not claimed anywhere**, deliberately. Public records list the
   company as an applicant, which is not certification. No OCal mark appears on this page and
   none should until a current certificate is in hand.
4. **The quote inbox is a placeholder** in this copy. The real address is unconfirmed.
5. **No B2B phone number** has been supplied for the facility.
6. **Only five client photographs exist.** Two of the five service-card backgrounds now use
   generated frames, and the remaining three use the nearest available client photograph rather
   than a literal match for that service.
7. **An age gate** is present on the client's live site and is not reproduced here.

## How this public copy differs from the review build

The internal client-review build is not what is published here. This copy is generated by a
staging script that deliberately:

- removes the one internal status note that names a real contact address;
- replaces the quote inbox with a placeholder;
- strips an account-linked referral parameter from outbound wholesale links;
- strips all source-code comments from the stylesheets;
- ships only the images the page actually references;
- adds the concept-mockup banner and `robots: noindex, nofollow`;
- replaces the client copyright notice with the agency attribution above.

## Licence and ownership

The Wildseed name, logo, product photography and About copy belong to Wildseed, LLC and are
used here solely to illustrate a design proposal for that company. The California licence
numbers shown on the page are matters of public record. No part of this repository asserts any
claim of ownership over the client's brand or intellectual property.
