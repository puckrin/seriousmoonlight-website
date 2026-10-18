# Serious Moonlight — holding page

Static site at **seriousmoonlight.co.uk**. Serious Moonlight is the trading name of a UK
sole trader and the umbrella for several independent software projects. This site is the
umbrella, not a product page.

**v1 scope: one bare-bones page** — name, a line of copy, a descriptor, and the legal
disclosure in the footer. No multi-page site, blog, CMS or component library.
**v2 (started 2026-10-09):** a plain list of links out to live project sites — Taneleer and
Tidemarq are released; Bellows sits under a "Coming soon" heading until it ships, then
moves up. Unannounced projects are not listed. It is a hand-written
`<ul class="projects">`, one `<li>` per project with a one-line description. No data file,
no templating. This site does not style
itself after any project's identity.

## The footer is load-bearing

Required by UK business-name disclosure rules; it must contain:

- **Shaun Puckrin**, trading as Serious Moonlight
- **Lytchett House, 13 Freeland Park, Wareham Road, Poole, Dorset, BH16 6FA**

A home address must never appear in this repo, in commit metadata, or on the site.
Serious Moonlight is a sole trader: never render "Ltd", "Limited" or anything implying
incorporation.

## Hard constraints

- No analytics, tracking or cookies. Not without an explicit, separate decision.
- No forms. Contact is a `mailto:` link or nothing; omit it until a working
  `@seriousmoonlight.co.uk` address exists.
- No third-party fonts or any other network requests. System fonts only.
- Static output; must work with JavaScript disabled. Fast and small.

## Design (decided 2026-10-05)

"Paper and ink": warm off-white `#F6F2E9`, near-black `#1E1B16`, system serif stack
(Charter, Iowan Old Style, Georgia) for wordmark and copy, system sans for the footer,
dark variant via `prefers-color-scheme`. Logo is `logo.svg` — a flat crescent rising over
a horizon line, `currentColor`, also the favicon (inline data URI).

## Tone

Understated: a small studio's calling card, not a startup landing page. No hero CTA, no
superlatives, no emoji. The page line is "Know when to stay in. Get things done." — a
deliberate, one-off exception to "no Bowie references in the copy". Don't add more, and
don't theme the site around the tour.

## Hosting

GitHub Pages, deployed by `.github/workflows/deploy.yml` on push to `main`. Only
`index.html`, `logo.svg`, `CNAME` and `.nojekyll` are published; everything else in the
repo is not served. DNS is at Porkbun.
