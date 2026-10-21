# Rakesh Bhakre Portfolio

## Pre-launch structural placeholders

Configure these four launch assets before publishing the section designs.

1. **Domain and SSL setup**
   - Canonical origin: `https://www.rakeshbhakre.in/`. A browser check of the supplied domain currently lands on the `www` host; confirm this is still the preferred canonical host at deployment.
   - DNS values are hosting-provider-specific and must not be guessed. Fill in the deployment record sheet with: apex `@` A/AAAA target `[HOST A/AAAA TARGETS]`; `www` CNAME target `[HOST WWW CNAME TARGET]`; ownership TXT record `[PROVIDER VERIFICATION NAME + VALUE]`; any required CAA records `[HOST CAA REQUIREMENTS]`.
   - Issue and verify a TLS certificate with both `rakeshbhakre.in` and `www.rakeshbhakre.in` in its SAN list. Redirect HTTP to HTTPS and redirect the apex to the canonical `www` host with a permanent redirect. Set one canonical URL per page.
   - Verify after DNS propagation with the provider's domain checker, `dig` or `nslookup`, a TLS certificate inspection, and HTTP status checks for apex, `www`, and HTTP redirects. Enable HSTS only after HTTPS and redirects are verified.

2. **Favicon and manifest**
   - Custom monochrome vector file: `/favicon.svg`, a simple `RB` letterform in muted olive on warm paper. No emoji, stock mark, or platform icon.
   - `/manifest.webmanifest` names the portfolio, uses `#F4F0EA` as the theme/background color, and points to the SVG icon. Confirm icon rendering and manifest response in browser developer tools after deployment.

3. **Attribution stripping**
   - The delivered source has no generator tag, template credit, vendor badge, or platform attribution. No third-party framework or hosted font is required.
   - Before launch, inspect rendered pages, source, footer, metadata, and response headers for `Made in`, `Built with`, `Powered by`, generator strings, or host-injected badges. Remove platform branding where permitted by the host's terms; do not misrepresent the hosting provider.

4. **Legal infrastructure**
   - Dedicated static page routes: `/privacy-policy/` and `/terms-of-service/`, backed by `privacy-policy/index.html` and `terms-of-service/index.html`. Slashless routes should redirect to the trailing-slash version or resolve to the same document.
   - The included documents are starter stubs. Confirm actual hosting logs, analytics, retention, third-party embeds, governing law, and content permissions before publishing. Replace or approve the notices for the final setup; they are not legal advice.

## Design system

- Base: warm paper `#F4F0EA`.
- Text: carbon ink `#1E1E1E`.
- One structural accent: heritage olive `#505A3D`.
- Borders and muted text are opacity tints of those three colors, not extra hues. No white or black canvas, gradients, neon, or extra accents.
- Display: editorial serif with tight tracking (`Newsreader`, then Georgia/system serif). Interface: functional system sans (`Inter`, then system sans). Mono is reserved for small indices and labels.
- 1px hairlines, tabular proof layout, large section spacing, asymmetric columns, and the native system cursor.
- Motion has an editorial, engineering-led purpose: a one-time kinetic title reveal, a traced SVG architecture path for GARUDX, selectable pipeline stages, and one-time in-view section reveals. Use 620–1350ms easing for these staged moments and 150–180ms for ordinary controls. Do not hijack scrolling, add cursor trails, bounce, run infinite decorative loops, or animate proof values. Keep a complete static fallback and honor `prefers-reduced-motion`.
- No stock photo or corporate illustration is included. The pipeline is an exact project-system diagram, not a decorative floating-card graphic. Any future photo must be a real, authentic documentary asset and must not imply project evidence that was not supplied.

#### [Section: Global Nav]

- **Structural Blueprint:**
  - Grid & Alignment: Centered 12-column max-width shell; wordmark anchors left, four short links align right. Sticky header stays on a warm-paper translucent surface with a single 1px hairline.
  - Visuals & Art Direction: No image in navigation. If a location detail is later added, use a real documentary photograph of a Navi Mumbai street or building facade, eye-level 35mm framing, hard late-afternoon side light, paper/ink/olive palette, no posed stock subject.
  - Styling Tokens: Paper `#F4F0EA`, ink `#1E1E1E`, olive `#505A3D`; 1px `rgba(30,30,30,.12)` border; serif wordmark accent with sans links; CSS targets `.site-header`, `.nav-row`, `.nav-links`; sticky offset `4.4rem`.
- **Component Blueprint:**
  - Semantic tree: `header.site-header > .wrap > a.wordmark + nav[aria-label] > ul > li > a`.
  - Interactive states: Native anchors; hover changes link ink to olive in 150ms; visible keyboard focus ring; no custom cursor or animated underline; wraps into a two-row header on narrow screens.
- **Display Copy (Production-Ready):**
  - Header: `Rakesh Bhakre`
  - Subhead / Body: Navigation labels: `Work`, `Skills`, `Experience`, `Contact`.
  - CTA / Action: `Contact`

#### [Section: Hero]

- **Structural Blueprint:**
  - Grid & Alignment: Asymmetric 8/4 split on the 12-column frame. Kinetic four-line serif headline and actions left; a custom GARUDX process map right. Stack the process map after the primary copy on mobile.
  - Visuals & Art Direction: The right-side visual is a hand-coded SVG system diagram of the actual upload, scan, findings, and report stages, not a live telemetry feed or generic floating-card illustration. No portrait or generated product mockup is used. If Rakesh supplies a real portrait later, commission an environmental portrait at eye level, 50mm lens, in a real work setting, with window-side light, architectural shadow, and natural paper/ink/olive wardrobe tones.
  - Styling Tokens: Paper `#F4F0EA`; ink `#1E1E1E`; olive `#505A3D`; serif heading `clamp(3.55rem, 9vw, 8.4rem)` with tight tracking; sans body; mono map labels; buttons use olive fill or transparent hairline outline. The title enters with an 820ms one-time clipped line reveal; the SVG path traces over 1350ms once when visible.
- **Component Blueprint:**
  - Semantic tree: `main > section#top[aria-labelledby] > .hero-grid > div(eyebrow,h1,lede,actions) + aside[aria-label](SVG map, step-button group, aria-live caption, static-feed note)`.
  - Interactive states: Four native buttons select upload, scan, findings, or report, highlighting the matching node and updating a factual caption. This is an architecture explainer, not simulated scan activity. Resume and work actions stay native links. Visible keyboard focus, 150ms button hover, and a fully static `prefers-reduced-motion` state.
- **Display Copy (Production-Ready):**
  - Header: `I build software that gets the work done.`
  - Subhead / Body: `I’m Rakesh, a software engineer with experience building application features, APIs, dashboards, and product workflows. My work spans Java and Spring Boot, React, Node.js, and applied computer vision.`
  - CTA / Action: `Explore selected work` · `Download résumé`

#### [Section: Proof / Value Matrix]

- **Structural Blueprint:**
  - Grid & Alignment: Four equal tabular columns separated by hairlines; two-by-two on mobile. Values are static text, not animated or counted up.
  - Visuals & Art Direction: No supporting photo. If real proof media is later supplied, use a documentary close-up of the actual GARUDX dashboard or candid event operations, photographed at a three-quarter angle in natural low-key light; retain muted olive, carbon, and paper tones and caption its source/context.
  - Styling Tokens: Olive metric numerals in serif; ink/opacity labels in sans; 1px ink-tint dividers; consistent numeric baselines using tabular figures.
- **Component Blueprint:**
  - Semantic tree: `section[aria-labelledby] > header(section index,h2,intro) + div[role=list] > div[role=listitem](value,label)`.
  - Interactive states: Values remain static and never count up. Cards may enter once with the shared 620ms section reveal; no faux live-state behavior. Links to deeper project evidence are located in the work section.
- **Display Copy (Production-Ready):**
  - Header: `Work with a record.`
  - Subhead / Body: `A few details from product security, software delivery, event operations, and team competition. Each fact points to specific work or experience below.`
  - CTA / Action: `Review the project details`

#### [Section: Editorial Feature Showcases]

- **Structural Blueprint:**
  - Grid & Alignment: Three editorial rows use project metadata in a narrow left rail, narrative in the wide center, and one action in a right rail. Row order: featured GARUDX, featured RestoQR, then a compact Intelligent Traffic Surveillance research note. Stack action below narrative on mobile.
  - Visuals & Art Direction: No screenshot is fabricated. GARUDX's actual system flow is shown in the hero diagram. If screenshots are later supplied, capture the real product UI at native resolution: GARUDX scan-results dashboard straight-on with neutral room reflections; RestoQR kitchen display at a slight 20-degree side angle in an operating restaurant with practical overhead light; traffic-project image only as a genuine frame from the user's system. Use natural low saturation and paper/ink/olive framing, with a caption that gives context.
  - Styling Tokens: Paper surface; ink body; olive project indices and actions; 1px hairline separators; serif titles `clamp(1.8rem, 3.2vw, 2.7rem)`; mono tags with thin ink borders. The traffic row uses a smaller title, tighter spacing, and shorter copy.
- **Component Blueprint:**
  - Semantic tree: `section#work > header + div.work-list > article.project[aria-labelledby]`; each article has metadata, `h3`, factual body, `ul.tag-list`, and external-link rail.
  - Interactive states: One-time in-view reveals sequence each project row with no scroll control. Native external links open a new tab with `rel="noreferrer"`; hover text changes to olive/ink with a 150ms transition; visible focus ring. No fake demo, fabricated screenshot, or unsupported client outcome.
- **Display Copy (Production-Ready):**
  - Header: `Systems built for use.`
  - Subhead / Body: `A security platform, a computer-vision research project, and a restaurant operations product. The summaries focus on my work and the technical decisions behind it.`
  - CTA / Action: `View product` · `View source` · `Visit live product`

#### [Section: Technical Specifications]

- **Structural Blueprint:**
  - Grid & Alignment: Asymmetric 5/7 split. Short framing paragraph on the left; semantic two-column table on the right, with hairline-separated category rows.
  - Visuals & Art Direction: No visual asset; the structured table is the evidence surface. If adding a photograph, use a true close-up of the actual workstation or device used for project testing, shot from a 45-degree overhead angle with controlled window light and no staged floating interface elements.
  - Styling Tokens: Table headings in olive mono; values in ink-tint sans; 1px carbon hairlines; paper base. Keep text contrast high and row padding consistent.
- **Component Blueprint:**
  - Semantic tree: `section#skills > header + div.technical-grid > div + table > tbody > tr > th[scope=row] + td`.
  - Interactive states: Read-only semantic table. No decorative hover state. Keyboard and screen readers follow native table order.
- **Display Copy (Production-Ready):**
  - Header: `Tools I work with.`
  - Subhead / Body: `Grouped by the work they support, rather than as a flat keyword list.`
  - CTA / Action: `Review how the tools were applied in selected work`

#### [Section: Experience and Education]

- **Structural Blueprint:**
  - Grid & Alignment: Two-column timeline with dates in a 4-column left rail and role details in an 8-column right rail. Hairline row boundaries, no vertical motion or timeline animation.
  - Visuals & Art Direction: No headshot or decorative timeline art. Optional documentary image of an event crew at work: wide frame from the room's edge, candid coordination rather than posed lineup, available ambient light, natural olive/paper/ink hues. Use only if Rakesh has permission to publish it.
  - Styling Tokens: Olive mono date labels; serif role titles; sans descriptions; 1px ink-opacity row dividers.
- **Component Blueprint:**
  - Semantic tree: `section#experience > header + div.timeline > article.timeline-item > time/date + div(h3,org,p)`.
  - Interactive states: Static reading flow, no interactive timeline. Email and profile links remain native anchors elsewhere.
- **Display Copy (Production-Ready):**
  - Header: `Build, coordinate, deliver.`
  - Subhead / Body: `Software work sits alongside experience coordinating people, logistics, and delivery under live conditions.`
  - CTA / Action: `See project work`

#### [Section: Recognition]

- **Structural Blueprint:**
  - Grid & Alignment: Two-by-two rectangular cards on desktop, one column on small screens; cards share identical thin borders and generous padding. Keep evidence statements paired with their context.
  - Visuals & Art Direction: No trophy icons or fabricated award imagery. If actual certificates or event photos are supplied, photograph them as documentary records from a straight-on or slight overhead angle under soft window light, with identifying details kept intact and paper/ink/olive color treatment.
  - Styling Tokens: Paper base; ink serif card titles; olive mono category label; 1px borders in ink tint; no shadows or gradient surfaces.
- **Component Blueprint:**
  - Semantic tree: `section > header + div.achievements > article.achievement(label,h3,p)`.
  - Interactive states: Cards are static. Links to source material may be added only when a real publication or award URL is supplied.
- **Display Copy (Production-Ready):**
  - Header: `Results with context.`
  - Subhead / Body: `Hackathon outcomes, software experience, and team delivery, described with the work behind each result.`
  - CTA / Action: `Explore the work behind each result`

#### [Section: Contact]

- **Structural Blueprint:**
  - Grid & Alignment: 7/5 split. Editorial invitation and short body left; single email action and professional profiles in a compact bordered panel right.
  - Visuals & Art Direction: No stock portrait or contact illustration. If a portrait is later supplied, use a real environmental portrait at eye level with a 50mm lens, honest window light, quiet architectural background, natural paper/ink/olive palette.
  - Styling Tokens: Serif headline; sans supporting copy; olive email link and primary button; ink hairline panel; 150ms utility hover.
- **Component Blueprint:**
  - Semantic tree: `section#contact > div.contact > div(eyebrow,h2,p) + div.contact-card(email,mailto button,social links)`.
  - Interactive states: `mailto:` link opens the user's email client; LinkedIn and GitHub open safely in new tabs. Keyboard focus is visible. No embedded form or data capture.
- **Display Copy (Production-Ready):**
  - Header: `Let’s talk about the work.`
  - Subhead / Body: `For software engineering roles, project discussions, or a closer walkthrough of my work, email is the most direct way to reach me.`
  - CTA / Action: `Email Rakesh`

#### [Section: Footer]

- **Structural Blueprint:**
  - Grid & Alignment: Single hairline top border; copyright/location left and compact legal/social links right. Wrap without overflow on narrow screens.
  - Visuals & Art Direction: No footer image or logo strip. Any future location photo should be a real, high-contrast architectural detail from Navi Mumbai, shot at a low oblique angle with natural shadow and only paper/ink/olive values.
  - Styling Tokens: Small sans text, ink at reduced opacity, paper background, 1px hairline; links use olive on hover.
- **Component Blueprint:**
  - Semantic tree: `footer.site-footer > .wrap.footer-row > span + nav[aria-label] > a`.
  - Interactive states: Native links, visible focus. No platform credits, gamified keyboard easter eggs, or simulated status indicators.
- **Display Copy (Production-Ready):**
  - Header: `© 2026 Rakesh Bhakre · Navi Mumbai, India`
  - Subhead / Body: Legal pages and professional profiles.
  - CTA / Action: `Privacy policy` · `Terms of service` · `LinkedIn` · `GitHub`

#### [Section: Legal Stubs]

- **Structural Blueprint:**
  - Grid & Alignment: Dedicated narrow reading column with a serif page title, short effective/review date, clear section subheads, and a restrained olive review callout. Separate document routes at `/privacy-policy/` and `/terms-of-service/`.
  - Visuals & Art Direction: No decorative media on legal pages. Keep the reading surface quiet and high contrast; if an image is ever required, use no image rather than interrupt legal readability.
  - Styling Tokens: Paper `#F4F0EA`; ink `#1E1E1E`; olive `#505A3D`; body measure around 48rem; hairline border; same system serif/sans stacks as the portfolio.
- **Component Blueprint:**
  - Semantic tree: Each route has `header > main > h1 + article.content(semantic h2/p/list) + footer`; canonical link to its own URL and a return link to `/`.
  - Interactive states: Plain anchor navigation and visible keyboard focus. No forms, trackers, or third-party embeds in the delivered pages. The included legal copy is a starter requiring provider and jurisdiction review.
- **Display Copy (Production-Ready):**
  - Header: `Privacy policy` / `Terms of service`
  - Subhead / Body: `Last reviewed: 21 October 2026. Confirm hosting, data, and legal details before production publication.`
  - CTA / Action: `Return to portfolio` · `Email Rakesh`
