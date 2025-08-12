# Arc Cards
A local-first, high-quality flashcards app with Apple-like design, day/night modes, and spaced repetition.

## Vision
Master anything with a delightful, privacy-first study experience. Arc Cards focuses on:
- Beautiful, distraction-free UI with responsive, accessible components
- Fast, offline-first operation with instant interactions
- Smart spaced repetition that adapts to you
- Extensible architecture for sync, sharing, and advanced authoring

## Current Status
- Local decks and cards stored in the browser (localStorage)
- Clean UI with system theme + manual light/dark override
- Basic spaced repetition (Again / Good / Easy)
- Import/export deck JSON

## Roadmap (20 steps)
1. Product definition: README with vision, information architecture, design tokens, and roadmap
2. Design system: typography scale, color tokens, spacing, radius, shadow; reusable buttons, inputs, cards
3. Domain model: formalize deck, card, scheduler, and persistence interfaces; migrate state shape for forward-compatibility
4. SRS v2: implement SM-2 inspired algorithm with ease/interval adjustments, leech handling, and new-card learning steps
5. UX polish: keyboard shortcuts (J/K/Space/1-3), focus rings, animations, reduced motion support, ARIA roles
6. Search & tags: tags per card, quick filters, client-side full-text search (MiniSearch)
7. Editor v2: Markdown support for front/back, inline code, math (KaTeX), syntax highlighting, image attachments
8. Data layer: storage abstraction (localStorage -> IndexedDB), versioned migrations, export/import schemas
9. PWA: manifest, icons, service worker with offline caching and background sync stub
10. Backup: automated local backups with restore points; single-file JSON export with attachments
11. Deck sharing: signed export format, import confirmation UI, conflict resolution (merge/duplicate handling)
12. Theming: theme presets, custom color accents, per-deck accent color; motion system
13. Analytics (local-only): study streaks, time on task, heatmaps; opt-in only
14. Settings: preferences UI (theme, shortcuts, scheduling knobs, data management)
15. Internationalization: i18n scaffolding, English + one additional locale
16. Accessibility: screen reader flows for study, form labeling, contrast checks
17. Testing: add lightweight web-test-runner or Playwright when Node is available; snapshot and interaction tests
18. Deployment: GitHub Pages (docs/), project badges, Open Graph meta
19. Capture: simple bookmarklet to add cards from selected text; plan for browser extension
20. Cloud sync: optional account with Supabase/Firebase, auth, multi-device sync, end-to-end encryption planning

## Getting Started
- Open index.html in a modern browser
- Create decks on the left, add cards, and start studying
- Use the theme selector in the top bar to match system or force light/dark

## Usage
- Study: click the card to flip; choose Again / Good / Easy to schedule
- Import/Export: export the current deck as JSON and import deck files

## Architecture
- Single-file React (UMD) with local state and localStorage persistence
- Components: Sidebar (decks), TopBar (theme), StudyView (SRS), CardEditor, CardTable
- Styling: CSS variables for tokens, responsive layout, light/dark via data-theme or system

## Contributing
- Fork the repo, create a topic branch, and submit a PR
- When Node is available, we’ll adopt a proper toolchain (Vite + TypeScript) and tests

## License
MIT
