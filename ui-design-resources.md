# UI Design Resources

A running list of sites for pulling UI components, blocks, and animations/transitions into projects. Most of these follow the "copy-paste source code" model popularized by shadcn/ui rather than shipping as opaque npm dependencies.

## shadcn/ui — [ui.shadcn.com](https://ui.shadcn.com)

- **What it is:** The foundational open-code component distribution platform for React. Not a traditional component library — it hands you the actual source, and many of the other sites below (beUI, RareUI) install through its CLI/registry mechanism.
- **Stack:** React, Tailwind CSS, Radix UI primitives, TypeScript.
- **Install:** `npx shadcn add <component>` (CLI adds source files directly into your project) or copy-paste from the docs.
- **License:** Open source (MIT-style), free.
- **Contents:** Core primitives (buttons, dialogs, forms, tables, dropdowns, etc.), theming system, and a growing "blocks" section for larger page sections.
- **Why it matters:** Treat this as the base layer/design system — most of the sites below either extend it or distribute components compatible with its CLI.

## Beautiful UI — [beautifului.dev](https://www.beautifului.dev)

- **What it is:** A focused, small library (~17 patterns) of crafted, copy-paste components specifically for **AI-native product interfaces** — chat agents, thinking/streaming states, tool-call displays, approval cards, diffs.
- **Stack:** React, Tailwind CSS.
- **Install:** Copy-paste source per component (source included so it can be handed to a coding agent and adapted).
- **License:** MIT.
- **Use case:** Reach for this specifically when building AI/agent chat UIs — human-in-the-loop approval flows, streaming responses, tool-call visualizations.

## beUI — [beui.dev](https://beui.dev)

- **What it is:** A larger library (~108 components) of animated components split into motion primitives (buttons, modals, toasts, tabs, cards) and larger "blocks" (command palettes, dynamic islands, swap widgets).
- **Stack:** React, TypeScript, Tailwind CSS, Motion (Framer Motion).
- **Install:** Installs via the shadcn registry (`npx shadcn add` style, works with npm/pnpm/yarn/bun) or direct source copy.
- **License:** MIT, no tiers/watermarks/license traps — free for personal and commercial use.
- **Use case:** Good general-purpose source for polished, pre-animated interactive components beyond shadcn's base set.

## RareUI — [rareui.dev](https://rareui.dev) (also rareui.com)

- **What it is:** An open-source registry of "rare"/unusual animated React components — heavier on visual flair (liquid/glass/neumorphic/retro button styles, particle cards, WebGL liquid backgrounds, shader-based effects).
- **Stack:** React, Tailwind CSS, Motion (Framer Motion), Three.js/WebGL for the shader-heavy effects.
- **Install:** `npx rareui add <component-name>` (shadcn-CLI-compatible) or copy-paste.
- **License:** MIT, 100% free and open source.
- **Use case:** Pull from here for standout/hero visual moments (landing pages, marketing sections) rather than everyday app UI — effects are intentionally attention-grabbing.

## Transitions.dev — [transitions.dev](https://transitions.dev)

- **What it is:** A curated collection of essential UI *transitions* (not full components) — modal toggles, dropdowns, panel/badge transitions, skeleton loaders, card resizes — each with a copy-ready snippet.
- **Stack:** Framework-agnostic CSS snippets, plus React/TypeScript variants.
- **Install:** Copy-paste per transition. Also ships as an agent skill (works with Claude Code, Cursor, GitHub Copilot, Codex, Gemini CLI) so a coding agent can pull the right transition into a project directly.
- **Content tiers:** Free tier covers common patterns (~27+ transitions); Pro tier adds more polished/complex ones (~36+, incl. modals/dropdowns/panels/badges).
- **License:** Free core library; Pro is paid.
- **Use case:** Reach for this when a component already exists but needs a specific enter/exit/state-change motion — complements the component libraries above rather than replacing them.

---

### Quick reference

| Site | Best for | Install method | License |
|---|---|---|---|
| ui.shadcn.com | Base design system / primitives | CLI (`shadcn add`) | Free |
| beautifului.dev | AI/agent chat UI patterns | Copy-paste | MIT |
| beui.dev | General animated components/blocks | shadcn-CLI-compatible or copy-paste | MIT |
| rareui.dev | Eye-catching visual/hero effects | `npx rareui add` or copy-paste | MIT |
| transitions.dev | Motion/transition snippets | Copy-paste or agent skill | Free (+Pro) |
