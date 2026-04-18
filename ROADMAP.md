# Agentic Web Design Roadmap

**Baseline**: Total beginner (no HTML/CSS/JS).
**Cadence**: 20+ hrs/week.
**Target**: Freelance/client work.
**Estimated total**: ~5 months.

Stack throughout: Claude Code + Vite + React 19 + Tailwind v4 + shadcn/ui.

---

## Stage 1: Get Hands Dirty

**Goal**: Get comfortable operating Claude Code. Generate, run, break, observe.

**Why this stage matters**: Skill #1 in agentic web design is fast iteration with an agent. You need muscle memory before you have good judgment. No fundamentals prerequisite — you learn by doing and asking Claude Code to explain what it builds.

**Deliverables**:
- Claude Code running locally with a Vite + React + Tailwind scaffold
- 5 single-page throwaway sites prompted end-to-end (landing page, pricing page, blog, dashboard mockup, portfolio)
- A running `notes.md`: what you prompted, what came back, what surprised you

**Practice mechanics**: Each session — pick a site type, prompt it cold, read every file Claude Code generates, delete anything you don't understand, re-prompt until you can read the whole thing. Ask Claude Code to explain any line you can't parse.

**Feedback mechanism**: Output runs or it doesn't. Page looks right or it doesn't. You understand the generated code or you don't — honest self-check.

**Checkpoint**: You can scaffold a new React + Tailwind page from a one-line prompt, preview it in the browser, and explain what every file does — without pausing.

**Estimated time**: 2 weeks (40+ hrs).

**Plateau indicators**: You're generating pretty pages but can't explain them. You're copying prompts from others instead of writing your own. You haven't broken anything yet.

---

## Stage 2: Develop Critique Skills

**Goal**: Learn to judge whether Claude Code's output is good, bad, outdated, or insecure — before running it.

**Why this stage matters**: An agentic web designer's highest-leverage skill is reading code critically. If you can't critique, you're rolling dice. This stage is where you absorb HTML/CSS/JS fundamentals — not through courses, but through deliberate study of output you directed.

**Deliverables**:
- A `critique-log.md` with 30+ critiqued outputs: prompt → what came back → what was wrong → fixed version
- A personal red-flag list: patterns you now refuse (useEffect for data fetching, manual useMemo, dangerouslySetInnerHTML, class components, etc.)
- A working mental model of the CSS box model, Flexbox, Grid, and the Tailwind utilities that map to each

**Practice mechanics**: For every prompt — before running the output — write down 3 things you'd change and why. Then run it and see if you were right. Ask Claude Code to critique its own output adversarially ("what's wrong with this?").

**Feedback mechanism**: Self-critique vs. what actually breaks. Claude Code's adversarial review. Your red-flag list growing over time.

**Checkpoint**: Given a React component Claude Code outputs, you can name 3 specific issues (performance, accessibility, modern patterns) before running it — and be right at least twice.

**Estimated time**: 3 weeks.

**Plateau indicators**: Your critiques stay vague ("this could be better"). You defer to the agent on every technical choice. You can't distinguish outdated React patterns from current ones.

---

## Stage 3: Build in Components

**Goal**: Direct Claude Code to build component by component, not page by page. Own the architecture.

**Why this stage matters**: Junior agentic work = "build me a page." Senior agentic work = "build me a `<PricingCard variant='featured' />` that fits this design system." Clients pay for the latter.

**Deliverables**:
- One personal design system repo with ~20 components (Button, Input, Card, Badge, Modal, Toast, Dropdown, DataTable, Skeleton, etc.) via shadcn/ui + Tailwind v4
- 3 landing pages built by composing only your own components — no page-level prompts
- Each component rendered in isolation (Storybook or a simple `/kitchen-sink` route)

**Practice mechanics**: Start every session by sketching the component tree on paper or in a comment. Prompt component by component. Refuse to let Claude Code build at the page level until you have the components it would need.

**Feedback mechanism**: Components compose cleanly or they don't. The kitchen sink route reveals broken states and visual inconsistencies. Landing pages built from your components reveal gaps.

**Checkpoint**: You can build a new landing page in under 2 hours using only components you already own — zero page-level generation.

**Estimated time**: 3 weeks.

**Plateau indicators**: Components all look slightly different (no design system discipline). You reach for page-level prompts under pressure. Kitchen sink is empty or stale.

---

## Stage 4: Add Interactivity

**Goal**: Ship products that do things — forms, state, server actions, optimistic UI, error states.

**Why this stage matters**: Static pages are table stakes for client work. The things clients actually need are interactions: sign-up flows, dashboards, filters, multi-step forms. This stage makes you hireable.

**Deliverables**:
- A working CRUD app (task manager or invoice tracker) using React 19 Actions + `useOptimistic`
- A multi-step form with validation, loading states, and error states for every field
- A dashboard with filters, pagination, and data fetching via TanStack Query

**Practice mechanics**: For every interactive feature, enumerate every state (idle, loading, error, success, empty, disabled) before prompting. Make Claude Code handle all of them. No shipping until the unhappy paths work.

**Feedback mechanism**: Does clicking work? Does it break when the network is slow or the API fails? Does it work via keyboard alone? Test all three before marking anything done.

**Checkpoint**: You can scope and ship a 3-screen interactive flow (e.g., a signup wizard with validation) end-to-end in a single day.

**Estimated time**: 3 weeks.

**Plateau indicators**: Loading spinners everywhere, no optimistic updates. Forms break on unexpected input. Everything works locally, nothing works when deployed.

---

## Stage 5: Clone Something Real

**Goal**: Reproduce a high-polish production site pixel-for-pixel and interaction-for-interaction.

**Why this stage matters**: Clients judge quality visually. Cloning forces you to notice the details that separate amateur from professional — spacing rhythms, typography scale, micro-animations, hover states. You can't fake attention to detail; you have to train it.

**Deliverables**:
- 2 full clones deployed on Vercel or Netlify (good targets: Linear landing page, Stripe docs, Vercel dashboard, Loom marketing site, Notion homepage)
- Each clone has a short README explaining what was hardest and what you had to fix

**Practice mechanics**: Open the real site side-by-side with your clone at all times. Measure spacing with browser devtools. Every difference you spot is an issue you log and fix. Don't move on until you can't spot the diff at a glance.

**Feedback mechanism**: Superimpose screenshots. Ask Claude Code to review the diff. Show someone who hasn't seen your work and note the first thing they notice.

**Checkpoint**: Your clone is indistinguishable from the source at a glance. You can name the subtle differences that remain.

**Estimated time**: 3 weeks.

**Plateau indicators**: "Close enough" is good enough for you. You're skipping the interactions and only doing the static layout. You can't spot your own errors.

---

## Stage 6: Build for Real Problem

**Goal**: Ship one paid client project end-to-end — brief → design → build → deploy → handoff.

**Why this stage matters**: The whole roadmap exists to make you effective at client work. A portfolio piece is not the same as a paying client. Paid work reveals what you didn't know you didn't know: scope creep, unclear briefs, revision cycles, handoff format, invoicing. One real project teaches more than five fake ones.

**Deliverables**:
- One paid project (even $200 counts — the number is less important than the process)
- A portfolio site with 3+ case studies (your two Stage 5 clones count; frame them as "here's how I work")
- A documented personal workflow: your prompting process, review checklist, quality bar, and handoff format
- An invoice you sent and got paid on

**Practice mechanics**: Start looking for a client during Stage 5, not after. Cold outreach to small businesses, Upwork, friends-of-friends, local service businesses with bad websites. Treat the brief like a spec. When you hit a wall, prompt — don't Google. Document what breaks the workflow so you can improve it.

**Feedback mechanism**: The client is the feedback. Did they pay without dispute? Did they request revisions you hadn't anticipated? Would they refer you? These are the real checkpoints.

**Checkpoint**: Project is signed off, deployed, and paid for.

**Estimated time**: 4–6 weeks.

**Plateau indicators**: You keep "preparing" instead of pitching. Scope creep eats weeks without pushback. You deliver something you'd be embarrassed to show a stranger.

---

## Opinionated choices — read and push back if you disagree

**1. No JS/CSS courses before Stage 1.**
Every credible educator says fundamentals matter and you need them before React. I've deliberately ignored that advice here. You'll absorb HTML/CSS/JS through reading and critiquing agent output in Stages 1–2, with Claude Code as your tutor. This is faster and more aligned with your actual goal. The risk: if you hit a wall in Stage 2 where critique doesn't click, we add a focused 2-week sprint on JS fundamentals before continuing. Watch for it.

**2. Vite + React 19 + Tailwind v4 + shadcn/ui. No Next.js until after Stage 6, if then.**
All research agrees this is the right 2026 beginner stack. Next.js adds server/client complexity that muddies the feedback loop too early. If your client work ends up requiring SSR, we'll add it then. Not before.

**3. Stage 6 is a real paid project, not a capstone.**
For a freelance goal, the only honest graduation test is a client who paid money. This means hustling for a first client during Stage 5, not after the roadmap is "complete." If this feels premature, it's supposed to. The whole point of Stages 1–5 is to get you ready faster than the traditional path assumes.
