# Claudeâ€™s 25 Concepts for People Who Donâ€™t Code

[![Claudeâ€™s 25 Concepts](guia/assets/banner-en.jpg)](https://linnoff88-dev.github.io/

**ðŸ‡§ðŸ‡· [PortuguÃªs](README.md) Â· ðŸ‡ºðŸ‡¸ [English](README.en.md) Â· ðŸ‡ªðŸ‡¸ [EspaÃ±ol](README.es.md)**

## What it is

This guide explains, in plain language, the 25 Claude features (Anthropicâ€™s AI assistant) that have appeared most often in the wave of announcements over the past few weeks. It is for people who use Claude at work but donâ€™t code: accountants, clinic owners, shopkeepers, teachers. Each concept has a short explanation, an everyday example, and the plan that includes it. At the end, thereâ€™s a plan comparison table, three steps to get started, and ready-to-copy prompts. You donâ€™t need to install anything to read it; some features require the Pro plan and the desktop app.

## ðŸ“– Guide

Full page: **https://linnoff88-dev.github.io/

## The 5 parts

1. **The brain** â€” models (Haiku, Sonnet, and Opus 5.5), Fable 5.1, tokens and context window, effort level, limits, and plans.
2. **Where to use it** â€” Chat, Claude Code, Cowork, sessions and split view, side chats, Claude Duet.
3. **What it does** â€” Artifacts, Docs/Slides/Design, Dashboards, Motion.
4. **What it knows about you** â€” memory, CLAUDE.md, skills, connectors, plugins, mods.
5. **Working on its own** â€” permission modes, subagents, Projects, `/goal` + bonus: scheduled tasks.

Also included: a â€œwhich plan has whatâ€ table, â€œwhere to start: just 3 things,â€ and ready-to-use prompts (a CLAUDE.md template, a prompt to create a skill, 3 `/goal` examples).

Facts checked against official pages (claude.com, code.claude.com, support.claude.com) on 11/01/2026. Plans and beta features change quickly: check claude.com/pricing.

## The process, from start to finish

| # | Step | Who does it | Command / where |
|---|---|---|---|
| 1 | Gather and verify facts on official pages (whatâ€™s confirmed, conflicting, or not found) | ðŸ§  session | `longrun/<data>-claude-25-conceitos/FATOS.md` (in the wifi project) |
| 2 | Generate the cover and hero artwork | âš™ï¸ script (Codex image_gen) | `node ~/.claude/skills/capa-ARCKHÉ/assets/gerar-capa.cjs --repo . --title "Os 25 conceitos do Claude" --cat Guia --save-raw guia/assets/hero.png --gerador auto` |
| 3 | Generate the 6 banners (live + grid Ã— PT/EN/ES) | âš™ï¸ script (Codex image_gen) | `bash ~/.claude/skills/projetos-landing-guia/assets/gerar-banner.sh --repo . ... [--estilo grade] [--lang en\|es]` |
| 4 | Write the guide in PT (25 `data-conceito` cards, plans, 3 steps, prompts, videos) | ðŸ§  session | `guia/index.html` |
| 5 | Translate into EN and ES | ðŸ¤– central translator (Codex by subscription) | `ARCKHÉ-traduz < pedido.txt -o guia/en/index.html` (same for `es`) |
| 6 | Verify: 25 concepts in each language, no external fonts, no leftover PT text | âš™ï¸ script | `grep -c 'data-conceito' guia/index.html guia/en/index.html guia/es/index.html` |
| 7 | Publish (commit + push; GitHub Actions publishes Pages) | ðŸ§  session | `git push` â†’ `.github/workflows/pages.yml` |
| 8 | Check that itâ€™s live (PT/EN/ES return 200) and capture mobile/desktop screenshots | âš™ï¸ script | `curl -sI https://linnoff88-dev.github.io/ |
| 9 | Add video links when theyâ€™re released | ðŸ§  session | replace the `<!-- VIDEO-EXPLICA -->` and `<!-- VIDEO-RTEX -->` markers in all 3 languages |

## License and notice

Open, free content from [ARCKHÉ AI](https://ARCKHÉ AI). Independent guide; not official Anthropic material.