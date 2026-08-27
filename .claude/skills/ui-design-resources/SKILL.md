---
name: ui-design-resources
description: Curated quick-reference catalog of UI/frontend design resources — component libraries (shadcn/ui, Beautiful UI, beUI, RareUI, Canvas UI), transition snippets (Transitions.dev), inspiration galleries (CollectUI, Recent.design), and MCP servers for real design/motion references (Mobbin MCP, 60fps MCP). Use whenever the user is doing UI/frontend design work and wants component ideas, a design-system starting point, animation/transition effects, visual inspiration for a screen or pattern, or a real-world reference for how shipped apps solved something — e.g. "what UI library should I use", "where can I find components for X", "I need a chat UI pattern", "I need a fancy hero animation", "show me onboarding flow examples", or building a React/Next.js/SwiftUI interface needing off-the-shelf pieces or references — even without naming a site. Also use if the user names any of these sites/domains directly.
---

# UI Design Resources

A curated shortlist of sites for pulling UI components, blocks, animations/transitions, and design inspiration into projects, so this doesn't need to be re-researched from scratch each time it comes up. Grouped by what each one actually gives you — "component library," "inspiration gallery," and "MCP server" call for different workflows.

Reach for this list whenever a task calls for existing UI pieces or references rather than building purely from imagination: picking a component library for a new app, finding a specific interaction pattern (chat UI, hero section, dropdown, onboarding flow), adding motion to something that already exists, or wanting to see how a real shipped product solved a screen before designing one.

## Component & animation libraries (copy-paste code)

Most follow the "copy-paste source code" model popularized by shadcn/ui rather than shipping as opaque npm dependencies — the code lands directly in the project as editable source.

### shadcn/ui — [ui.shadcn.com](https://ui.shadcn.com)
The foundational layer. Not a typical component library — it hands you the actual source code rather than an installed dependency, and several of the other sites below install *through* its CLI/registry mechanism. Start here for the base design system.
- **Stack:** React, Tailwind CSS, Radix UI primitives, TypeScript.
- **Install:** `npx shadcn add <component>`, or copy-paste from the docs.
- **License:** Free, open source.
- **Reach for it when:** starting a new project's design system, or needing a solid accessible primitive (dialog, combobox, form field) before reaching for anything fancier.

### Beautiful UI — [beautifului.dev](https://www.beautifului.dev)
A small, focused library (~17 patterns) purpose-built for **AI-native product interfaces** — chat agents, thinking/streaming states, tool-call displays, approval cards, diffs.
- **Stack:** React, Tailwind CSS. **Install:** Copy-paste source per component. **License:** MIT.
- **Reach for it when:** building a chat UI, agent tool-call visualization, human-in-the-loop approval flow, or any AI/LLM product surface.

### beUI — [beui.dev](https://beui.dev)
A larger library (~108 components) of animated pieces, split into motion primitives (buttons, modals, toasts, tabs, cards) and larger assembled blocks (command palettes, dynamic islands, swap widgets).
- **Stack:** React, TypeScript, Tailwind CSS, Motion (Framer Motion). **Install:** shadcn-registry-compatible or direct source copy. **License:** MIT, no watermarks or tiers.
- **Reach for it when:** the base shadcn set feels too plain and something needs polished built-in motion without hand-rolling the animation.

### RareUI — [rareui.dev](https://rareui.dev) (also rareui.com)
A registry of unusual, attention-grabbing animated components — liquid/glass/neumorphic/retro button styles, particle cards, WebGL liquid backgrounds, shader-based effects.
- **Stack:** React, Tailwind CSS, Motion, Three.js/WebGL for the shader-heavy pieces. **Install:** `npx rareui add <component-name>` or copy-paste. **License:** MIT, 100% free.
- **Reach for it when:** a landing page or marketing section needs a standout hero moment. Not the right source for everyday app UI — these are deliberately loud.

### Canvas UI — [canvasui.dev](https://canvasui.dev)
"HTML-in-canvas" components — real, selectable/clickable HTML rendered inside `<canvas>` with WebGL shader effects (fire, fluid, glass refraction, cloth physics, glitch) running live over it.
- **Stack:** React, Vue, Svelte, Solid, Preact, or vanilla TS; WebGL under the hood (~25 effects). **Install:** shadcn-CLI-compatible or copy-paste. **License:** MIT + Commons Clause (blocks reselling the library itself as a service; fine for use inside a normal app).
- **Reach for it when:** RareUI's flair isn't enough and the effect genuinely needs GPU-driven distortion of real DOM content (text/images that visibly melt, ripple, or refract).

### Transitions.dev — [transitions.dev](https://transitions.dev)
Not components — just the essential web **transitions**: modal toggles, dropdown/panel/badge transitions, skeleton loaders, card resizes. Each ships a copy-ready snippet.
- **Stack:** Framework-agnostic CSS snippets, plus React/TypeScript variants. **Install:** Copy-paste, or via its own agent skill (works with Claude Code, Cursor, Copilot, Codex, Gemini CLI). **License:** Free tier (~27+ transitions); Pro tier paid (~36+).
- **Reach for it when:** a component already exists but its enter/exit/state-change motion feels abrupt or missing. Web-only — see 60fps MCP below for the native-iOS equivalent.

## Inspiration & reference galleries (look, don't copy code)

Not component sources — curated screenshots to study before designing or building something.

### CollectUI — [collectui.com](https://collectui.com)
Daily-updated inspiration curated from the Daily UI archive and Dribbble, organized by concrete UI pattern (checkout flow, onboarding, todo list, user profile, landing page, etc.).
- **Reach for it when:** starting a specific, narrow UI pattern and wanting to see a range of ways designers have approached that exact screen before sketching one.

### Recent.design — [recent.design](https://recent.design)
A daily-curated showcase gallery of full websites, apps, and tools — broader/aesthetic-level inspiration rather than pattern-by-pattern breakdowns.
- **Reach for it when:** wanting overall visual direction/trend-spotting for a new project (typography, color, layout feel) rather than a single component.

## MCP servers (agent-queryable design references)

Unlike the sites above, these aren't browsed manually — they're MCP connections an AI coding agent can query directly for real, production design/motion references. Each requires its own setup/auth outside this catalog (OAuth sign-in or a license key), so surface them as an option to connect rather than assuming they're already wired up.

### Mobbin MCP — [mobbin.com/mcp](https://mobbin.com/mcp)
Official hosted MCP server (`https://api.mobbin.com/mcp`) giving natural-language search over 600,000+ real UI screens and 140,000+ flows captured from actual shipped mobile/web/desktop apps (fintech, e-commerce, health, productivity, social, SaaS), updated weekly. Returns screen images inline.
- **Setup:** No install — add the endpoint to any MCP client; first use opens a browser for OAuth sign-in. No API key.
- **Reach for it when:** wanting to see how a specific real, shipped product solved a screen or flow (e.g. "onboarding flows for fintech apps"), grounded in production examples rather than curated concept shots.

### 60fps MCP — [60fps.design/mcp](https://60fps.design/mcp)
MCP server (bundled with paid 60fps PRO) exposing a library of 2,000+ real iOS interactions recorded from shipping apps, with motion breakdowns (trigger → start → move → settle) and compile-checked SwiftUI motion code. Read-only.
- **Tools:** `search_shots`, `get_shot`, `get_motion_breakdown`, `get_motion_code`. **Setup:** Requires a 60fps PRO license key in the MCP client config.
- **Reach for it when:** building SwiftUI motion/interactions and wanting a real reference implementation with actual working code — the native-iOS analogue of Transitions.dev.

## Quick-reference table

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

## How to use this when helping with UI work

1. Identify what's actually needed: a base primitive (→ shadcn), a fuller animated component (→ beUI), a loud visual/hero moment (→ RareUI or Canvas UI), an AI/chat-specific pattern (→ Beautiful UI), just motion for something that exists (→ Transitions.dev for web, 60fps MCP for native iOS), or a look at how it's been solved before starting (→ CollectUI for a pattern, Recent.design for overall direction, Mobbin MCP for real shipped examples).
2. Default to shadcn/ui as the foundation unless the project already has a different system in place — most of the component libraries here are designed to sit on top of it or install compatibly with its CLI.
3. Prefer copy-paste/CLI-installed source over adding a new opaque dependency, in keeping with how these libraries distribute their code — it keeps the component fully editable in the project.
4. Note licensing/cost before recommending: most of these are free/MIT, except Canvas UI (MIT + Commons Clause — fine for normal use, not for reselling the library itself), Transitions.dev Pro (paid tier), and 60fps MCP (requires a paid PRO license).
5. For the two MCP servers, don't assume they're connected — mention that connecting requires the user's own auth (Mobbin: OAuth sign-in) or license key (60fps PRO) in their MCP client.
