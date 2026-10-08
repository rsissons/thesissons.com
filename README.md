# thesissons.com

The project showcase at https://thesissons.com: one static page, hosted free on GitHub Pages.

## Business section

The Business section at the top leads with the PhotoWallz featured card (https://photowallz.com/), written into `index.html` by hand since its repo is private (screenshot `img/photowallz.webp`). Below it come public repos with the `business` topic, then the private products in `PRIVATE_BUSINESS` (hand-written cards with an "Ask me about it" email button instead of Open and Source). The Email AI Assistant screenshot (`img/email-ai.webp`) is its dashboard running on made-up demo data, never real customer email.

## How projects get listed

The page reads Ron's public repos from the GitHub API when it loads. A repo appears if it has one of these topics (the first match, in this order, picks its section):

| Topic | Section |
|---|---|
| `business` | Business |
| `retirement-planning` | Retirement planning |
| `kids` | For the kids |
| `game` | Games |
| `cooking` | Cooking |

To add a project: make the repo public, give it one of those topics, and set its website (the "homepage" in the repo's About box). To give it a screenshot, add `img/<repo-name>.webp` (800×500) and an entry in `IMAGES` in `index.html`; otherwise GitHub's generated preview card is used. Nicer names go in `TITLES`.

`FALLBACK` in `index.html` is a built-in copy of the list, shown if the GitHub API can't be reached. Update it when projects change.

## Domain

`thesissons.com` and `www.thesissons.com` point here (the `CNAME` file). Email for the domain (Google Workspace MX and SPF records) is separate and untouched.
