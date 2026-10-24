# Guidelines for mock.html

This document tracks all strict rules, constraints, and instructions followed while making edits to `mock.html`.

## 1. Tone and Language
- **Strictly professional, objective, and academic.**
- No hyperbolic marketing language is allowed. All text should rely on engineering facts and objective validation.

## 2. Structural Constraints
- **Preserve Site Chrome:** Do NOT alter the `<head>`, `<nav>`, CSS styles, or `<footer>`.
- **Maintain Design System:** Do NOT change the global color scheme, typography, or layout logic.
- **Class Usage:** Only use existing CSS classes (e.g., `.section`, `.section-label`, `.how-grid`, `.how-card`, `.ability-grid`, `.econ-grid`, `.terminal-block`).

## 3. Data Independence and Placeholders
- **Benchmark Independence:** Any newly injected text/framework must be independent of specific benchmark results (like token counts or accuracy drops specific to a single run) unless explicitly instructed.
- **Blank Spaces:** If content must be added that depends on variable benchmark results, the spaces containing those variable numbers (such as token counts or percentage drops) must be left blank (e.g. `[ ]`) so they can be filled dynamically or separately.

## 4. Execution
- Ensure all HTML output is complete and ready for deployment without corrupting any preexisting non-targeted sections.

## 5. Documentation Pages & Design System Standards
- **Pixel-Perfect Figma Parity:**
  - All documentation pages (`platform.html`, `opensource.html`, `agent_plugins.html`, `integrations.html`, `release_notes.html`) must strictly preserve the modern design system shown in the Figma screenshots.
  - Header: Negentro logo (SVG layer mark), navigation links with active purple underline indicator, `⌘K` search button, light/dark theme toggle (`toggleTheme()`), GitHub repository link, and purple "Dashboard" CTA button.
  - Sidebar: Categorized groups (all-caps gray headers), rounded pill links, and active state with soft purple pill background and left-accent bar.
  - Right Sidebar (TOC): "On this page" sticky navigation that highlights the active section dynamically on scroll.
  - Interactive Filter Tabs & Search: Directory and timeline views must include working category filter pills and live real-time search inputs filtering items instantly.
  - Footer & Navigation: Split previous/next navigation card, action buttons (`Suggest edits`, `Raise issue`), and global bottom footer with social/docs links.

- **Content Grounding from Source Files:**
  - All documentation text, architecture details, and code examples must strictly be drawn from `userguide.pdf` and the corresponding `docs/docs_<section>.md` files:
    - Platform: `docs/docs_platform.md`
    - Open Source: `docs/docs_opensource.md`
    - Agent Plugins: `docs/docs_agentplugins.md`
    - Integrations: `docs/docs_integrations.md` (and `docs/docs_integration.md`)
    - Cookbooks: `docs/docs_cookbooks.md`
    - API Reference: `docs/docs_apireference.md`
    - Release Notes: `docs/docs_releasenotes.md`
  - Product naming and architecture: Reflect Negentro / PiAPI (PiyAPI) capabilities (bitemporal graph memory, UnifiedScorer, MCP server, CDC connectors, BYOK key manager, Redis semantic caching, PostgreSQL + pgvector).

- **The Red Indicator Rule (Missing Documentation Protocol):**
  - If any option, framework, agent, tool, SDK, or integration in the sidebar or directory grid lacks sufficient/relevant setup data in `userguide.pdf` or `docs_<section>.md`:
    1. **DO NOT invent or hallucinate content.**
    2. Style that option/button in **RED** (`color: #ef4444;`, with a red badge `[No docs]`).
    3. In that section's view, display an explicit red warning banner indicating that content is pending from the user or awaiting future Figma design frames.
    4. This immediately communicates to the user that the system is aware of the integration, but authoritative documentation is not yet available.

- **Universal Topbar Cross-Linking:**
  - Every page must contain functioning topbar links between all existing documentation sections:
    - `Platform` &rarr; `platform.html`
    - `Open Source` &rarr; `opensource.html`
    - `Agent Plugins` &rarr; `agent_plugins.html`
    - `Integrations` &rarr; `integrations.html`
    - `Cookbooks` &rarr; `cookbooks.html`
    - `API Reference` &rarr; `api_reference.html`
    - `Release Notes` &rarr; `release_notes.html`

- **File Cleanliness:**
  - Never create redundant duplicate files (such as `*_copy.html`). Update the designated primary HTML file directly.

