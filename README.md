# home

The static welcome page served at <https://home.1995parham.me>.

That name has to resolve and answer for other reasons, so this gives it something friendly to return instead of a `404`. It is just a front door: no links, no navigation, nothing behind it.

It doubles as a liveness signal. Reaching it means the house still has power and an uplink, and the internet-facing host is up and serving — so the page says as much.

## Serving

nginx clones this repository and serves it as a static root, configured from a private infrastructure repo. A push here becomes live on the next provisioning run.

## Constraints

Everything is inline: no CDN, no webfont, no external request of any kind. Many visitors cannot reach jsdelivr, unpkg or `fonts.googleapis.com`, and a page that depends on them renders broken.
