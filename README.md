# javidz.com

Static website files for **javidz.com**, the personal portfolio website of Javid Ahmad.

## Overview

This repository contains a self-contained static site export. It can be served by any static hosting provider or basic HTTP server. There is no package manager, framework build step, or server-side application code required.

## Project Structure

```text
.
├── index.html
├── support.js
└── cdn-cgi/
    └── scripts/5c5dd728/cloudflare-static/email-decode.min.js
```

- `index.html` - main website entry point.
- `support.js` - runtime script required by the exported page.
- `cdn-cgi/scripts/5c5dd728/cloudflare-static/email-decode.min.js` - local copy of the email decoding script referenced by the page.

## Local Development

Run a local static server from the project root:

```sh
python3 -m http.server 8080
```

Open the site at:

```text
http://localhost:8080/
```

## Deployment

Deploy the full contents of this folder to the web root for `javidz.com`.

Required files and folders:

```text
index.html
support.js
cdn-cgi/
```

The page loads Google Fonts and React/Babel from public CDNs through the exported runtime, so the deployed site should allow outbound access to those CDN resources.

## Notes

The current site was generated from a static HTML export and adapted for direct hosting as `index.html`.
