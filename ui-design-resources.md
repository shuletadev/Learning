# UI Design Resources

A running list of sites for pulling UI components, blocks, and animations/transitions into projects — plus inspiration galleries and MCP servers that give an AI agent direct, queryable access to real design references. Grouped by what each one actually gives you, since "component library," "inspiration gallery," and "MCP server" call for different workflows.

## Component & animation libraries (copy-paste code)

Most of these follow the "copy-paste source code" model popularized by shadcn/ui rather than shipping as opaque npm dependencies — the code lands in the project as editable source.

### shadcn/ui — [ui.shadcn.com](https://ui.shadcn.com)

- **What it is:** The foundational open-code component distribution platform for React. Not a traditional component library — it hands you the actual source, and several of the other sites here (beUI, RareUI, Canvas UI) install through its CLI/registry mechanism.
- **Stack:** React, Tailwind CSS, Radix UI primitives, TypeScript.
- **Install:** `npx shadcn add <component>` (CLI adds source files directly into your project) or copy-paste from the docs.
- **License:** Open source (MIT-style), free.
- **Contents:** Core primitives (buttons, dialogs, forms, tables, dropdowns, etc.), theming system, and a growing "blocks" section for larger page sections.
- **Why it matters:** Treat this as the base layer/design system — most of the sites below either extend it or distribute components compatible with its CLI.

### Beautiful UI — [beautifului.dev](https://www.beautifului.dev)

- **What it is:** A focused, small library (~17 patterns) of crafted, copy-paste components specifically for **AI-native product interfaces** — chat agents, thinking/streaming states, tool-call displays, approval cards, diffs.
- **Stack:** React, Tailwind CSS.
- **Install:** Copy-paste source per component (source included so it can be handed to a coding agent and adapted).
- **License:** MIT.
- **Use case:** Reach for this specifically when building AI/agent chat UIs — human-in-the-loop approval flows, streaming responses, tool-call visualizations.

### beUI — [beui.dev](https://beui.dev)

- **What it is:** A larger library (~108 components) of animated components split into motion primitives (buttons, modals, toasts, tabs, cards) and larger "blocks" (command palettes, dynamic islands, swap widgets).
- **Stack:** React, TypeScript, Tailwind CSS, Motion (Framer Motion).
- **Install:** Installs via the shadcn registry (`npx shadcn add` style, works with npm/pnpm/yarn/bun) or direct source copy.
- **License:** MIT, no tiers/watermarks/license traps — free for personal and commercial use.
- **Use case:** Good general-purpose source for polished, pre-animated interactive components beyond shadcn's base set.

### RareUI — [rareui.dev](https://rareui.dev) (also rareui.com)

- **What it is:** An open-source registry of "rare"/unusual animated React components — heavier on visual flair (liquid/glass/neumorphic/retro button styles, particle cards, WebGL liquid backgrounds, shader-based effects).
- **Stack:** React, Tailwind CSS, Motion (Framer Motion), Three.js/WebGL for the shader-heavy effects.
- **Install:** `npx rareui add <component-name>` (shadcn-CLI-compatible) or copy-paste.
- **License:** MIT, 100% free and open source.
- **Use case:** Pull from here for standout/hero visual moments (landing pages, marketing sections) rather than everyday app UI — effects are intentionally attention-grabbing.

### Canvas UI — [canvasui.dev](https://canvasui.dev)

- **What it is:** A library of creative "HTML-in-canvas" components — real, selectable/clickable HTML rendered inside a `<canvas>` element with WebGL shader effects (fire, fluid/liquid, glass refraction, cloth physics, glitch) running live over it, without screenshots or iframes.
- **Stack:** React, Vue, Svelte, Solid, Preact, or vanilla TS; WebGL under the hood. ~25 effects.
- **Install:** shadcn-CLI-compatible or direct copy-paste.
- **License:** Free, open source under **MIT + Commons Clause** (unlike the others here, Commons Clause blocks reselling the library itself as a hosted service/product — fine for using it inside a normal app or site).
- **Use case:** Reach for this when RareUI's Framer-Motion-based flair isn't enough and the effect genuinely needs GPU-driven distortion of real DOM content (e.g. a hero section where text/images visibly melt, ripple, or refract).

### Transitions.dev — [transitions.dev](https://transitions.dev)

- **What it is:** A curated collection of essential UI *transitions* (not full components) — modal toggles, dropdowns, panel/badge transitions, skeleton loaders, card resizes — each with a copy-ready snippet.
- **Stack:** Framework-agnostic CSS snippets, plus React/TypeScript variants.
- **Install:** Copy-paste per transition. Also ships as an agent skill (works with Claude Code, Cursor, GitHub Copilot, Codex, Gemini CLI) so a coding agent can pull the right transition into a project directly.
- **Content tiers:** Free tier covers common patterns (~27+ transitions); Pro tier adds more polished/complex ones (~36+, incl. modals/dropdowns/panels/badges).
- **License:** Free core library; Pro is paid.
- **Use case:** Reach for this when a component already exists but needs a specific enter/exit/state-change motion — complements the component libraries above rather than replacing them. Web-only (see 60fps below for the native-iOS equivalent).

## Inspiration & reference galleries (look, don't copy code)

These aren't component sources — they're curated screenshots/shots to study before designing or building something, useful for seeing how a specific pattern or overall aesthetic has actually been solved.

### CollectUI — [collectui.com](https://collectui.com)

- **What it is:** Daily-updated design inspiration curated from the Daily UI archive and Dribbble, organized by concrete UI pattern (checkout flow, onboarding, todo list, user profile, landing page, etc.).
- **Use case:** Pull this up when starting a specific, narrow UI pattern and want to see a range of ways designers have approached that exact screen before sketching your own.

### Recent.design — [recent.design](https://recent.design)

- **What it is:** A daily-curated showcase gallery of full websites, apps, and tools — broader/aesthetic-level inspiration rather than pattern-by-pattern breakdowns.
- **Use case:** Pull this up for overall visual direction/trend-spotting on a new project (typography, color, layout feel) rather than for a single component.

## MCP servers (agent-queryable design references)

Unlike the sites above, these aren't browsed manually — they're MCP connections an AI coding agent (Claude Code included) can query directly for real, production design/motion references. Both require going through their own setup/auth flow outside this doc.

### Mobbin MCP — [mobbin.com/mcp](https://mobbin.com/mcp)

- **What it is:** Official hosted MCP server (`https://api.mobbin.com/mcp`, Streamable HTTP) giving an AI agent natural-language search over Mobbin's library of 600,000+ real UI screens and 140,000+ flows captured from actual shipped mobile, web, and desktop apps (fintech, e-commerce, health, productivity, social, SaaS), hand-curated and updated weekly. Returns screen images inline in tool responses.
- **Setup:** Nothing to install/clone — add the endpoint to any MCP-compatible client; first use opens a browser to sign in and authorize via OAuth. No API key needed.
- **Use case:** Reach for this when you need to see how a specific real, shipped product solved a screen or flow (e.g. "show me onboarding flows for fintech apps") grounded in production examples, not curated concept shots.

### 60fps MCP — [60fps.design/mcp](https://60fps.design/mcp)

- **What it is:** MCP server (bundled with paid **60fps PRO**) giving an AI agent access to a library of 2,000+ real iOS interactions recorded from shipping apps, with full motion breakdowns (trigger → start → move → settle) and compile-checked SwiftUI motion code. Read-only.
- **Tools exposed:** `search_shots`, `get_shot`, `get_motion_breakdown`, `get_motion_code`.
- **Setup:** Requires a 60fps PRO license key, configured in the MCP-compatible client.
- **Use case:** The native-iOS analogue of Transitions.dev — reach for this when building SwiftUI motion/interactions and want a real reference implementation with actual working code, not a web CSS transition.

---

### Quick reference

| Site | Type | Best for | Install / access | License |
|---|---|---|---|---|
| ui.shadcn.com | Component library | Base design system / primitives | CLI (`shadcn add`) | Free |
| beautifului.dev | Component library | AI/agent chat UI patterns | Copy-paste | MIT |
| beui.dev | Component library | General animated components/blocks | shadcn-CLI-compatible or copy-paste | MIT |
| rareui.dev | Component library | Eye-catching visual/hero effects | `npx rareui add` or copy-paste | MIT |
| canvasui.dev | Component library | GPU/WebGL DOM-distortion effects | shadcn-CLI-compatible or copy-paste | MIT + Commons Clause |
| transitions.dev | Transition snippets | Web motion/transition snippets | Copy-paste or agent skill | Free (+Pro) |
| collectui.com | Inspiration gallery | Pattern-specific visual reference | Browse only | — |
| recent.design | Inspiration gallery | Overall aesthetic/trend inspiration | Browse only | — |
| mobbin.com/mcp | MCP server | Real shipped-app screens & flows | Hosted MCP, OAuth | Free (account) |
| 60fps.design/mcp | MCP server | Native iOS motion reference + SwiftUI code | Hosted MCP, license key | Paid (PRO) |
