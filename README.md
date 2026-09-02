# derail.games

The Derail Games Ltd company site. Static: two files, no build step, no deps.

Deployed to GitHub Pages; DNS stays at GoDaddy (apex A records to GitHub's
four IPs, everything else — notably the Google Workspace MX records — left
alone).

## Why this exists

Apple rejected the Apple Developer Program organization enrollment for
DERAIL GAMES LTD because `derail.games` served a registrar parking page.
Apple requires the org's website to be "publicly available, functional, and
the domain must be associated with your organization". The company record
section is there for that check: legal entity, company number, registered
office, director — matching Companies House exactly.

## Design

Palette and type are BloxTrace's, taken unchanged from
`../bloxtraceweb/src/styles/tokens.css`. Periwinkle `#6b76e5` stays the only
hue. If the tokens change there, change them here too — they are duplicated
on purpose, because this site has no build step and should never grow one.

## Local preview

```sh
python3 -m http.server 4173
```

## Deploy

Push to `main`. Pages publishes from the repo root; `CNAME` pins the domain.
