# Lloyd's Local Services

Public website for Lloyd's Local Services, an owner-operated business in Newmarket, New Hampshire. The work covers home technology, smart home setup, troubleshooting, product research, project coordination, and selected assembly for the Seacoast and southern Maine.

The live site is [lloydslocalservices.com](https://lloydslocalservices.com/).

## How this is published

GitHub Pages serves the `main` branch from the repository root. `index.html` is the whole page. There is no build, package install, or generated output. `.nojekyll` keeps Pages from running Jekyll, so these files are copied as they are. `CNAME` sets the custom domain.

## Repository files

| File | Role |
| --- | --- |
| `index.html` | The site, including the contact form |
| `favicon.svg`, `favicon-16x16.png`, `favicon-32x32.png`, `apple-touch-icon.png` | Icons linked from the page |
| `og-image.png` | Social preview image |
| `photo-disclosure.css` | Styles for optional, closed-by-default job photos. Nothing in `index.html` links it yet |
| `CNAME` | Custom domain for GitHub Pages |
| `.github/workflows/ops-drift-gate-audit.yml` | Read-only dependency audit on pull requests and manual runs. It does not deploy the site |

The contact form posts to FormSubmit. Its action URL in `index.html` is the live form configuration.

## Local check

Open `index.html` in a browser, or serve this folder:

```bash
python3 -m http.server 8080
```

Then open `http://127.0.0.1:8080/`. The contact form only completes on the live site.
