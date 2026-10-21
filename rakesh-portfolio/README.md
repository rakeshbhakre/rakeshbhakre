# Rakesh Bhakre portfolio rebuild

A static editorial portfolio built from the supplied `index.html` and the résumé details provided in chat. The source uses HTML, CSS, and a small inline JavaScript interaction for the GARUDX architecture explainer. It has no third-party framework, remote font, analytics, or external script dependency.

## Preview locally

From this directory run:

```sh
python3 -m http.server 8000
```

Then open `http://localhost:8000`. The portfolio is responsive and self-contained. The GARUDX process map is an interactive project explainer, not a live scan feed.

## Contents

- `index.html`: portfolio homepage
- `blueprint.md`: section-by-section design and component plan
- `favicon.svg`: custom monochrome vector monogram
- `manifest.webmanifest`: web app metadata
- `assets/Rakesh_Bhakre_Resume.pdf`: résumé download from the provided attachment
- `privacy-policy/index.html`: privacy route at `/privacy-policy/`
- `terms-of-service/index.html`: terms route at `/terms-of-service/`

## Production setup placeholders

No hosting provider or deployment account was supplied, so no production DNS values are invented and no production deployment has been made.

- Canonical host target: `https://www.rakeshbhakre.in/` (verify before switching production files).
- Apex `@` A/AAAA records: `[HOST A/AAAA TARGETS]`
- `www` CNAME: `[HOST WWW CNAME TARGET]`
- Provider ownership TXT record: `[PROVIDER VERIFICATION NAME + VALUE]`
- CAA requirements, if any: `[HOST CAA REQUIREMENTS]`
- TLS certificate must include both `rakeshbhakre.in` and `www.rakeshbhakre.in`.
- Redirect HTTP to HTTPS and apex to the canonical `www` URL after certificate and DNS verification.
- Configure the host to serve the legal documents at `/privacy-policy/` and `/terms-of-service/`; preserve slashless access with a redirect or rewrite.

Before launch, confirm those record values with the selected host, check canonical redirects and certificate coverage, review the legal stubs for actual provider practices and applicable law, and inspect the rendered source for host-injected branding. The legal files are starter copy, not legal advice.
