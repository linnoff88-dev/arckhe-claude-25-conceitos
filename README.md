# Os 25 conceitos do Claude para quem nêÂ£o programa

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


[![Os 25 conceitos do Claude](guia/assets/banner.jpg)](https://linnoff88-dev.github.io/

**ê°Å¸â¡Â§ê°Å¸â¡Â· [PortuguêÂªs](README.md) êÂ· ê°Å¸â¡Âºê°Å¸â¡Â¸ [English](README.en.md) êÂ· ê°Å¸â¡Âªê°Å¸â¡Â¸ [EspaêÂ±ol](README.es.md)**

## O que êÂ©

Este guia explica, em portuguêÂªs simples, os 25 recursos do Claude (o assistente de IA da Anthropic) que mais aparecem na leva de novidades das êÂºltimas semanas. êâ° para quem usa o Claude no trabalho mas nêÂ£o programa: contador, dono de clêÂ­nica, lojista, professor. Cada conceito tem uma explicaêÂ§êÂ£o curta, um exemplo do dia a dia e o plano em que estêÂ¡ disponêÂ­vel. No fim, uma tabela de planos, trêÂªs passos para comeêÂ§ar e prompts prontos para copiar. Para ler nêÂ£o precisa instalar nada; alguns recursos pedem o plano Pro e o app de computador.

## ê°Å¸ââ Guia

PêÂ¡gina completa: **https://linnoff88-dev.github.io/

## As 5 partes

1. **O cêÂ©rebro** ê¢â¬â modelos (Haiku, Sonnet e Opus 5.5), Fable 5.1, tokens e janela de contexto, nêÂ­vel de esforêÂ§o, limites e planos.
2. **Onde usar** ê¢â¬â Chat, Claude Code, Cowork, sessêÂµes e split view, side chats, Claude Duet.
3. **O que ele faz** ê¢â¬â Artifacts, Docs/Slides/Design, Dashboards, Motion.
4. **O que ele sabe de vocêÂª** ê¢â¬â memêÂ³ria, CLAUDE.md, skills, conectores, plugins, mods.
5. **Trabalhar sozinho** ê¢â¬â modos de permissêÂ£o, subagentes, Projects, `/goal` + bêÂ´nus: tarefas agendadas.

Mais: tabela "qual plano tem o quêÂª", "por onde comeêÂ§ar: sêÂ³ 3 coisas" e prompts prontos (modelo de CLAUDE.md, prompt para criar skill, 3 exemplos de `/goal`).

Fatos conferidos nas pêÂ¡ginas oficiais (claude.com, code.claude.com, support.claude.com) em 01/11/2026. Planos e recursos em beta mudam rêÂ¡pido: confira em claude.com/pricing.

## O processo, do inêÂ­cio ao fim

| # | Passo | Quem faz | Comando / onde |
|---|---|---|---|
| 1 | Levantar e conferir os fatos nas pêÂ¡ginas oficiais (o que êÂ© confirmado, divergente ou nêÂ£o achado) | ê°Å¸Â§Â  sessêÂ£o | `longrun/<data>-claude-25-conceitos/FATOS.md` (no projeto wifi) |
| 2 | Gerar a capa e a arte da hero | ê¢Å¡â¢ê¯Â¸Â script (Codex image_gen) | `node ~/.claude/skills/capa-ARCKHê/assets/gerar-capa.cjs --repo . --title "Os 25 conceitos do Claude" --cat Guia --save-raw guia/assets/hero.png --gerador auto` |
| 3 | Gerar os 6 banners (live + grade êâ PT/EN/ES) | ê¢Å¡â¢ê¯Â¸Â script (Codex image_gen) | `bash ~/.claude/skills/projetos-landing-guia/assets/gerar-banner.sh --repo . ... [--estilo grade] [--lang en\|es]` |
| 4 | Escrever o guia em PT (25 cartêÂµes `data-conceito`, planos, 3 passos, prompts, vêÂ­deos) | ê°Å¸Â§Â  sessêÂ£o | `guia/index.html` |
| 5 | Traduzir para EN e ES | ê°Å¸Â¤â tradutor central (Codex pela assinatura) | `ARCKHê-traduz < pedido.txt -o guia/en/index.html` (idem `es`) |
| 6 | Verificar: 25 conceitos em cada idioma, nada de fonte externa, sem texto PT sobrando | ê¢Å¡â¢ê¯Â¸Â script | `grep -c 'data-conceito' guia/index.html guia/en/index.html guia/es/index.html` |
| 7 | Publicar (commit + push; o GitHub Actions sobe o Pages) | ê°Å¸Â§Â  sessêÂ£o | `git push` ê¢â â `.github/workflows/pages.yml` |
| 8 | Conferir no ar (PT/EN/ES respondem 200) e print mobile/desktop | ê¢Å¡â¢ê¯Â¸Â script | `curl -sI https://linnoff88-dev.github.io/ |
| 9 | PêÂ´r os links dos vêÂ­deos quando saêÂ­rem | ê°Å¸Â§Â  sessêÂ£o | trocar os marcadores `<!-- VIDEO-EXPLICA -->` e `<!-- VIDEO-RTEX -->` nos 3 idiomas |

## LicenêÂ§a e aviso

ConteêÂºdo aberto e gratuito do [ARCKHê AI](https://ARCKHê AI). Guia independente; nêÂ£o êÂ© material oficial da Anthropic.

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>