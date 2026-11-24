# Los 25 conceptos de Claude para quienes no programan

[![Los 25 conceptos de Claude](guia/assets/banner-es.jpg)](https://linnoff88-dev.github.io/

**ðŸ‡§ðŸ‡· [PortuguÃªs](README.md) Â· ðŸ‡ºðŸ‡¸ [English](README.en.md) Â· ðŸ‡ªðŸ‡¸ [EspaÃ±ol](README.es.md)**

## QuÃ© es

Esta guÃ­a explica, en lenguaje simple, los 25 recursos de Claude (el asistente de IA de Anthropic) que mÃ¡s aparecen en la ola de novedades de las Ãºltimas semanas. EstÃ¡ dirigida a quienes usan Claude en el trabajo, pero no programan: contadores, dueÃ±os de clÃ­nicas, comerciantes, docentes. Cada concepto incluye una explicaciÃ³n breve, un ejemplo cotidiano y el plan en el que estÃ¡ disponible. Al final, encontrarÃ¡s una tabla de planes, tres pasos para empezar y prompts listos para copiar. No necesitas instalar nada para leerla; algunos recursos requieren el plan Pro y la aplicaciÃ³n de escritorio.

## ðŸ“– GuÃ­a

PÃ¡gina completa: **https://linnoff88-dev.github.io/

## Las 5 partes

1. **El cerebro** â€” modelos (Haiku, Sonnet y Opus 5.5), Fable 5.1, tokens y ventana de contexto, nivel de esfuerzo, lÃ­mites y planes.
2. **DÃ³nde usarlo** â€” Chat, Claude Code, Cowork, sesiones y split view, side chats, Claude Duet.
3. **QuÃ© hace** â€” Artifacts, Docs/Slides/Design, Dashboards, Motion.
4. **QuÃ© sabe de ti** â€” memoria, CLAUDE.md, skills, conectores, plugins, mods.
5. **Trabajar por tu cuenta** â€” modos de permiso, subagentes, Projects, `/goal` + extra: tareas programadas.

AdemÃ¡s: tabla Â«quÃ© incluye cada planÂ», Â«por dÃ³nde empezar: solo 3 cosasÂ» y prompts listos (modelo de CLAUDE.md, prompt para crear una skill, 3 ejemplos de `/goal`).

Datos verificados en las pÃ¡ginas oficiales (claude.com, code.claude.com, support.claude.com) el 01/11/2026. Los planes y las funciones en beta cambian rÃ¡pido: consulta claude.com/pricing.

## El proceso, de principio a fin

| # | Paso | QuiÃ©n lo hace | Comando / dÃ³nde |
|---|---|---|---|
| 1 | Recopilar y verificar los datos en las pÃ¡ginas oficiales (quÃ© estÃ¡ confirmado, quÃ© difiere o quÃ© no se encontrÃ³) | ðŸ§  sesiÃ³n | `longrun/<data>-claude-25-conceitos/FATOS.md` (en el proyecto wifi) |
| 2 | Generar la portada y el arte de hero | âš™ï¸ script (Codex image_gen) | `node ~/.claude/skills/capa-ARCKHÉ/assets/gerar-capa.cjs --repo . --title "Os 25 conceitos do Claude" --cat Guia --save-raw guia/assets/hero.png --gerador auto` |
| 3 | Generar los 6 banners (live + grade Ã— PT/EN/ES) | âš™ï¸ script (Codex image_gen) | `bash ~/.claude/skills/projetos-landing-guia/assets/gerar-banner.sh --repo . ... [--estilo grade] [--lang en\|es]` |
| 4 | Escribir la guÃ­a en PT (25 tarjetas `data-conceito`, planes, 3 pasos, prompts, videos) | ðŸ§  sesiÃ³n | `guia/index.html` |
| 5 | Traducir a EN y ES | ðŸ¤– traductor central (Codex con suscripciÃ³n) | `ARCKHÉ-traduz < pedido.txt -o guia/en/index.html` (lo mismo para `es`) |
| 6 | Verificar: 25 conceptos en cada idioma, nada de fuentes externas, sin texto en PT sobrante | âš™ï¸ script | `grep -c 'data-conceito' guia/index.html guia/en/index.html guia/es/index.html` |
| 7 | Publicar (commit + push; GitHub Actions publica Pages) | ðŸ§  sesiÃ³n | `git push` â†’ `.github/workflows/pages.yml` |
| 8 | Comprobar que estÃ© disponible (PT/EN/ES responden 200) y tomar capturas para mÃ³vil y escritorio | âš™ï¸ script | `curl -sI https://linnoff88-dev.github.io/ |
| 9 | AÃ±adir los enlaces de los videos cuando estÃ©n disponibles | ðŸ§  sesiÃ³n | reemplazar los marcadores `<!-- VIDEO-EXPLICA -->` y `<!-- VIDEO-RTEX -->` en los 3 idiomas |

## Licencia y aviso

Contenido abierto y gratuito de [ARCKHÉ AI](https://ARCKHÉ AI). GuÃ­a independiente; no es material oficial de Anthropic.