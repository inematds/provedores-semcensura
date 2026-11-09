# CLAUDE.md — provedores-semcensura

Página landing + guia (PT/EN/ES) sobre provedores de IA sem censura (uncensored/abliterated) por API, roteador, GPU alugada ou local.

- Guia: `guia/index.html` (PT, fonte), `guia/en/`, `guia/es/`; banners em `guia/assets/`; capa em `capa/capa.png`.
- Publicação: commit + push em `inematds/provedores-semcensura`; GitHub Pages via Actions (`.github/workflows/pages.yml`). Autor: `inematds <inematds@gmail.com>`. Push que toca `.github/workflows/` vai por SSH (token `gh` sem escopo `workflow`).
- Fonte dos fatos: `~/projetos/output/provedores-semcensura/PESQUISA.md`. Nunca inventar preço, KYC ou política; o que não foi confirmado aparece como "não confirmado / confira no site". Preço sempre com data ("conferido em DD/MM/AAAA").
- Não citar autor, canal ou vídeo de origem. Não criar contas nem chamar APIs de provedores de IA.
- Mudou o PT → retraduzir com `inema-traduz` e conferir EN/ES (mesma contagem de tags, nenhuma palavra PT sobrando).
- Processo completo: README, seção "O processo, do início ao fim".

## Self-learning

When I correct you, or you catch yourself making a mistake: before continuing, add the lesson as a one-line rule at the TOP of the Lessons section below, so it never happens again.

## Lessons
- Base URL de provedor no exemplo de código só depois de conferir na doc pública (Venice = `https://api.venice.ai/api/v1`; Ollama local = `http://localhost:11434/v1`, chave obrigatória mas ignorada). (09/11/2026)
