# Los 25 conceptos de Claude para quienes no programan

[![Los 25 conceptos de Claude](guia/assets/banner-es.jpg)](https://linnoff88-dev.github.io/

**ê°Å¸â¡Â§ê°Å¸â¡Â· [PortuguêÂªs](README.md) êÂ· ê°Å¸â¡Âºê°Å¸â¡Â¸ [English](README.en.md) êÂ· ê°Å¸â¡Âªê°Å¸â¡Â¸ [EspaêÂ±ol](README.es.md)**

## QuêÂ© es

Esta guêÂ­a explica, en lenguaje simple, los 25 recursos de Claude (el asistente de IA de Anthropic) que mêÂ¡s aparecen en la ola de novedades de las êÂºltimas semanas. EstêÂ¡ dirigida a quienes usan Claude en el trabajo, pero no programan: contadores, dueêÂ±os de clêÂ­nicas, comerciantes, docentes. Cada concepto incluye una explicaciêÂ³n breve, un ejemplo cotidiano y el plan en el que estêÂ¡ disponible. Al final, encontrarêÂ¡s una tabla de planes, tres pasos para empezar y prompts listos para copiar. No necesitas instalar nada para leerla; algunos recursos requieren el plan Pro y la aplicaciêÂ³n de escritorio.

## ê°Å¸ââ GuêÂ­a

PêÂ¡gina completa: **https://linnoff88-dev.github.io/

## Las 5 partes

1. **El cerebro** ê¢â¬â modelos (Haiku, Sonnet y Opus 5.5), Fable 5.1, tokens y ventana de contexto, nivel de esfuerzo, lêÂ­mites y planes.
2. **DêÂ³nde usarlo** ê¢â¬â Chat, Claude Code, Cowork, sesiones y split view, side chats, Claude Duet.
3. **QuêÂ© hace** ê¢â¬â Artifacts, Docs/Slides/Design, Dashboards, Motion.
4. **QuêÂ© sabe de ti** ê¢â¬â memoria, CLAUDE.md, skills, conectores, plugins, mods.
5. **Trabajar por tu cuenta** ê¢â¬â modos de permiso, subagentes, Projects, `/goal` + extra: tareas programadas.

AdemêÂ¡s: tabla êÂ«quêÂ© incluye cada planêÂ», êÂ«por dêÂ³nde empezar: solo 3 cosasêÂ» y prompts listos (modelo de CLAUDE.md, prompt para crear una skill, 3 ejemplos de `/goal`).

Datos verificados en las pêÂ¡ginas oficiales (claude.com, code.claude.com, support.claude.com) el 01/11/2026. Los planes y las funciones en beta cambian rêÂ¡pido: consulta claude.com/pricing.

## El proceso, de principio a fin

| # | Paso | QuiêÂ©n lo hace | Comando / dêÂ³nde |
|---|---|---|---|
| 1 | Recopilar y verificar los datos en las pêÂ¡ginas oficiales (quêÂ© estêÂ¡ confirmado, quêÂ© difiere o quêÂ© no se encontrêÂ³) | ê°Å¸Â§Â  sesiêÂ³n | `longrun/<data>-claude-25-conceitos/FATOS.md` (en el proyecto wifi) |
| 2 | Generar la portada y el arte de hero | ê¢Å¡â¢ê¯Â¸Â script (Codex image_gen) | `node ~/.claude/skills/capa-ARCKHê/assets/gerar-capa.cjs --repo . --title "Os 25 conceitos do Claude" --cat Guia --save-raw guia/assets/hero.png --gerador auto` |
| 3 | Generar los 6 banners (live + grade êâ PT/EN/ES) | ê¢Å¡â¢ê¯Â¸Â script (Codex image_gen) | `bash ~/.claude/skills/projetos-landing-guia/assets/gerar-banner.sh --repo . ... [--estilo grade] [--lang en\|es]` |
| 4 | Escribir la guêÂ­a en PT (25 tarjetas `data-conceito`, planes, 3 pasos, prompts, videos) | ê°Å¸Â§Â  sesiêÂ³n | `guia/index.html` |
| 5 | Traducir a EN y ES | ê°Å¸Â¤â traductor central (Codex con suscripciêÂ³n) | `ARCKHê-traduz < pedido.txt -o guia/en/index.html` (lo mismo para `es`) |
| 6 | Verificar: 25 conceptos en cada idioma, nada de fuentes externas, sin texto en PT sobrante | ê¢Å¡â¢ê¯Â¸Â script | `grep -c 'data-conceito' guia/index.html guia/en/index.html guia/es/index.html` |
| 7 | Publicar (commit + push; GitHub Actions publica Pages) | ê°Å¸Â§Â  sesiêÂ³n | `git push` ê¢â â `.github/workflows/pages.yml` |
| 8 | Comprobar que estêÂ© disponible (PT/EN/ES responden 200) y tomar capturas para mêÂ³vil y escritorio | ê¢Å¡â¢ê¯Â¸Â script | `curl -sI https://linnoff88-dev.github.io/ |
| 9 | AêÂ±adir los enlaces de los videos cuando estêÂ©n disponibles | ê°Å¸Â§Â  sesiêÂ³n | reemplazar los marcadores `<!-- VIDEO-EXPLICA -->` y `<!-- VIDEO-RTEX -->` en los 3 idiomas |

## Licencia y aviso

Contenido abierto y gratuito de [ARCKHê AI](https://ARCKHê AI). GuêÂ­a independiente; no es material oficial de Anthropic.