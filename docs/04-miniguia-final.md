# 04 · Miniguia de Estudo (versão expandida)

> Entrega final consolidada: **resumos**, **glossário** e **prompts reutilizáveis**.
> Versão enxuta no [README principal](../README.md#-4-miniguia-de-estudo-entrega-final).

---

## 4.1 📝 Resumos estruturados

### A) IA Generativa vs. Discriminativa
- **Discriminativa:** aprende fronteiras para **classificar/prever** (ex.: spam ou não-spam).
- **Generativa:** aprende a distribuição dos dados para **criar** conteúdo novo (texto, imagem, código).
- **De bolso:** *discriminativa separa; generativa cria.*

### B) LLM e a previsão do próximo token
- Um **LLM** prevê o **próximo token** dado o contexto. Gerar texto = repetir essa previsão.
- **Token** → pedaço de palavra; **Embedding** → vetor que captura significado.
- **Parâmetros (pesos):** os "botões" ajustados no treino; armazenam o conhecimento estatístico.

### C) Transformer e atenção
- O **Transformer** (2017) dispensou a recorrência e permitiu **paralelizar** o treino → escala.
- **Self-attention:** cada token pondera a relevância dos demais (resolve referências, contexto).
- **Q, K, V (Query, Key, Value):** a query de um token "consulta" as keys dos outros; os values
  relevantes são combinados conforme o peso da atenção.
- LLMs de geração (tipo GPT) são **decoder-only**.

### D) Etapas de treino
1. **Pré-treinamento** — prever o próximo token em grandes corpora → conhecimento geral.
2. **Fine-tuning** — especializar em tarefa/domínio com dados focados.
3. **RLHF** — feedback humano alinha o modelo a respostas úteis, honestas e seguras.

### E) Engenharia de prompt
- **Zero-shot:** sem exemplos. **Few-shot:** com exemplos no prompt.
- **Chain-of-Thought:** "pense passo a passo" → melhora raciocínio multi-etapa.
- **Receita:** `Papel + Tarefa + Contexto/Fonte + Formato + Restrições`.
- **Temperatura:** controla aleatoriedade (baixa = mais determinístico; alta = mais criativo).

### F) RAG (Retrieval-Augmented Generation)
- Busca trechos relevantes numa base e os **injeta no prompt** antes de responder.
- É, na prática, **o que o NotebookLM faz** com as suas fontes.
- **Vantagem:** ancora a resposta → menos alucinação + citações verificáveis.
- **RAG vs. fine-tuning:** RAG para *conhecimento que muda/precisa citar*; fine-tuning para
  *comportamento/estilo* consistente.

### G) Limitações e riscos
| Risco | O que é | Mitigação |
|-------|---------|-----------|
| Alucinação | Afirmar falso com confiança | RAG + exigir citação |
| Viés | Reproduz vieses dos dados | Curadoria + revisão humana |
| Corte de conhecimento | Não sabe de fatos recentes | RAG / busca |
| Janela de contexto | Limite de tokens | Resumir / dividir |
| Custo e latência | Modelos grandes são caros | Escolher o modelo certo |

---

## 4.2 📒 Glossário (expandido)

| Termo | Definição |
|-------|-----------|
| **Token** | Menor unidade de texto processada (≈ pedaço de palavra) |
| **Tokenização** | Quebra do texto em tokens |
| **Embedding** | Vetor numérico que representa significado |
| **Espaço vetorial** | "Mapa" onde itens de sentido próximo ficam próximos |
| **Transformer** | Arquitetura baseada em atenção; base dos LLMs |
| **Self-Attention** | Cada token pondera a relevância dos demais |
| **Q, K, V** | Query, Key, Value — componentes do cálculo de atenção |
| **Parâmetros (pesos)** | Valores ajustados no treino que guardam o "conhecimento" |
| **Pré-treinamento** | Aprender linguagem prevendo o próximo token |
| **Fine-tuning** | Ajuste a uma tarefa/domínio específico |
| **RLHF** | Ajuste com feedback humano para alinhamento |
| **Prompt** | Instrução/entrada enviada ao modelo |
| **Zero-shot / Few-shot** | Sem exemplos / com poucos exemplos no prompt |
| **Chain-of-Thought** | Raciocínio passo a passo |
| **Temperatura** | Controla a aleatoriedade da saída |
| **Janela de contexto** | Máximo de tokens considerados por vez |
| **Alucinação** | Resposta falsa apresentada como verdadeira |
| **RAG** | Geração ancorada em documentos recuperados |
| **Inferência** | Usar um modelo treinado para gerar resposta |
| **Foundation Model** | Modelo genérico que serve de base a várias aplicações |
| **Multimodal** | Lida com mais de um tipo de dado (texto, imagem, áudio) |
| **Decoder-only** | Arquitetura focada em gerar texto (ex.: GPT) |

---

## 4.3 🔁 Prompts reutilizáveis

Os 8 prompts essenciais estão no [README](../README.md#43--prompts-reutilizáveis) e a
**biblioteca completa** (16+ prompts categorizados) em
[`/prompts/biblioteca-de-prompts.md`](../prompts/biblioteca-de-prompts.md).

> 🔑 Use sempre: *"responda em português do Brasil, use somente as fontes e cite o trecho;
> se não constar, escreva 'não consta'."*
