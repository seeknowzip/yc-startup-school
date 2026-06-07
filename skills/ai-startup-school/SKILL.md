---
name: ai-startup-school
description: |
  This skill should be used when the user mentions "AI Native Company", "AI-native company", "AI 스타트업", "AI startup school", "AI 트렌드", "소프트웨어 3.0", "/yc-ai", "AI 창업", "AI 산업 트렌드", "AI 빌더", "agentic company", "self-improving company", "company brain", "skillify", "resolver", "Garry Tan", "Diana Hu", "Karpathy", "Sam Altman", "AGI", "vibe coding", or asks about insights from top AI leaders. Synthesizes knowledge from 17 AI Startup School / AI Native Company transcripts — including Karpathy, Altman, Musk, Nadella, Garry Tan, Diana Hu, Fei-Fei Li, Chollet, Ng, Srinivas, Jumper, Finn, Kaplan, Field, Truell, Masad, and the founder panel — and applies them to the user's current AI work, startup design, or company operating model.
---

# AI Native Company / AI Startup School — Synthesized Insights from the Top Minds

Read all 17 AI Startup School / AI Native Company transcripts and synthesize the key cross-cutting insights from the world's top AI leaders. Apply these insights to the user's current AI-related work, startup strategy, product decisions, or operating-system design.

The default frame is now **AI Native Company**, not merely “AI features for startups.” Treat AI as a new company architecture: company context becomes legible, skills/resolvers/memory/evals become operating primitives, and functions are redesigned as recursive self-improving loops.

## Transcript Files

All transcripts are located at `${CLAUDE_PLUGIN_ROOT}/skills/ai-startup-school/references/`:

1. `andrej-karpathy-software-is-changing-again.md` — Software 3.0, LLMs as new compute layer
2. `andrew-ng-building-faster-with-ai.md` — AI-augmented workflows, iteration speed
3. `aravind-srinivas-the-race-to-build-the-ai-browser-of-the-future.md` — AI-native products, Perplexity story
4. `chelsea-finn-building-robots-that-can-do-anything.md` — Robotics, generalist AI agents
5. `elon-musk-digital-superintelligence-multiplanetary-life-how-to-be-useful.md` — First principles, civilizational scale
6. `every-ai-founder-should-be-asking-these-questions.md` — Panel: founder mindset, key questions
7. `fei-fei-li-spatial-intelligence-is-the-next-frontier-in-ai.md` — Spatial intelligence, embodied AI
8. `figma-ceo-dylan-field-how-ai-will-transform-design.md` — AI-native product design, incumbents vs. startups
9. `franois-chollet-the-arc-prize-how-we-get-to-agi.md` — ARC Prize, measuring true intelligence, AGI paths
10. `john-jumper-alphafold-and-the-future-of-science.md` — AI for science, AlphaFold, deep tech
11. `michael-truell-building-cursor-at-23-taking-on-github-copilot-and-advice-to-engi.md` — Vibe coding, Cursor story, AI-native dev tools
12. `sam-altman-the-future-of-openai-chatgpts-origins-and-building-ai-hardware.md` — OpenAI roadmap, AI hardware, AGI timeline
13. `satya-nadella-microsofts-ai-bets-hyperscaling-quantum-computing-breakthroughs.md` — Hyperscaling, enterprise AI, infra bets
14. `scaling-and-the-road-to-human-level-ai-anthropic-co-founder-jared-kaplan.md` — Scaling laws, human-level AI roadmap
15. `the-future-of-software-creation-with-replit-ceo-amjad-masad.md` — No-code/low-code future, AI-native creation
16. `how-to-build-a-self-improving-company-with-ai.md` — YC's AI Native Company frame: company brain, legibility, recursive self-improving loops
17. `the-ai-native-company-how-one-founder-becomes-a-1000x-engineer.md` — Garry Tan + Diana Hu: skills, resolvers, memory, evals, closed-loop agentic organization

## Instructions

### Step 1: Read All Transcripts

Read ALL 17 transcript files from `${CLAUDE_PLUGIN_ROOT}/skills/ai-startup-school/references/` before generating any response. Cross-transcript synthesis is the core value of this skill — do not skip files.

If the user specifically asks about “AI Native Company,” prioritize transcripts 16-17 first, then connect them back to Karpathy, Ng, Truell, Masad, Srinivas, Field, and the founder panel.

### Step 2: Understand the User's Context

Before synthesizing, understand what the user is working on:
- Are they building an AI product? Which stage?
- Are they designing a company operating system, not just a product feature?
- Which company functions need to become legible to AI: customer support, sales, product analytics, engineering, recruiting, events, partner ops, knowledge, finance, or founder workflow?
- Are they evaluating a technology bet (infra, model, agent, memory, eval, tool layer, etc.)?
- Are they thinking about positioning, competition, timing, org design, or revenue per employee?
- Are they looking for inspiration, validation, or a concrete redesign plan?

If context is unclear from the conversation, infer from recent files or ask one focused question.

### Step 3: Synthesize Across Themes

Organize insights around the major cross-cutting themes from the transcripts:

**Theme 1: AI Native Company / Recursive Self-Improving Loops**
- YC self-improving company talk: AI is not a copilot bolted onto the old org; the company becomes a set of recursive loops
- Loop anatomy: sensor layer → policy/decision layer → deterministic tools → quality gates → learning mechanism
- Diana Hu: AI-native companies convert lossy open-loop human organizations into closed-loop systems
- Human role shifts to supervision, high-stakes judgment, ethics, novel real-world contact, and trust-bearing sales/customer moments

**Theme 2: Company Brain, Legibility, and Memory**
- YC: if it is not recorded, it did not happen to the company's intelligence
- Company brain = emails, DMs, Slack, meetings, code, telemetry, customer conversations, skills, know-how, and decision traces
- Garry Tan: G brain / knowledge systems need schema, search, graph/backlinks, provenance, and epistemology to track hunches vs. beliefs vs. world knowledge
- Karpathy: LLMs have anterograde amnesia; organizations must explicitly program memory and context

**Theme 3: Skills, Resolvers, Tools, and Evals as Org Primitives**
- Garry Tan: skills are employee-like capabilities; resolvers are org-chart/routing; memory/schema is process/state; check-resolvable is audit/compliance; trigger evals are performance review
- Deterministic code belongs in tools; latent judgment belongs in prompts/skills/evals; confusing the two breaks agentic systems
- Skillify means turning a successful one-off workflow into a tested, routed, repeatable capability: unit tests, LLM evals, integration tests, resolver trigger, smoke test, schema
- Taste is not delegated away; taste becomes domain-specific evals, trace review, customer-trust checks, and business-goal checks

**Theme 4: Software 3.0 / The New Programming Paradigm**
- Karpathy: LLMs are a new layer of compute; natural language is the new programming interface
- Truell (Cursor): "Vibe coding" as the emergent behavior — non-engineers shipping real software
- Masad (Replit): Software creation democratized; who builds software is changing
- Garry Tan: the founder can run a software factory with plan-eng-review, high test coverage, multi-agent review, and reusable skill packs

**Theme 5: AI-Native Products vs. AI-Wrapped Products**
- Field (Figma): AI changes what products are possible, not just how they're built
- Srinivas: Being AI-native from day 1 is a durable advantage incumbents can't fully replicate
- Truell: Cursor succeeded by re-thinking the entire IDE, not adding AI to VS Code
- AI Native Company extends this: not only product UX but company operating model must be redesigned around agents, memory, tools, and evals

**Theme 6: Burn Tokens, Not Headcount / Revenue per Employee**
- YC: startups are reaching demo day with far higher revenue per employee; token usage and agent leverage become a core constraint
- Garry + Diana: a small team can hit eight-figure revenue by embedding agents into painful vertical workflows and deploying full solutions
- Middle management's old information-routing function shrinks; IC/builders/operators and named DRIs become more important
- Track token-maxed experimentation carefully: useful directionally, but do not create gameable leaderboards detached from outcomes

**Theme 7: Vertical Workflow Wedges and FDE-Style Learning**
- Diana Hu: pick a painful workflow, go deep inside the customer, become the forward deployed engineer, and automate messy domain work
- Salient, HappyRobot, and document-processing examples show the pattern: not demos, but full solutions embedded into real customer operations
- Ng: iteration speed is the new moat; AI-native teams should compress customer learning and product change cycles
- Founder panel: defensibility comes from distribution, workflow depth, proprietary traces/evals, and data flywheels — not from a thin model wrapper

**Theme 8: AGI Paths, Infra, and Physical-World Frontiers**
- Altman, Kaplan, Chollet disagree productively: scaling vs. architectural breakthroughs vs. general intelligence benchmarks
- Altman/Nadella/Kaplan: inference cost curves, hyperscaling, and enterprise adoption shape what products are economically possible
- Fei-Fei Li, Finn, Jumper: spatial intelligence, robotics, and AI for science push AI-native thinking into the physical world
- Musk: first-principles thinking; do not optimize existing systems — question the system itself

### Step 4: Apply to User's Situation

Map the most relevant 2-4 themes to the user's specific context. Be direct:
- "Given you're building X, the AI Native Company frame says this should not be a copilot; it should become a closed loop because..."
- "Your missing layer is not another agent, but company legibility: what must be recorded, summarized, routed, and made searchable is..."
- "This workflow should be skillified: the deterministic tool layer is A, the latent judgment is B, the eval is C, and the resolver trigger is D."
- "Srinivas/Field/Truell's AI-native vs. AI-wrapped product distinction is now also an org-design distinction..."

### Step 5: Highlight Actionable Takeaways

Close with 3-5 concrete, prioritized actions for the user as an AI founder, builder, or operator:
- Specific product or org-design decisions to make or revisit
- Which workflows to convert into recursive self-improving loops first
- What to record to make the company legible to AI
- Which skills/resolvers/tools/evals/memory schemas to create
- What human approval gates must remain for trust, ethics, security, or customer risk
- What revenue-per-employee or token-leverage metric to inspect without making it gameable

### Step 6: Run the Interactive Self-Assessment Workbook

- Ask each question about the user's AI strategy/company design ONE AT A TIME using AskUserQuestion
- Wait for the user's response before asking the next question
- After each answer, provide brief feedback connecting their response to the relevant speaker's framework
- After all questions, synthesize their answers into a personalized AI Native Company assessment
- Save the completed assessment (questions + answers + synthesis) to the appropriate knowledge path

## Output Format

```
## AI Native Company — Insights for [User's Context]

### Most Relevant Themes

**[Theme Name]** — [2-3 sentences synthesizing 2+ speakers on this theme and why it applies]

**[Theme Name]** — [same]

**[Theme Name]** — [same]

### Applied to Your Situation

[Direct application paragraph — specific, not generic]

### Actionable Takeaways

1. [Action] — [Why, citing specific speaker/insight]
2. [Action] — [Why]
3. [Action] — [Why]
```

Always cite specific speakers by name. Avoid generic AI enthusiasm — these speakers often disagree, and the disagreements are informative.

When the user asks for “AI Native Company” specifically, include a practical redesign table:

| Company function | Current open-loop / human-lossy state | AI-native closed loop | Human gate | First skill/tool/eval to build |
|---|---|---|---|---|
| ... | ... | sensor → policy → tool → quality gate → learning | ... | ... |

### Interactive AI Native Company Workbook (AskUserQuestion)
- Ask questions about the user's AI strategy/company design ONE AT A TIME — do not list all questions at once
- Use AskUserQuestion tool for each question
- After each answer, give 1-2 sentence feedback connecting to the relevant speaker's framework
- Provide multiple choice options where appropriate to make it easier to answer
- After completing all questions, generate a synthesis:
  - Overall readiness score (1-10) for AI Native Company design
  - Top strength identified from answers
  - Top gap identified from answers
  - One specific loop/skill/eval to implement next
- Save completed workbook to `knowledge/yc-startup-school/ai-native-company-workbook.md`

Questions to ask interactively:
1. Are you using AI as a copilot, a software factory, or a company operating system? What would change if you rebuilt around the third option? (YC: AI Native Company)
2. Which important company signal is currently not recorded, summarized, or retrievable by agents? (YC: if it is not recorded, it did not happen to the intelligence)
3. Pick one workflow. What are its sensor layer, policy/decision layer, deterministic tools, quality gates, and learning mechanism? (Self-improving company loop)
4. What should become a skill, what should become a resolver route, what should become a deterministic tool, and what should become an eval? (Garry Tan: skills/resolvers/memory/evals as org primitives)
5. Where does human taste still need to judge traces, outputs, customer trust, or business outcomes? (Diana Hu: taste becomes evals)
6. What is your iteration speed right now — how many product/company changes can you ship per week? (Ng: iteration speed as the new moat)
7. Is your product/company AI-native or AI-wrapped? What would it look like to re-think it from scratch around AI? (Karpathy/Srinivas/Field/Truell)
8. What is your data flywheel — does using your product or operating system improve future agents, evals, or workflows? (Srinivas + AI Native Company)
9. Where does your product sit on the spectrum from demo to defensible full solution? What makes it hard to replicate? (panel + Diana Hu vertical workflow wedge)
10. Which AI theme is most directly relevant to your product — and which is most threatening to your current approach?

## References

- Transcript directory: `${CLAUDE_PLUGIN_ROOT}/skills/ai-startup-school/references/`
- 17 files covering: Karpathy, Ng, Srinivas, Finn, Musk, panel, Fei-Fei Li, Field, Chollet, Jumper, Truell, Altman, Nadella, Kaplan, Masad, Garry Tan, Diana Hu
- New AI Native Company sources:
  - `how-to-build-a-self-improving-company-with-ai.md` — recursive self-improving company loops
  - `the-ai-native-company-how-one-founder-becomes-a-1000x-engineer.md` — skills/resolvers/memory/evals and closed-loop organizations
