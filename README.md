# provedores-semcensura

[![IA sem censura: onde usar, quanto custa e o que conferir](guia/assets/banner.jpg)](https://inematds.github.io/provedores-semcensura/guia/)

**🇧🇷 [Português](README.md) · 🇺🇸 [English](README.en.md) · 🇪🇸 [Español](README.es.md)**

## O que é

Este guia mostra onde encontrar modelos de IA “sem censura”, ou seja, versões que não recusam pedidos. Serve para quem testa a segurança do próprio sistema, pesquisa ou só quer um assistente que não trave em assunto delicado. Você vê numa tabela os provedores por API, por chat, por GPU alugada e no seu próprio computador, com preço, privacidade declarada e se pedem identidade. Para usar, basta ler; os exemplos pedem uma conta no provedor escolhido ou o Ollama instalado.

## 📖 Guia de uso

Guia completo (landing + passo a passo): **https://inematds.github.io/provedores-semcensura/guia/**

## O que tem no guia

- Diferença entre **uncensored** (fine-tune, tipo Dolphin), **abliterated** (remove a “direção de recusa” dos pesos, sem treinar) e **jailbroken** (prompt que engana as regras), e o que se perde sem a trava.
- Como achar esses modelos no Hugging Face.
- Tabela comparativa: Venice, abliteration.ai, orcarouter (Ollama), OpenRouter, Featherless, RunPod e local com Ollama — tipo, modelos, preço (conferido em 09/11/2026), identidade, privacidade declarada, compatibilidade OpenAI.
- “Qual escolher” por situação.
- Passo a passo: Venice pela API compatível com OpenAI, modelo local com Ollama, e ligar num harness de agente.
- Para onde vão os seus dados e uso responsável.

Nada aqui foi testado com conta ou chave: os fatos vêm das páginas públicas dos provedores; o que não deu para confirmar aparece como “não confirmado”.

## O processo, do início ao fim

Legenda: 🧠 sessão com o Nei · ⚙️ script · 🤖 `claude -p` / agente

1. 🧠 **Pesquisa** das páginas públicas dos provedores (só leitura, sem conta nem API) → `~/projetos/output/provedores-semcensura/PESQUISA.md`, com o que não foi confirmado.
2. ⚙️ **Capa** do catálogo + arte crua da hero: `node ~/.claude/skills/capa-inema/assets/gerar-capa.cjs --repo . --title "Provedores de IA sem censura" --cat "IA" --save-raw guia/assets/hero.png --gerador auto` → `capa/capa.png`.
3. ⚙️ **Banners** (Codex image_gen pela assinatura), 2 estilos × 3 idiomas: `bash ~/.claude/skills/projetos-landing-guia/assets/gerar-banner.sh --repo . --title "IA SEM CENSURA" --destaque "CENSURA" ...` (`--estilo grade --saida banner-grade`, `--lang en|es --saida banner-en|banner-es`...). Conferir o texto desenhado.
4. 🧠 **Guia PT** em `guia/index.html` (skill `projetos-landing-guia`), só com fatos da pesquisa.
5. 🤖 **Tradução** EN/ES pelo tradutor central: `inema-traduz -o out-en.html < prompt-en.txt` → `guia/en/index.html` e `guia/es/index.html`.
6. 🤖 **Revisão independente** por outro agente (persona de quem nunca viu o projeto).
7. ⚙️ **Publicar**: `git push` → GitHub Actions (`.github/workflows/pages.yml`) publica no Pages; conferir 200 em `/guia/`, `/guia/en/`, `/guia/es/`.
8. 🧠 **Atualizar preços**: refazer o passo 1 e trocar a data “conferido em” no guia e nos READMEs.

## Relacionados no INEMA

- [IA privada em 3 níveis](https://inematds.github.io/ia-privada-3-niveis/guia/)
- [IA sem censura defensiva](https://inematds.github.io/ia-sem-censura-defensiva/guia/)

---

Conteúdo aberto do [INEMA.CLUB](https://inema.club). Use com responsabilidade: tirar a trava do modelo não tira a lei.
