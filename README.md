# Maguire Solicitors — website redesign

A complete redesign of [maguiresolicitors.co.uk](https://www.maguiresolicitors.co.uk/)
for Maguire Solicitors, Glasgow — immigration and asylum specialists, established 2011.

## Files

| File | Description |
|---|---|
| `index.html` | **The site.** Navy & gold, using the firm's existing brand colours (`#2a2e42` / `#efbc33`). |
| `index-sandstone.html` | Alternate "Sandstone & Slate" palette, kept for comparison. Structurally identical. |
| `assets/team/opt/` | Optimised team photographs and the Scottish Legal Aid Board sticker. |

Each HTML file is fully self-contained — no build step, no dependencies, no server.
Team photographs and the SLAB sticker are embedded as data URIs, so a file works
opened directly from disk. Fonts (Fraunces, Manrope) load from Google Fonts.

Open `index.html` in a browser, or serve the folder:

```
python3 -m http.server 8000
```

## What the redesign does

- **Triage-first hero.** Plain-language entry points ("I've been arrested or charged")
  rather than legal category names, because people don't arrive knowing they need
  "SSSC Professional Regulation".
- **Immigration-led.** The firm's founding practice gets a dedicated section covering
  personal, business and investor routes, ahead of the general practice index.
- **Legal aid, stated plainly.** SLAB registration surfaced as its own section rather
  than footer small print — much of the firm's work is legally aided.
- **All 10 practice areas** as an expandable index carrying 106 specific services.
- **Searchable team roster** of 35 people, filterable by role.
- Light and dark themes, keyboard accessible, `prefers-reduced-motion` respected,
  no horizontal scroll, WCAG AA contrast throughout.

## Before going live

- [ ] **Law Society of Scotland registration number** — currently a visible placeholder
      in the footer. Scottish solicitors must identify their regulator and registration
      details; this is a launch blocker.
- [ ] Wire the enquiry form to a real mailbox (it validates and confirms, but sends nothing).
- [ ] Confirm Karah Murphy's exact job title, and Alysha's surname.
- [ ] Photographs for the seven staff still shown as initials.
- [ ] Consider splitting practice areas into separate URLs for SEO and deep linking —
      the old site had eight distinct pages; this is a single page with anchors.

## Content provenance

Copy, team names and roles, testimonials, address and the SLAB wording are taken from
the firm's existing site. Nothing has been invented — where information was unavailable
it is marked as a visible placeholder rather than filled with plausible text.
