# 02 · Curadoria de Fontes (versão expandida)

> Fichas detalhadas de cada fonte. Lista resumida no
> [README principal](../README.md#-2-curadoria-de-fontes) e instruções de upload em
> [`/fontes`](../fontes/README.md).

## 🧮 Como avaliei cada fonte

Pontuei (1–3) em 4 critérios: **Acesso aberto**, **Autoridade**, **Licença** e **Complementaridade**.
Só entraram fontes com nota alta nos quatro.

---

## 📄 F1 — Attention Is All You Need (2017)

- **Link:** https://arxiv.org/abs/1706.03762
- **Autores:** Vaswani, Shazeer, Parmar, Uszkoreit, Jones, Gomez, Kaiser, Polosukhin (Google).
- **Tipo / Licença:** Paper · arXiv (acesso aberto).
- **Por que escolhi:** é **o** artigo que introduziu a arquitetura Transformer — fundamento de
  praticamente todos os LLMs atuais. Fonte primária e indispensável.
- **O que extrair:** a ideia de *self-attention* e por que dispensar recorrência permitiu escala.

## 🎨 F2 — The Illustrated Transformer

- **Link:** https://jalammar.github.io/illustrated-transformer/
- **Autor:** Jay Alammar.
- **Tipo / Licença:** Artigo web · CC BY-NC-SA 4.0.
- **Por que escolhi:** traduz o paper F1 em **explicação visual** acessível. Perfeito par
  "teoria (F1) + didática (F2)".
- **O que extrair:** a intuição visual de Q, K, V e do fluxo de atenção.

## 📚 F3 — A Survey of Large Language Models (2023)

- **Link:** https://arxiv.org/abs/2303.18223
- **Autores:** Zhao, Zhou et al. (21 autores).
- **Tipo / Licença:** Paper extenso (survey) · arXiv (acesso aberto).
- **Por que escolhi:** dá a **visão panorâmica e atualizada** — pré-treino, adaptação, uso e
  avaliação de LLMs. Ótimo para conectar conceitos.
- **O que extrair:** taxonomia das etapas de treino e capacidades emergentes.
- **Atenção:** é longo (100+ páginas) — use o NotebookLM para resumir capítulos específicos.

## 🟦 F4 — Introduction to LLMs (Google ML Crash Course)

- **Link:** https://developers.google.com/machine-learning/resources/intro-llms
- **Autor/Instituição:** Google.
- **Tipo / Licença:** Curso/artigo · CC BY 4.0.
- **Por que escolhi:** material **didático e estruturado**, com exercícios — excelente porta de entrada.
- **O que extrair:** fundamentos de modelos de linguagem, contexto e tokens.

## 🛠️ F5 — Prompt Engineering Guide (DAIR.AI)

- **Link:** https://www.promptingguide.ai/
- **Autor/Instituição:** DAIR.AI + comunidade.
- **Tipo / Licença:** Guia web open-source.
- **Por que escolhi:** referência **prática** e mantida sobre técnicas de prompt
  (zero-shot, few-shot, CoT).
- **O que extrair:** padrões de prompt que viram a base da [biblioteca reutilizável](../prompts/biblioteca-de-prompts.md).

---

## 🧩 Mapa de complementaridade

| Necessidade | Fonte principal | Complemento |
|-------------|-----------------|-------------|
| Fundamento teórico (Transformer) | F1 | F2 (visual) |
| Panorama / etapas de treino | F3 | F4 (didático) |
| Prática de prompt | F5 | — |

> 🔎 **Conclusão da curadoria:** o conjunto cobre **teoria → intuição → panorama → prática**,
> evitando depender de uma única perspectiva.
