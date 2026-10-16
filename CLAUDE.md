# yc-startup-school — YC Startup School skills

Agent skills for the YC Startup School family (`yc-1…yc-8`, `yc-ai`, `yc-pg`), derived from github.com/team-attention/yc-startup-school. `README.md` is the user-facing description; this file holds maintenance invariants.

## Layout & invariants

- Each `skills/<name>/` is self-contained: `SKILL.md`, `agents/openai.yaml`, and its sources under `references/`. Link sources with skill-relative paths (`references/<file>.md`). Do not use absolute paths, links outside the skill folder, or `${CLAUDE_PLUGIN_ROOT}`; installs may copy or symlink a single skill folder.
- `references/bonus/` holds lectures no skill uses yet. Move a file into a skill's `references/` before linking it.
- Workbook files are saved only on request, to the user's destination or `yc-startup-school-notes/` in the current working directory. `knowledge/` is a git-ignored local output folder, not corpus.
- Keep descriptions free of skills that are not in this repository.

## Corpus discipline

- Preserve imported lecture and essay files byte-for-byte; frontmatter and TOC blocks are the only labeled additions. Files that held only metadata may be filled with captions under the provenance rule below.
- Added transcripts keep provenance in frontmatter: YouTube URL, retrieval date, `transcript_auto_generated`, `transcript_human_verified: false`, and `transcript_sha256` over the text after the Transcript heading. List them in the skill's source map with the auto-caption note.
- `reading-notes.md` and `source-map.md` are navigation aids, not evidence; remove claims from them that the source text does not support. Skills cite titles, speakers, and frontmatter URLs, not local paths.

## Behavior to preserve

Answer questions, review supplied material, and run workbooks only on request. Attribute claims to the actual speaker or author and check quotes against the source. Separate source advice from its application, and do not treat YC's premise of a company aiming for very fast growth (often venture-funded) as the user's goal. Keep the conditions attached to cited numbers, match the source's certainty, and define named concepts as the source does.

## Release

Publish to github.com/seeknowzip/yc-startup-school (a fork of team-attention/yc-startup-school) from a clean export, never by pushing a working copy's history. Replace the published tree wholesale with `skills/`, `references/`, `scripts/`, `.claude-plugin/`, `README.md`, `LICENSE`, `CLAUDE.md`, `AGENTS.md`, and `.gitignore`, so renamed or removed upstream files do not linger. Before pushing, check that `find skills -name SKILL.md` lists exactly the ten skills, that `grep -r "AskUserQuestion\|CLAUDE_PLUGIN_ROOT" skills` finds nothing, and that `claude plugin validate .` passes. After pushing, install through both marketplaces (`yc-startup-school@seeknowzip-yc`) in a clean Claude Code and Codex home.

Upstream naming: `yc-ai` was `ai-startup-school`; `yc-pg` was `guru-paul-graham`.
