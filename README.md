# 🧠 Miniguia de Estudos com NotebookLM — IA Generativa e LLMs

> Caderno temático construído com **Inteligência Artificial como ferramenta de aprendizagem ativa**.
> Projeto prático do desafio **DIO** unindo *pensamento crítico*, *curadoria de fontes* e
> *engenharia de prompts* para transformar 5 fontes abertas em um guia de estudo reutilizável.

![Tema](https://img.shields.io/badge/tema-IA%20Generativa%20%26%20LLMs-6f42c1)
![Ferramenta](https://img.shields.io/badge/ferramenta-NotebookLM-1a73e8)
![Status](https://img.shields.io/badge/status-em%20construção-yellow)
![Licença](https://img.shields.io/badge/licença-MIT-green)
![Feito para](https://img.shields.io/badge/feito%20para-DIO-000000)

---

## 📑 Índice

1. [Sobre o projeto](#-sobre-o-projeto)
2. [Contexto e objetivos](#-1-contexto-e-objetivos)
3. [Curadoria de fontes](#-2-curadoria-de-fontes)
4. [Engenharia de prompts e "cicatrizes"](#-3-engenharia-de-prompts-e-cicatrizes)
5. [Miniguia de estudo (entrega final)](#-4-miniguia-de-estudo-entrega-final)
6. [Estrutura do repositório](#-estrutura-do-repositório)
7. [Como reproduzir este caderno](#-como-reproduzir-este-caderno-passo-a-passo)
8. [Próximos passos](#-próximos-passos)
9. [Licença e autoria](#-licença-e-autoria)

---

## 🎯 Sobre o projeto

Este repositório documenta um **Caderno Temático** criado no
[**NotebookLM**](https://notebooklm.google.com) — a ferramenta do Google que atua como um
"assistente de pesquisa" ancorado **exclusivamente nas fontes que você fornece**.

A proposta não é apenas "usar a IA", e sim **demonstrar o raciocínio** por trás do estudo:
quais fontes escolhi, **por que** as escolhi, quais perguntas fiz, o que deu certo, o que deu
errado (as *cicatrizes*) e como cheguei ao material final consolidado.

> 💡 **Por que esse tema?** Estudar *IA Generativa* **usando** uma ferramenta de IA é uma
> narrativa poderosa de portfólio: mostra que sei aprender um assunto novo **com** as próprias
> tecnologias que ele descreve.

---

## 📍 1. Contexto e Objetivos

### Assunto de interesse escolhido

**Fundamentos de IA Generativa e Grandes Modelos de Linguagem (LLMs).**

Escolhi este tema porque a IA Generativa deixou de ser tendência e virou **infraestrutura**:
está em assistentes de código, atendimento, busca e produtividade. Eu queria sair do uso
"mágico" da ferramenta e entender **o que acontece por baixo** — como um LLM representa
texto, como ele "decide" a próxima palavra e por que ele às vezes erra com confiança
(alucina).

### Objetivos de estudo

Defini objetivos **claros e verificáveis** (cada um vira uma seção do miniguia final):

| # | Objetivo | Como sei que atingi |
|---|----------|---------------------|
| O1 | Diferenciar **IA Generativa** de IA tradicional (discriminativa) | Consigo explicar com 1 exemplo de cada |
| O2 | Entender a arquitetura **Transformer** e o mecanismo de **atenção** | Consigo descrever o fluxo token → embedding → atenção → saída |
| O3 | Compreender as etapas de treino: **pré-treino → fine-tuning → RLHF** | Consigo dizer o que cada etapa adiciona ao modelo |
| O4 | Dominar o básico de **engenharia de prompt** (zero-shot, few-shot, chain-of-thought) | Tenho prompts reutilizáveis que funcionam |
| O5 | Entender **RAG** e por que ele reduz alucinação | Consigo explicar quando usar RAG vs. fine-tuning |
| O6 | Reconhecer **limitações e riscos** (alucinação, viés, corte de conhecimento) | Sei listar 5 limitações e como mitigá-las |

### Público e pré-requisitos

- **Público-alvo:** estudantes e devs iniciantes/intermediários em IA.
- **Pré-requisitos:** lógica de programação básica e curiosidade. **Não** exige matemática avançada.

---

## 📚 2. Curadoria de Fontes

Selecionei **5 fontes abertas, gratuitas e confiáveis**, equilibrando *teoria fundamental*
(papers), *didática visual* (artigos ilustrados) e *prática* (guias). Todas foram (ou serão)
**carregadas no NotebookLM** como base de conhecimento do caderno.

> ✅ **Critério de curadoria:** priorizei fontes (1) abertas/gratuitas, (2) de autoridade
> reconhecida, (3) com licença que permite uso (várias são *Creative Commons*) e
> (4) complementares entre si — da teoria ao uso prático.

| # | Fonte | Tipo | Licença | Por que escolhi |
|---|-------|------|---------|-----------------|
| F1 | [**Attention Is All You Need** (Vaswani et al., 2017)](https://arxiv.org/abs/1706.03762) | Paper (PDF) | arXiv (aberto) | O artigo que **criou o Transformer** — base de praticamente todo LLM moderno |
| F2 | [**The Illustrated Transformer** (Jay Alammar)](https://jalammar.github.io/illustrated-transformer/) | Artigo web | CC BY-NC-SA 4.0 | Explica o Transformer **visualmente**, traduzindo o paper F1 para iniciantes |
| F3 | [**A Survey of Large Language Models** (Zhao et al., 2023)](https://arxiv.org/abs/2303.18223) | Paper (PDF) | arXiv (aberto) | Visão **panorâmica** e atualizada de LLMs: treino, adaptação e avaliação |
| F4 | [**Introduction to LLMs — Google ML Crash Course**](https://developers.google.com/machine-learning/resources/intro-llms) | Curso/artigo | CC BY 4.0 | Fundamentos didáticos do Google, com exercícios — ótimo para fixar conceitos |
| F5 | [**Prompt Engineering Guide** (DAIR.AI)](https://www.promptingguide.ai/) | Guia web | Aberto (open-source) | Referência prática e mantida pela comunidade sobre **técnicas de prompt** |

> 📎 Os PDFs baixados e o detalhamento da curadoria estão em [`/fontes`](./fontes/README.md).
> Ao carregar no NotebookLM, prefira **colar o link** (F2, F4, F5) e **subir o PDF** (F1, F3).

> ⚠️ **Nota de integridade:** confirmei que os 5 links estavam ativos na data de publicação
> deste repositório. Sempre **revalide os links** e respeite as licenças antes de redistribuir
> qualquer material.

---

## 🧪 3. Engenharia de Prompts e "Cicatrizes"

Esta é a seção que mais **mostra raciocínio** — e a que o mercado mais valoriza. Aqui registro
as perguntas estratégicas, as **variações** que testei, as **respostas** obtidas e,
principalmente, as **dificuldades** (as *cicatrizes* / troubleshooting).

> 🧩 **Como li esta seção:** cada caso segue o padrão
> **Objetivo → Prompt v1 → Problema → Prompt v2 (ajuste) → Resultado → Lição.**

> 🟡 **AVISO IMPORTANTE — preencha com a SUA experiência real.**
> Os exemplos abaixo são um **modelo realista** para te guiar. Ao rodar no NotebookLM,
> **substitua** os trechos `> 📝 Resposta obtida (resumo):` pelas respostas reais que você
> receber, e ajuste as cicatrizes conforme as suas dificuldades. É exatamente esse registro
> honesto que diferencia um portfólio "nota 10".

### 🧭 Metodologia de teste

1. Comecei com um prompt **amplo** (zero-shot) e fui **estreitando** (refino iterativo).
2. Sempre pedi para a IA **citar a fonte/trecho** (o NotebookLM mostra as citações) — isso é
   minha principal defesa contra alucinação.
3. Para cada pergunta, testei **pelo menos 2 variações** e comparei qual respondeu melhor.

### Caso 1 — Definir o conceito central

- **Objetivo:** entender a diferença entre IA Generativa e IA discriminativa (Objetivo O1).
- **Prompt v1 (zero-shot, amplo):**
  > `O que é IA Generativa?`
- **🩹 Cicatriz:** a resposta veio **genérica e longa**, repetindo definições de marketing
  sem ancorar nas minhas fontes.
- **Prompt v2 (com papel + restrição + formato):**
  > `Você é um professor de IA. Com base apenas nas fontes deste notebook, explique a
  > diferença entre IA generativa e IA discriminativa em até 5 linhas, com 1 exemplo de cada.
  > Cite a fonte usada.`
- **✅ Resultado:** resposta curta, comparativa e **com citação** clicável.

> 📝 **Resposta obtida (resumo):** _[cole aqui o resumo da resposta real do NotebookLM]_

### Caso 2 — Forçar profundidade técnica (atenção/Transformer)

- **Objetivo:** entender o mecanismo de atenção (Objetivo O2).
- **Prompt v1:**
  > `Explique o mecanismo de atenção.`
- **🩹 Cicatriz:** a IA mergulhou direto em **matrizes Q, K, V** sem contexto — entendi as
  fórmulas, mas não a **intuição**.
- **Prompt v2 (pedindo analogia + progressão):**
  > `Explique o mecanismo de "self-attention" em 3 níveis: (1) uma analogia do dia a dia,
  > (2) a intuição (por que cada palavra "olha" para as outras), (3) os termos técnicos
  > Q, K e V. Baseie-se em "Attention Is All You Need" e no "Illustrated Transformer".`
- **✅ Resultado:** a camada de analogia destravou o entendimento; só então os termos técnicos
  fizeram sentido.

> 📝 **Resposta obtida (resumo):** _[cole aqui]_

### Caso 3 — Comparar fontes (pensamento crítico)

- **Objetivo:** ver se as fontes concordam sobre as etapas de treino (Objetivo O3).
- **Prompt (cross-source):**
  > `Compare como o "Survey of LLMs" e o material do Google descrevem as etapas de treino de
  > um LLM. Onde concordam e onde se complementam? Responda em tabela.`
- **🩹 Cicatriz:** quando uma fonte **não cobria** o assunto, a IA tendia a "preencher a
  lacuna" com conhecimento geral. **Solução:** adicionei a trava
  *"se uma fonte não mencionar, escreva 'não consta'"*.

> 📝 **Resposta obtida (resumo):** _[cole aqui]_

### Caso 4 — Gerar material de estudo (aplicação)

- **Objetivo:** produzir um quiz de autoavaliação (Objetivos O1–O6).
- **Prompt:**
  > `Crie 5 perguntas de múltipla escolha (com gabarito comentado) cobrindo os conceitos
  > centrais deste notebook, em nível iniciante. Para cada questão, indique a fonte.`
- **🩹 Cicatriz:** no início as alternativas erradas eram **óbvias demais**. Pedi
  *"distratores plausíveis"* e a qualidade do quiz subiu muito.

> 📝 **Resposta obtida (resumo):** _[cole aqui]_

### 📋 Tabela-resumo dos testes

| Pergunta estratégica | Técnica de prompt | Cicatriz / dificuldade | Como superei |
|----------------------|-------------------|------------------------|--------------|
| O que é IA Generativa? | Papel + restrição + formato | Resposta genérica de marketing | "Apenas com base nas fontes" + limite de linhas |
| Como funciona a atenção? | Analogia em camadas | Excesso de matemática sem intuição | Pedir analogia **antes** dos termos técnicos |
| As fontes concordam? | Cross-source + tabela | IA preenchia lacunas inventando | Trava "se não consta, escreva 'não consta'" |
| Quero um quiz | Geração + critério de qualidade | Distratores óbvios | Pedir "distratores plausíveis" |

### 🎓 Lições aprendidas (troubleshooting consolidado)

- **Especificidade vence:** papel + escopo + formato + tamanho transforma a resposta.
- **Cite sempre a fonte:** no NotebookLM, exigir citação reduz drasticamente a alucinação.
- **Trave as lacunas:** instruir "se não consta, diga 'não consta'" evita invenção.
- **Itere:** o primeiro prompt raramente é o melhor — refine em 2–3 rodadas.
- **Idioma:** peça explicitamente **"responda em português do Brasil"** para padronizar a saída.

---

## 📖 4. Miniguia de Estudo (Entrega Final)

Resultado consolidado do estudo: **resumos estruturados**, **glossário** e
**prompts reutilizáveis**. Versões expandidas em
[`/docs/04-miniguia-final.md`](./docs/04-miniguia-final.md) e
[`/prompts/biblioteca-de-prompts.md`](./prompts/biblioteca-de-prompts.md).

### 4.1 📝 Resumos estruturados

#### A) IA Generativa vs. IA Discriminativa
- **IA discriminativa** aprende **fronteiras** para *classificar/prever* (ex.: "este e-mail é
  spam?"). Responde **rótulos**.
- **IA generativa** aprende a **distribuição dos dados** para *criar* conteúdo novo (texto,
  imagem, código). Responde **conteúdo inédito**.
- **Resumo de bolso:** discriminativa *separa*; generativa *cria*.

#### B) O que é um LLM e como ele "pensa"
- Um **LLM** (Large Language Model) é uma rede neural treinada para **prever o próximo token**
  dado o contexto anterior. Gerar texto = repetir essa previsão, token a token.
- O texto é quebrado em **tokens** (pedaços de palavra) e convertido em **embeddings** (vetores
  numéricos que capturam significado). Palavras de sentido próximo ficam próximas no espaço vetorial.
- **Parâmetros (pesos)** são os "botões" ajustados no treino; bilhões deles armazenam o
  conhecimento estatístico da linguagem.

#### C) A arquitetura Transformer e a atenção
- O **Transformer** (paper F1, 2017) substituiu redes recorrentes e permitiu **paralelizar** o
  treino — destravando a escala dos LLMs atuais.
- O mecanismo de **self-attention** deixa cada token "olhar" para todos os outros e **pesar** quais
  são mais relevantes para o contexto (ex.: ligar "ele" ao substantivo certo na frase).
- Modelos como o GPT são **decoder-only**: ótimos para *gerar* texto continuando o contexto.

#### D) Como um LLM é treinado
1. **Pré-treinamento:** lê enormes volumes de texto e aprende a prever o próximo token (conhecimento geral).
2. **Fine-tuning (ajuste fino):** especializa o modelo em uma tarefa/domínio com dados focados.
3. **RLHF** (*Reinforcement Learning from Human Feedback*): humanos avaliam respostas e o modelo
   é ajustado para ser mais **útil, honesto e seguro** — é o que torna o chat "alinhado".

#### E) Engenharia de Prompt (o essencial)
- **Zero-shot:** pedir direto, sem exemplos.
- **Few-shot:** dar **alguns exemplos** no prompt para guiar o formato/estilo.
- **Chain-of-Thought (CoT):** pedir para a IA **"pensar passo a passo"** — melhora raciocínio
  em problemas com várias etapas.
- **Receita prática:** `Papel + Tarefa + Contexto/Fonte + Formato + Restrições`.

#### F) RAG — Retrieval-Augmented Generation
- **RAG** = buscar trechos relevantes em uma base de documentos e **injetá-los no prompt** antes
  de o modelo responder. É, em essência, **o que o NotebookLM faz** com as suas fontes.
- **Vantagem:** respostas ancoradas em fontes → **menos alucinação** e citações verificáveis.
- **RAG vs. fine-tuning:** use **RAG** para *conhecimento que muda/precisa de citação*; use
  **fine-tuning** para *comportamento/estilo* consistente.

#### G) Limitações e riscos
- **Alucinação:** afirmar algo falso com confiança. *Mitigação:* RAG + exigir citações.
- **Viés:** reproduz vieses dos dados de treino. *Mitigação:* curadoria e revisão humana.
- **Corte de conhecimento:** não sabe de fatos após a data de treino. *Mitigação:* RAG/busca.
- **Janela de contexto:** há um limite de tokens por interação. *Mitigação:* resumir/dividir.
- **Custo/latência:** modelos grandes são caros. *Mitigação:* escolher o modelo certo p/ a tarefa.

### 4.2 📒 Glossário

| Termo | Definição curta |
|-------|-----------------|
| **Token** | Menor unidade de texto processada pelo modelo (≈ pedaço de palavra) |
| **Tokenização** | Processo de quebrar texto em tokens |
| **Embedding** | Representação vetorial (numérica) do significado de um token/texto |
| **Transformer** | Arquitetura de rede neural baseada em atenção; base dos LLMs |
| **Self-Attention** | Mecanismo em que cada token pondera a relevância dos demais |
| **Parâmetros (pesos)** | Valores ajustados no treino que armazenam o "conhecimento" do modelo |
| **Pré-treinamento** | Fase em que o modelo aprende linguagem prevendo o próximo token |
| **Fine-tuning** | Ajuste do modelo a uma tarefa/domínio específico |
| **RLHF** | Ajuste com feedback humano para alinhar utilidade e segurança |
| **Prompt** | Instrução/entrada de texto enviada ao modelo |
| **Zero-shot** | Pedir uma tarefa sem fornecer exemplos |
| **Few-shot** | Fornecer alguns exemplos no prompt para guiar a resposta |
| **Chain-of-Thought** | Pedir raciocínio passo a passo para melhorar a resposta |
| **Temperatura** | Hiperparâmetro que controla a aleatoriedade/criatividade da saída |
| **Janela de contexto** | Quantidade máxima de tokens que o modelo considera por vez |
| **Alucinação** | Resposta falsa apresentada como verdadeira |
| **RAG** | Gerar respostas ancoradas em documentos recuperados de uma base |
| **Inferência** | Ato de usar um modelo já treinado para gerar uma resposta |
| **Foundation Model** | Modelo grande e genérico, base para múltiplas aplicações |
| **Multimodal** | Modelo que lida com mais de um tipo de dado (texto, imagem, áudio) |

### 4.3 🔁 Prompts reutilizáveis

Conjunto pronto para **revisar este (ou qualquer) tema** no NotebookLM. Biblioteca completa em
[`/prompts/biblioteca-de-prompts.md`](./prompts/biblioteca-de-prompts.md).

```text
# 1. RESUMO EXECUTIVO
Resuma os conceitos centrais deste notebook em até 10 bullets, do mais fundamental
ao mais avançado. Responda em português do Brasil e cite a fonte de cada ponto.

# 2. EXPLIQUE COMO SE EU TIVESSE 12 ANOS (ELI5)
Explique o conceito de "{TEMA}" usando uma analogia simples do dia a dia, em até 5 linhas.

# 3. GLOSSÁRIO AUTOMÁTICO
Liste os 15 termos mais importantes deste notebook com uma definição de 1 linha cada,
em ordem alfabética. Se um termo não constar nas fontes, escreva "não consta".

# 4. QUIZ DE AUTOAVALIAÇÃO
Crie 5 questões de múltipla escolha (nível iniciante) com distratores plausíveis
e gabarito comentado. Indique a fonte de cada questão.

# 5. MAPA DE CONEXÕES
Mostre como os principais conceitos deste notebook se conectam, em formato de
lista hierárquica (tópico → subtópicos). Aponte dependências entre eles.

# 6. CAÇADOR DE LACUNAS
Com base nos meus objetivos de estudo, aponte quais tópicos as fontes cobrem mal
ou não cobrem, e sugira o que eu deveria estudar a seguir.

# 7. FLASHCARDS (PERGUNTA/RESPOSTA)
Gere 10 flashcards no formato "P: ... | R: ..." cobrindo os conceitos centrais.

# 8. VERIFICAÇÃO ANTIALUCINAÇÃO
Responda à pergunta "{PERGUNTA}" usando SOMENTE as fontes. Cite o trecho. Se a
informação não estiver nas fontes, responda exatamente "não consta nas fontes".
```

---

## 🗂️ Estrutura do repositório

```
miniguia-estudos-notebooklm/
├── README.md                       # 👈 Você está aqui (entrega principal e completa)
├── PASSO-A-PASSO.md                # Guia prático para montar o caderno no NotebookLM
├── LICENSE                         # Licença MIT
├── .gitignore                      # Ignora temporários, OS e PDFs pesados (opcional)
├── docs/
│   ├── 01-contexto-e-objetivos.md  # Versão expandida do contexto e objetivos
│   ├── 02-curadoria-de-fontes.md   # Detalhe da curadoria e critérios
│   ├── 03-engenharia-de-prompts.md # Diário completo de testes e cicatrizes
│   └── 04-miniguia-final.md         # Miniguia consolidado e expandido
├── fontes/
│   └── README.md                   # Lista de fontes + onde colocar os PDFs baixados
├── prompts/
│   └── biblioteca-de-prompts.md    # Biblioteca completa de prompts reutilizáveis
└── assets/
    └── README.md                   # Onde colocar prints do NotebookLM (evidências)
```

---

## 🚀 Como reproduzir este caderno (passo a passo)

> 📋 Versão detalhada e à prova de erro (com os links prontos para copiar): **[PASSO-A-PASSO.md](./PASSO-A-PASSO.md)**.

1. **Acesse** o [NotebookLM](https://notebooklm.google.com) e faça login com sua Conta Google.
2. Clique em **"Novo notebook"** e dê um nome (ex.: *"IA Generativa e LLMs"*).
3. **Adicione as fontes** (botão *Adicionar fontes*):
   - Cole os **links** de F2, F4 e F5.
   - Faça **upload dos PDFs** de F1 e F3 (baixe-os do arXiv — veja [`/fontes`](./fontes/README.md)).
4. Aguarde o NotebookLM **indexar** as fontes.
5. Rode os **prompts reutilizáveis** (seção 4.3) e registre as respostas.
6. Para cada teste relevante, **tire um print** e salve em [`/assets`](./assets/) como evidência.
7. **Substitua** no README os marcadores `📝 Resposta obtida` pelos resultados reais.
8. Explore os recursos do NotebookLM: **Resumo**, **Perguntas sugeridas**, **Mapa mental** e o
   **Áudio Overview** (podcast gerado a partir das suas fontes) — ótimo para revisão.

> 💡 **Dica de ouro:** salve as melhores respostas como **Notas** dentro do próprio NotebookLM.
> Elas viram novas "fontes" e enriquecem as próximas perguntas.

---

## 📌 Próximos passos

- [ ] Carregar as 5 fontes no NotebookLM e indexar.
- [ ] Rodar os 8 prompts reutilizáveis e colar as respostas reais.
- [ ] Substituir os marcadores `📝 Resposta obtida` pelas saídas reais.
- [ ] Adicionar prints das evidências em `/assets`.
- [ ] Gerar o **Áudio Overview** e linká-lo aqui.
- [ ] Expandir o glossário com 5 termos que surgirem durante o estudo.
- [ ] (Opcional) Criar um 2º caderno temático sobre **Agentes de IA / RAG avançado**.

---

## 📄 Licença e Autoria

Distribuído sob a **Licença MIT** — veja [LICENSE](./LICENSE).
O conteúdo das fontes externas pertence aos seus respectivos autores; respeite as licenças citadas.

**Autor:** Thiago Miranda · [GitHub](https://github.com/thiagomirandahs) · feito com 💜 para a [DIO](https://www.dio.me)

> _Caderno temático criado como parte do desafio de projeto da DIO sobre uso de IA como
> ferramenta de aprendizagem ativa._
