DESIGN.md — electricianalgarve.com
Read this file before making any design or layout change to this project. Do not deviate from it without explicit sign-off, logged in the Changelog below.
Aesthetic family
Editorial / trade-craft — closer to a specialty print publication or an architecture studio's site than a SaaS landing page or local-service template. Reference points (not to copy, but to anchor the feel):

* A well-set editorial magazine site — confident typography carries the page, not decoration.
* A specialty craftsperson or architecture studio site — restrained, material-led, unhurried. Explicitly NOT: SaaS startup, "local business template," dark-mode-plus- neon-accent (this was tried and rejected — it's its own cliché, not an escape from one).

Typography

* Display: Fraunces, weight 400 only (never 600+, never faux-bold)
* Body: Source Sans 3, 400 regular / 600 for emphasis only
* Mono: reserved strictly for the phone number and any numeric index — never a default label/button voice
* Max line length for body paragraphs: 68 characters (enforce via max-width, not container width)

Color

* Background: #FAF7F0 (warm paper — not pure white)
* Ink: #1A1815 (near-black — not pure black)
* Accent: #3D5C56 (muted petrol) — used ONLY for link underlines, numeric indices, and at most one hairline rule per section
* CTAs (Call, WhatsApp) are EXEMPT from the quiet palette — they must pass 7:1 contrast against the paper background and read as the obvious exit ramp, even though nothing else on the page is high-contrast
* No gradients. No dark mode. One accent color only.

Spacing
Use only: 8px, 16px, 24px, 40px, 64px, 96px, 140px. Section vertical padding = 140px desktop / 64px mobile. No arbitrary values.
Banned patterns (P0 — screams AI-generated, never ship these)

* Purple/blue gradients, Inter font
* Hero-plus-three-stat-row as the default hero shape
* Icon-in-a-rounded-square or icon-in-a-circle used as a repeated system
* "Everything in cards" — repeated bordered-box-with-shadow containers down the page
* Glassmorphism / backdrop-blur as decoration
* Center-aligned-everything
* Rounded corners above 4px radius, anywhere
* Dot-pagination carousels, accordion chevron-in-circle widgets

Banned patterns (P1 — obvious AI smell, fix before shipping)

* Identical spacing applied uniformly to every section regardless of content
* Generic CTA copy ("Get Started," "Learn More," "Unlock," "Elevate")
* A card, box, or container using border + background fill + shadow simultaneously (pick at most one)

Self-audit process (required before presenting any build to the user)

1. Build the section.
2. Check it against the P0 list above, line by line. Fix anything that matches.
3. Check it against the P1 list. Fix anything that matches.
4. Only then take a screenshot and present it.
5. State explicitly which fonts and hex values are actually computed on the key elements (not "I used Fraunces" — the literal computed style), so drift is caught immediately rather than after the fact.

Process rules

* One section at a time. Confirm with the user before moving to the next.
* Do not touch, "improve," or modify any section/file not explicitly named in the current request.
* Before writing code, restate the relevant part of this spec back to the user in your own words to confirm shared understanding.
* After writing CSS, show the raw CSS for the changed section before rendering a screenshot.

Changelog

* 2026-08-29: Established this file. Locked type (Fraunces/Source Sans 3), color (#FAF7F0 / #1A1815 / #3D5C56), banned dark-mode-plus-lime-accent system used previously. Hero left untouched pending separate pass. Reason for reset: prior sessions repeatedly reverted to generic patterns (bold sans hero, card grids, wrong colors) despite detailed one-off prompts — this file exists so the constraints persist across sessions instead of being re-explained and re-lost each time.
* 2026-08-29 (later same day): Explicit sign-off received in chat to deviate from this entire file for the current build — full-page redesign toward a Mark Levinson (marklevinson.com) reference direction: deep near-black theme (#0D0A1A/#130f22/#1e1840), DM Serif Display + DM Sans + Syne typography, lime #C8F400 as primary accent and deep purple #6B21D4 as secondary accent, card-based UI (bordered cards, icon circles, image thumbnails) reinstated including the trust bar, mobile reviews carousel, service card images, and Why Us icon/metric grid removed in the prior reset. This supersedes every rule above (aesthetic family, type, color, spacing scale, P0/P1 bans) for this build. Content/SEO (headings, copy, links, alt text, schema) was kept unchanged per the standing content rule the user restated in the same request. Not yet reconciled with the rest of this file — if a future session is asked to follow DESIGN.md's original system again, that is also a explicit-sign-off change and should get its own changelog entry rather than silently reverting.
