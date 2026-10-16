# YC Startup School skills

Agent skills that help you apply Y Combinator's Startup School lectures to the work in front of you. Describe your situation or share a plan in Claude Code or Codex, and the agent reads the relevant lectures, applies them to your case, and says which lecture and speaker each point comes from. It is meant for people founding a startup, running a solo or small business, or leading a new product inside a company.

This is a modified version of [team-attention/yc-startup-school](https://github.com/team-attention/yc-startup-school) by Team Attention. See [Changes from the original](#changes-from-the-original). It is not affiliated with or endorsed by Y Combinator.

## Skills

| Skill | Use it when | Sources |
|---|---|---|
| `yc-1-deciding-to-start-a-startup` | Deciding whether and when to start | Harj Taggar; Dalton Caldwell & Michael Seibel; 2 Paul Graham essays |
| `yc-2-getting-and-evaluating-startup-ideas` | Judging, finding, or pivoting an idea | Jared Friedman; Dalton Caldwell; Dalton Caldwell & Michael Seibel; Paul Graham |
| `yc-3-building-your-founding-team` | Finding co-founders, working together, splitting equity | Catheryn Li & Divya Bhat; Harj Taggar; Michael Seibel; Dalton Caldwell & Michael Seibel; Kevin Hale |
| `yc-4-planning-an-mvp` | Preparing user interviews, scoping an MVP | Gustaf Alströmer; Michael Seibel; Diana Hu; Tom Blomfield (vibe coding) |
| `yc-5-launching` | Planning a launch and first customers | Kat Mañalac; Gustaf Alströmer; Paul Graham; Aaron Epstein (cold email) |
| `yc-6-growing-and-monetizing` | Choosing metrics, growth priorities, business model, pricing | Divya Bhat; Tom Blomfield; Aaron Epstein; Gustaf Alströmer; related lectures by Tom Blomfield and David Lieb |
| `yc-7-fundraising-and-company-building` | Preparing to raise or apply to YC | Brad Flora; Dalton Caldwell |
| `yc-8-stories-from-great-founders` | Learning from the Zuckerberg and Wojcicki talks | Mark Zuckerberg, Anne Wojcicki (interviewed by Sam Altman) |
| `yc-ai` | Applying AI talks to AI product, company, or workflow decisions | 15 AI Startup School talks and 2 talks on AI-native companies |
| `yc-pg` | Applying Paul Graham's startup essays | 14 essays |

Each skill keeps its sources in its own `references/` folder, so a skill also works when its folder is installed on its own.

## Install

The repository is both a Claude Code plugin marketplace and a Codex plugin marketplace. Restart the app or start a new session after installing.

**Claude Code**

```bash
claude plugin marketplace add seeknowzip/yc-startup-school
claude plugin install ycombinator-startup-school@ycombinator-startup-school
```

Inside a Claude Code session, the same steps are `/plugin marketplace add seeknowzip/yc-startup-school` and `/plugin install ycombinator-startup-school@ycombinator-startup-school`.

**Codex**

```bash
codex plugin marketplace add seeknowzip/yc-startup-school
codex plugin add ycombinator-startup-school@ycombinator-startup-school
```

**Without the plugin system** — copy the skill folders into your personal skills directory:

```bash
git clone https://github.com/seeknowzip/yc-startup-school.git
mkdir -p ~/.claude/skills && cp -R yc-startup-school/skills/* ~/.claude/skills/   # Claude Code
mkdir -p ~/.agents/skills && cp -R yc-startup-school/skills/* ~/.agents/skills/   # Codex (older versions also read ~/.codex/skills)
```

## Use

Describe your situation in plain language; the agent picks the matching skill. You can also call a skill directly:

- Claude Code plugin: `/ycombinator-startup-school:yc-4-planning-an-mvp` (type `/yc-4` and pick it from the list). Copied skills are `/yc-4-planning-an-mvp`.
- Codex: `$yc-4-planning-an-mvp` (type `$` to pick a skill).

Example requests:

- "My friend and I are starting a company. Is a 50:50 equity split OK?"
- "Review the MVP scope I set for a new feature at work: …"
- "I run a SaaS on my own. Which metrics should I track?"
- "Walk me through the module 4 workbook."
- "Apply Paul Graham's Do Things That Don't Scale to my 40-customer subscription business."

## How the skills respond

- **Question:** answers it from the relevant lectures.
- **Review:** looks at the plan, draft, or evidence you share and applies the lectures to it.
- **Workbook:** runs the module workbook only when you ask for one, and saves a file only when you ask. Without a destination, files go to `yc-startup-school-notes/` in the current working directory.

The skills separate what a speaker said from how it applies to you. YC advice often assumes a startup aiming for very fast growth, usually with venture funding; the skills keep your goals, such as a solo or bootstrapped business or a product inside a company, in view instead of treating that context as a requirement.

## Changes from the original

- Answers match the request. Most original skills read every source, asked workbook questions one at a time, and saved an assessment on every call. Questions now get answers, reviews get reviews, and the workbook runs on request.
- Reads only the lectures a request needs. The original concept summaries are kept as `reading-notes.md` for finding topics, with claims the source text does not support removed; quotes and claims are checked against the source text.
- Fills lectures that had no transcript. Eleven curriculum lectures were missing text (metadata only, missing files, or video only). They now contain English auto-generated YouTube captions with timestamps, marked `transcript_auto_generated: true` and `transcript_human_verified: false`.
- Separates lecture advice from its application to the user's situation, including the fast-growth assumption noted above.
- Cites lecture titles, speakers, and source URLs instead of local file paths.
- `ai-startup-school` is renamed `yc-ai`, and `guru-paul-graham` is renamed `yc-pg`. Both follow the same request handling. The PG skill no longer speaks in Paul Graham's voice.
- Related bonus lectures used by modules 4–7 moved into those skills' `references/`. `references/bonus/` keeps four lectures that no skill uses yet.
- Installs as a plugin in both Claude Code and Codex, with Codex UI metadata in each skill's `agents/openai.yaml`.
- Unrelated drafts in the original repository root were removed.

Transcripts and essays carried over from the original are unchanged, except the three files that held only metadata, which now contain captions. Two frontmatter values were re-quoted so YAML parsers can read them.

## Sources

Most transcripts come from `ycombinator.com/library`; Paul Graham essays come from the YC Library and `paulgraham.com`; the added lectures use YouTube auto-generated captions. The original scraper is kept at `scripts/scrape_yc_library.py`; it writes to `transcripts/` for review rather than into the skill folders.

## Credits

- [Team Attention](https://github.com/team-attention) — the original [yc-startup-school](https://github.com/team-attention/yc-startup-school) skills, transcript collection, and scraper
- [Y Combinator](https://www.ycombinator.com/) — Startup School and AI Startup School lecture content, used for educational purposes
- [Paul Graham](https://paulgraham.com/) — original essays

## License

MIT for the skill instructions and repository code. See [LICENSE](LICENSE).

Lecture transcripts, captions, and essays remain the property of their respective authors and Y Combinator. They are not covered by the MIT license. If you hold rights to included content and want it removed, please open an issue.
