# Casa Limone — Vanilla Static Site Re-Architecture

## 1. Project Overview
Refactor the MVP landing page (`mvp/*`) into a maintainable, component-driven static architecture using vanilla web standards. The project emphasizes modularity, zero external dependencies, and simplicity with no build step required.

---

## 2. Core Principles & Stack
- **Languages**: HTML5, CSS3, Vanilla ES6+ JavaScript.
- **Frameworks / Libraries**: None (0 external dependencies, no bundlers, no npm build process).
- **Architecture**: Native Web Components (`HTMLElement`, `customElements.define`, ES Modules).
- **Data Management**: External JSON files for localized content and dynamic section data (`data/`).
- **Build Step**: None. Runs directly in any static file server or modern browser.
- **Hosting Target**: GitHub Pages.

---

## 3. Architecture & Directory Structure

```text
├── index.html              # Main static entry point
├── styles/
│   ├── tokens.css          # Design tokens (colors, typography, spacing from classical design system)
│   └── main.css            # Base, layout & utility styles
├── data/
│   └── i18n/
│       └── en.json         # Content strings, section data, and metadata
├── components/             # Reusable Native Web Components
│   ├── app-nav.js          # Navigation bar
│   ├── hero-section.js     # Hero banner
│   ├── feature-card.js     # Reusable cards / items
│   ├── photo-plate.js      # Image mats & gallery plates
│   └── app-footer.js       # Footer
└── assets/                 # Brand assets, images, icons
```

---

## 4. Key Requirements & Features

1. **Component Modularity (React-like without a framework)**:
   - Native browser Web Components (`customElements.define`) for clean encapsulation, reusability, and modularity.
   - Declarative usage in markup with attribute and property bindings.
2. **Data-Driven Architecture**:
   - Decouple text copy and dynamic data from HTML into clean JSON files.
   - Easy maintenance and straightforward internationalization (i18n).
3. **Design System Adherence**:
   - Follow the editorial, classical aesthetic established in `mvp/classical-0ded8838-9ef2-4568-8ba6-df4b571712a2/` (Cormorant Garamond + Lora, hairline borders, muted palettes, no solid heavy fills).
4. **GitHub Pages Deployment**:
   - Native relative asset resolution (`./assets/...`) ensuring immediate compatibility with GitHub Pages custom domains and repository sub-paths.

---

## 5. Implementation Roadmap

- [ ] **Phase 1: Foundation & Design Tokens**
  - Extract design tokens, typography, and core CSS from `mvp/classical-...` into `styles/tokens.css` and `styles/main.css`.
- [ ] **Phase 2: Data Schema & Extraction**
  - Organize and centralize copy/assets into structured JSON (`data/i18n/en.json`).
- [ ] **Phase 3: Component Development**
  - Build native Web Components (`components/`) for each section of the landing page.
- [ ] **Phase 4: Site Assembly & Verification**
  - Assemble the clean `index.html` shell and test dynamic data binding and responsive layout.
- [ ] **Phase 5: GitHub Pages Readiness**
  - Verify relative paths, ensure zero-build execution, and document deployment steps.