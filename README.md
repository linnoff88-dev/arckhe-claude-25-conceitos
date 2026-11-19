# Os 25 conceitos do Claude para quem nÃ£o programa

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


[![Os 25 conceitos do Claude](guia/assets/banner.jpg)](https://inematds.github.io/claude-25-conceitos/guia/)

**ðŸ‡§ðŸ‡· [PortuguÃªs](README.md) Â· ðŸ‡ºðŸ‡¸ [English](README.en.md) Â· ðŸ‡ªðŸ‡¸ [EspaÃ±ol](README.es.md)**

## O que Ã©

Este guia explica, em portuguÃªs simples, os 25 recursos do Claude (o assistente de IA da Anthropic) que mais aparecem na leva de novidades das Ãºltimas semanas. Ã‰ para quem usa o Claude no trabalho mas nÃ£o programa: contador, dono de clÃ­nica, lojista, professor. Cada conceito tem uma explicaÃ§Ã£o curta, um exemplo do dia a dia e o plano em que estÃ¡ disponÃ­vel. No fim, uma tabela de planos, trÃªs passos para comeÃ§ar e prompts prontos para copiar. Para ler nÃ£o precisa instalar nada; alguns recursos pedem o plano Pro e o app de computador.

## ðŸ“– Guia

PÃ¡gina completa: **https://inematds.github.io/claude-25-conceitos/guia/**

## As 5 partes

1. **O cÃ©rebro** â€” modelos (Haiku, Sonnet e Opus 5.5), Fable 5.1, tokens e janela de contexto, nÃ­vel de esforÃ§o, limites e planos.
2. **Onde usar** â€” Chat, Claude Code, Cowork, sessÃµes e split view, side chats, Claude Duet.
3. **O que ele faz** â€” Artifacts, Docs/Slides/Design, Dashboards, Motion.
4. **O que ele sabe de vocÃª** â€” memÃ³ria, CLAUDE.md, skills, conectores, plugins, mods.
5. **Trabalhar sozinho** â€” modos de permissÃ£o, subagentes, Projects, `/goal` + bÃ´nus: tarefas agendadas.

Mais: tabela "qual plano tem o quÃª", "por onde comeÃ§ar: sÃ³ 3 coisas" e prompts prontos (modelo de CLAUDE.md, prompt para criar skill, 3 exemplos de `/goal`).

Fatos conferidos nas pÃ¡ginas oficiais (claude.com, code.claude.com, support.claude.com) em 01/11/2026. Planos e recursos em beta mudam rÃ¡pido: confira em claude.com/pricing.

## O processo, do inÃ­cio ao fim

| # | Passo | Quem faz | Comando / onde |
|---|---|---|---|
| 1 | Levantar e conferir os fatos nas pÃ¡ginas oficiais (o que Ã© confirmado, divergente ou nÃ£o achado) | ðŸ§  sessÃ£o | `longrun/<data>-claude-25-conceitos/FATOS.md` (no projeto wifi) |
| 2 | Gerar a capa e a arte da hero | âš™ï¸ script (Codex image_gen) | `node ~/.claude/skills/capa-inema/assets/gerar-capa.cjs --repo . --title "Os 25 conceitos do Claude" --cat Guia --save-raw guia/assets/hero.png --gerador auto` |
| 3 | Gerar os 6 banners (live + grade Ã— PT/EN/ES) | âš™ï¸ script (Codex image_gen) | `bash ~/.claude/skills/projetos-landing-guia/assets/gerar-banner.sh --repo . ... [--estilo grade] [--lang en\|es]` |
| 4 | Escrever o guia em PT (25 cartÃµes `data-conceito`, planos, 3 passos, prompts, vÃ­deos) | ðŸ§  sessÃ£o | `guia/index.html` |
| 5 | Traduzir para EN e ES | ðŸ¤– tradutor central (Codex pela assinatura) | `inema-traduz < pedido.txt -o guia/en/index.html` (idem `es`) |
| 6 | Verificar: 25 conceitos em cada idioma, nada de fonte externa, sem texto PT sobrando | âš™ï¸ script | `grep -c 'data-conceito' guia/index.html guia/en/index.html guia/es/index.html` |
| 7 | Publicar (commit + push; o GitHub Actions sobe o Pages) | ðŸ§  sessÃ£o | `git push` â†’ `.github/workflows/pages.yml` |
| 8 | Conferir no ar (PT/EN/ES respondem 200) e print mobile/desktop | âš™ï¸ script | `curl -sI https://inematds.github.io/claude-25-conceitos/guia/` |
| 9 | PÃ´r os links dos vÃ­deos quando saÃ­rem | ðŸ§  sessÃ£o | trocar os marcadores `<!-- VIDEO-EXPLICA -->` e `<!-- VIDEO-RTEX -->` nos 3 idiomas |

## LicenÃ§a e aviso

ConteÃºdo aberto e gratuito do [INEMA.CLUB](https://inema.club). Guia independente; nÃ£o Ã© material oficial da Anthropic.

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>