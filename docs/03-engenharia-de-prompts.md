# 03 · Engenharia de Prompts e "Cicatrizes" (diário completo)

> Diário de bordo dos testes de prompt. Resumo no
> [README principal](../README.md#-3-engenharia-de-prompts-e-cicatrizes).

> 🟡 **PREENCHA COM SUA EXPERIÊNCIA REAL.** Abaixo há (A) um modelo realista já preenchido e
> (B) um **template em branco** para você registrar cada novo teste durante o estudo. O valor
> deste documento está na **honestidade do registro** — inclusive dos erros.

---

## A) Modelo realista (exemplo a adaptar)

### Caso 1 — Definir o conceito central (IA generativa vs. discriminativa)

| Campo | Conteúdo |
|-------|----------|
| **Objetivo** | O1 — diferenciar generativa de discriminativa |
| **Prompt v1** | `O que é IA Generativa?` |
| **Problema (cicatriz)** | Resposta genérica, longa, "de marketing", sem ancorar nas fontes |
| **Prompt v2** | `Você é um professor de IA. Apenas com base nas fontes deste notebook, explique a diferença entre IA generativa e discriminativa em até 5 linhas, com 1 exemplo de cada. Cite a fonte.` |
| **Resultado** | Resposta curta, comparativa e **com citação clicável** |
| **Lição** | Papel + escopo ("apenas com base nas fontes") + formato + limite de tamanho |
| **Resposta real** | _[cole aqui]_ |

### Caso 2 — Profundidade técnica (atenção)

| Campo | Conteúdo |
|-------|----------|
| **Objetivo** | O2 — entender self-attention |
| **Prompt v1** | `Explique o mecanismo de atenção.` |
| **Problema (cicatriz)** | Pulou direto para matrizes Q, K, V — sem intuição |
| **Prompt v2** | `Explique self-attention em 3 níveis: (1) analogia do dia a dia, (2) intuição, (3) termos técnicos Q/K/V. Baseie-se em F1 e F2.` |
| **Resultado** | A analogia destravou o entendimento antes dos termos técnicos |
| **Lição** | Pedir **analogia antes** da matemática |
| **Resposta real** | _[cole aqui]_ |

### Caso 3 — Comparar fontes (pensamento crítico)

| Campo | Conteúdo |
|-------|----------|
| **Objetivo** | O3 — etapas de treino |
| **Prompt** | `Compare como F3 e F4 descrevem as etapas de treino de um LLM. Onde concordam e se complementam? Em tabela. Se não constar, escreva "não consta".` |
| **Problema (cicatriz)** | A IA "preenchia lacunas" com conhecimento geral quando a fonte não cobria |
| **Lição** | Adicionar a trava `"se não constar, escreva 'não consta'"` |
| **Resposta real** | _[cole aqui]_ |

### Caso 4 — Gerar quiz (aplicação)

| Campo | Conteúdo |
|-------|----------|
| **Objetivo** | O1–O6 — autoavaliação |
| **Prompt** | `Crie 5 questões de múltipla escolha (iniciante) com distratores plausíveis e gabarito comentado. Indique a fonte.` |
| **Problema (cicatriz)** | Alternativas erradas óbvias demais |
| **Lição** | Pedir explicitamente **"distratores plausíveis"** |
| **Resposta real** | _[cole aqui]_ |

---

## B) Template em branco (copie para cada novo teste)

```text
### Caso N — <título>

- Objetivo: <O?>
- Prompt v1: <...>
- Problema / cicatriz: <o que deu errado?>
- Prompt v2 (ajuste): <...>
- Resultado: <melhorou? como?>
- Lição aprendida: <regra que vou reutilizar>
- Resposta real (resumo): <cole aqui>
- Print (opcional): ../assets/<arquivo>.png
```

---

## 🎓 Lições consolidadas (troubleshooting)

| Sintoma | Causa provável | Correção |
|---------|----------------|----------|
| Resposta genérica/longa | Prompt amplo demais | Adicionar papel, escopo, formato e limite |
| Excesso de matemática | Faltou pedir intuição | Pedir analogia antes dos termos técnicos |
| IA "inventa" (alucina) | Lacuna na fonte | Travar com "se não constar, escreva 'não consta'" + exigir citação |
| Quiz fraco | Critério ausente | Pedir "distratores plausíveis", nível e gabarito comentado |
| Saída em inglês | Idioma não especificado | Adicionar "responda em português do Brasil" |
