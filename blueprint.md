# Swapnali Jadhav Portfolio

## Pre-launch structural checklist

1. **Domain and SSL setup**
   - Configure canonical `https://` origin and update `<link rel="canonical">` and `og:url` metadata in `index.html`, `privacy-policy/index.html`, and `terms-of-service/index.html` once the final domain is chosen.
   - Verify HTTPS certificate issuance and permanent HTTP → HTTPS redirects before enabling HSTS.

2. **Favicon and manifest**
   - Custom monochrome vector file: `./favicon.svg`, a geometric `SJ` monogram in heritage olive (`#505A3D`) on warm paper (`#F4F0EA`).
   - `./manifest.webmanifest` names Swapnali Jadhav's portfolio, uses `#F4F0EA` as theme/background color, and references `./favicon.svg`.

3. **Attribution-free static delivery**
   - Zero generator tags, vendor badges, third-party analytics trackers, or external runtime font dependencies.
   - Résumé PDF served directly from `./assets/Swapnali_Jadhav_Resume.pdf`.

4. **Legal routes**
   - Static legal stubs at `./privacy-policy/` (`privacy-policy/index.html`) and `./terms-of-service/` (`terms-of-service/index.html`), styled in the shared warm-paper / carbon-ink / heritage-olive palette.

## Design system

- **Base:** Warm paper `#F4F0EA` with subtle SVG fractal-noise grain.
- **Text:** Carbon ink `#1E1E1E` and opacity tints.
- **Accent:** Heritage olive `#505A3D` and opacity tints.
- **Typography:** Editorial serif display (`Newsreader` / Georgia stack), clean interface sans (`Inter` / system sans), and monospace indices (`SFMono-Regular` / Consolas).
- **Interactive engineering elements:**
  1. **Hero AEGIS Fault-Flow Map:** Selectable 4-stage SVG architecture trace (`01 Detect`, `02 Explain`, `03 Recommend`, `04 Safety`) with progressive path highlighting, node click & keyboard arrow-key support, and stage specification readouts.
  2. **Expandable System Architecture & Benchmark Drawers:** Inline hairline drawers on the featured projects — including an interactive 3-episode spacecraft fault-injection simulation walkthrough for **AEGIS** (`29/40` overall episodes, `5/5` reaction-wheel friction), a 4-module breakdown for **Air-Hand Gesture Recognition**, and a 3-stage biosignal ML pipeline for **Plant Whisper**.
  3. **Skill-to-Project Traceability Table:** Interactive semantic specification table (`03 / Technical specifications`) that cross-references each tool category directly to the projects, internships, and coursework where it was applied.
  4. **Accessibility & Reduced Motion:** Full keyboard support, ARIA live regions, static tabular proof figures, and `prefers-reduced-motion` compliance.
