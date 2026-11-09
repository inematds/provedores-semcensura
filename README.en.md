# provedores-semcensura

[![Uncensored AI: where to use it, what it costs, and what to check](guia/assets/banner-en.jpg)](https://inematds.github.io/provedores-semcensura/guia/en/)

**🇧🇷 [Português](README.md) · 🇺🇸 [English](README.en.md) · 🇪🇸 [Español](README.es.md)**

## What it is

This guide shows where to find “uncensored” AI models, meaning versions that don’t refuse requests. It’s for people testing their own systems’ security, doing research, or simply looking for an assistant that doesn’t shut down on sensitive topics. A table lists providers offering API access, chat, rented GPUs, and local use on your own computer, along with prices, stated privacy policies, and whether they require identity verification. To use it, just read the guide; the examples require an account with the provider you choose or Ollama installed.

## 📖 User guide

Complete guide (landing page + step-by-step instructions): **https://inematds.github.io/provedores-semcensura/guia/en/**

## What’s in the guide

- The difference between **uncensored** (fine-tuned, like Dolphin), **abliterated** (removes the “refusal direction” from the weights without training), and **jailbroken** (a prompt that tricks the rules), and what gets lost when the guardrails are removed.
- How to find these models on Hugging Face.
- Comparison table: Venice, abliteration.ai, orcarouter (Ollama), OpenRouter, Featherless, RunPod, and local use with Ollama — type, models, price (checked on 09/11/2026), identity verification, stated privacy policy, OpenAI compatibility.
- “Which one to choose” for different situations.
- Step-by-step instructions: Venice through the OpenAI-compatible API, a local model with Ollama, and connecting it to an agent harness.
- Where your data goes and responsible use.

Nothing here was tested with an account or API key: the information comes from the providers’ public pages; anything that couldn’t be confirmed is marked “not confirmed.”

## The process, from start to finish

Legend: 🧠 session with Nei · ⚙️ script · 🤖 `claude -p` / agent

1. 🧠 **Research** the providers’ public pages (read-only, no account or API) → `~/projetos/output/provedores-semcensura/PESQUISA.md`, including anything that couldn’t be confirmed.
2. ⚙️ **Cover** for the catalog + raw hero artwork: `node ~/.claude/skills/capa-inema/assets/gerar-capa.cjs --repo . --title "Provedores de IA sem censura" --cat "IA" --save-raw guia/assets/hero.png --gerador auto` → `capa/capa.png`.
3. ⚙️ **Banners** (Codex image_gen via subscription), 2 styles × 3 languages: `bash ~/.claude/skills/projetos-landing-guia/assets/gerar-banner.sh --repo . --title "IA SEM CENSURA" --destaque "CENSURA" ...` (`--estilo grade --saida banner-grade`, `--lang en|es --saida banner-en|banner-es`...). Check the text in the image.
4. 🧠 **PT guide** in `guia/index.html` (skill `projetos-landing-guia`), using only facts from the research.
5. 🤖 **EN/ES translation** with the central translator: `inema-traduz -o out-en.html < prompt-en.txt` → `guia/en/index.html` and `guia/es/index.html`.
6. 🤖 **Independent review** by another agent (from the perspective of someone who has never seen the project).
7. ⚙️ **Publish**: `git push` → GitHub Actions (`.github/workflows/pages.yml`) publishes to Pages; check for a 200 response at `/guia/`, `/guia/en/`, `/guia/es/`.
8. 🧠 **Update prices**: repeat step 1 and change the “checked on” date in the guide and READMEs.

## Related on INEMA

- [Private AI in 3 tiers](https://inematds.github.io/ia-privada-3-niveis/guia/en/)
- [Defensive uncensored AI](https://inematds.github.io/ia-sem-censura-defensiva/guia/en/)

---

Open content from [INEMA.CLUB](https://inema.club). Use responsibly: removing a model’s guardrails doesn’t remove the law.