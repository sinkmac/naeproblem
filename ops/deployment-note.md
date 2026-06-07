# Deployment note

## Project

- Local path: `/home/sink/projects/naeproblem`
- GitHub repo: `https://github.com/sinkmac/naeproblem`
- Netlify site: `naeproblem`
- Netlify site ID: `aa0f1aa0-a69f-4d10-a89b-0ac1585b4fdb`
- Netlify admin: `https://app.netlify.com/projects/naeproblem`

## Live URLs

- Production URL: `https://naeproblem.netlify.app`
- Initial immutable deploy URL: `https://6a257d7f36389da75d30a79f--naeproblem.netlify.app`

## Verification performed

- `npm run check`: 0 errors, 0 warnings
- `npm run build`: successful with `@sveltejs/adapter-netlify`
- Production raw HTML checks confirmed:
  - `Naeproblem` present
  - `Browse the tools` present
  - `No affiliate links` present
  - forbidden civic/sport/gambling strings absent: `JustInCase`, `StillHere`, `LeavingForces`, `BiteForecast`, `noveltyodds`
  - 7 outbound tool links present
  - Broadband Switch Calculator has no outbound link
- Browser production visual check confirmed styled/polished page with no blocking visual issue.

## Domain note

- `naeproblem.scot` RDAP check returned HTTP 404 / `domain not found`.
- IONOS browser automation did not return a usable availability result, so final purchase/checkout should still be confirmed manually inside IONOS.
