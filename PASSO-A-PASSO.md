# 🧭 Passo a Passo — Montar o Caderno no NotebookLM

Guia prático para criar o caderno temático **"IA Generativa e LLMs"** no NotebookLM e
preencher este repositório com os **resultados reais**. Tempo estimado: 20–30 min.

> Pré-requisito: estar logado no [NotebookLM](https://notebooklm.google.com) com sua Conta Google.

---

## Etapa 1 — Criar o notebook

1. Acesse **notebooklm.google.com**.
2. Clique em **"Criar novo"** (canto superior direito) ou **"Criar novo notebook"**.
3. Um notebook vazio abre já com o painel **"Adicionar fontes"**.

## Etapa 2 — Adicionar as 5 fontes

1. No painel de fontes, clique em **"Sites"**.
2. No campo **"Cole os links"**, cole as 5 URLs abaixo (pode colar todas de uma vez):

```
https://arxiv.org/abs/1706.03762
https://jalammar.github.io/illustrated-transformer/
https://arxiv.org/abs/2303.18223
https://developers.google.com/machine-learning/resources/intro-llms
https://www.promptingguide.ai/
```

3. Clique em **"Inserir"** e aguarde o NotebookLM **processar/indexar** cada fonte.

> 💡 **Sobre os papers (F1 e F3):** pela página `/abs/` o NotebookLM importa o **resumo
> (abstract)**. Se quiser o **texto completo**, baixe o PDF no arXiv (botão *View PDF*) e use
> **"Enviar arquivos"** em vez de "Sites". Veja [`/fontes`](./fontes/README.md).

## Etapa 3 — Renomear o notebook

- Clique no título **"Notebook sem título"** (canto superior esquerdo) e troque para
  **`IA Generativa e LLMs`**.

## Etapa 4 — Rodar os prompts

No campo **"Comece a digitar..."** (rodapé central), cole **um prompt por vez** e tecle Enter.
Comece por estes 6 (biblioteca completa em [`/prompts`](./prompts/biblioteca-de-prompts.md)):

```text
1) Você é um professor didático. Resuma os conceitos centrais deste notebook em até 10
   bullets, do mais fundamental ao mais avançado. Responda em português do Brasil e cite a
   fonte de cada ponto.

2) Liste os 15 termos mais importantes deste notebook com uma definição de 1 linha cada,
   em ordem alfabética. Se um termo não constar nas fontes, escreva "não consta".

3) Explique "self-attention" em 3 níveis: (1) uma analogia do dia a dia, (2) a intuição,
   (3) os termos técnicos Q, K e V. Baseie-se em "Attention Is All You Need" e no
   "Illustrated Transformer".

4) Compare como o "Survey of LLMs" e o material do Google descrevem as etapas de treino de
   um LLM. Onde concordam e onde se complementam? Responda em tabela. Se não constar,
   escreva "não consta".

5) Crie 5 questões de múltipla escolha (nível iniciante) com distratores plausíveis e
   gabarito comentado. Indique a fonte de cada questão.

6) Responda "O que é RAG e por que reduz alucinação?" usando SOMENTE as fontes. Cite o
   trecho. Se não estiver nas fontes, responda "não consta nas fontes".
```

## Etapa 5 — Capturar as respostas reais

Para cada prompt, **copie a resposta** do NotebookLM e cole no lugar certo:

- No [`README.md`](./README.md), seção **3** → substitua os marcadores
  `📝 Resposta obtida (resumo): [cole aqui]`.
- No [`docs/03-engenharia-de-prompts.md`](./docs/03-engenharia-de-prompts.md) → campos
  `Resposta real`.

> ✍️ Registre também as **dificuldades** ("cicatrizes"): o que o prompt v1 errou, o que você
> ajustou. **É isso que faz o projeto ser "nota 10".**

## Etapa 6 — Tirar prints (evidências)

Capture e salve em [`/assets`](./assets/):
- O notebook **com as 5 fontes** carregadas.
- Uma **resposta com citação** (mostrando a fonte clicável).

No README, referencie assim:
```markdown
![Notebook com as 5 fontes](./assets/notebook-com-fontes.png)
```

## Etapa 7 — Atualizar o GitHub

```bash
cd "E:/SKILLS COPILOT/miniguia-estudos-notebooklm"
git add .
git commit -m "docs: adiciona respostas reais do NotebookLM e evidencias"
git push
```

---

## ⭐ Bônus do NotebookLM (vale muito no portfólio)

No painel **"Estúdio"** (direita), gere e depois mencione no README:
- **Resumo em Áudio** (um *podcast* gerado a partir das suas fontes);
- **Mapa mental**;
- **Guia de estudo** / **Cartões** (flashcards) / **Teste**.

Pronto! Com as respostas reais coladas e os prints adicionados, seu caderno temático fica
completo e original. 🎉
