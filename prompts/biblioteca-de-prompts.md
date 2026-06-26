# 🔁 Biblioteca de Prompts Reutilizáveis

Coleção pronta para **estudar qualquer tema** no NotebookLM (ou em outro LLM). Substitua os
campos entre `{chaves}`. Todos os prompts seguem a receita:
**Papel + Tarefa + Contexto/Fonte + Formato + Restrições.**

> 🛡️ **Regra de ouro antialucinação:** quando o assunto exigir precisão, sempre termine com
> *"use somente as fontes deste notebook e cite o trecho; se não constar, escreva 'não consta'."*

---

## 🟢 1. Compreensão e resumo

```text
# RESUMO EXECUTIVO
Você é um professor didático. Resuma os conceitos centrais deste notebook em até 10 bullets,
do mais fundamental ao mais avançado. Responda em português do Brasil e cite a fonte de cada ponto.
```

```text
# EXPLIQUE PARA INICIANTES (ELI5)
Explique "{TEMA}" como se eu tivesse 12 anos, usando uma analogia do dia a dia, em até 5 linhas.
```

```text
# RESUMO EM 3 NÍVEIS
Explique "{TEMA}" em 3 níveis de profundidade: (1) uma frase, (2) um parágrafo, (3) técnico.
```

---

## 🔵 2. Aprofundamento

```text
# DESTRINCHAR UM CONCEITO
Explique "{CONCEITO}" em camadas: analogia → intuição → definição técnica → exemplo.
Baseie-se nas fontes e cite-as.
```

```text
# COMPARAÇÃO CRUZADA (PENSAMENTO CRÍTICO)
Compare como as fontes "{FONTE A}" e "{FONTE B}" tratam "{TEMA}". Onde concordam, onde
divergem e onde se complementam? Responda em tabela. Se uma fonte não cobrir, escreva "não consta".
```

```text
# PERGUNTAS SOCRÁTICAS
Faça-me 5 perguntas, da mais simples à mais difícil, que testem se eu realmente entendi "{TEMA}".
```

---

## 🟣 3. Geração de material de estudo

```text
# GLOSSÁRIO AUTOMÁTICO
Liste os 15 termos mais importantes deste notebook com definição de 1 linha cada, em ordem
alfabética. Se um termo não constar nas fontes, escreva "não consta".
```

```text
# QUIZ DE AUTOAVALIAÇÃO
Crie 5 questões de múltipla escolha (nível {iniciante/intermediário}) com distratores plausíveis
e gabarito comentado. Indique a fonte de cada questão.
```

```text
# FLASHCARDS
Gere 10 flashcards no formato "P: ... | R: ..." cobrindo os conceitos centrais deste notebook.
```

```text
# PLANO DE ESTUDOS
Com base nas fontes e no objetivo "{OBJETIVO}", monte um plano de estudos de {N} dias,
com tópicos por dia e uma tarefa prática ao final de cada dia.
```

---

## 🟠 4. Organização e conexões

```text
# MAPA DE CONEXÕES
Mostre como os principais conceitos deste notebook se conectam, em lista hierárquica
(tópico → subtópicos), apontando dependências entre eles.
```

```text
# LINHA DO TEMPO
Organize cronologicamente os marcos/ideias citados nas fontes, com 1 frase explicando a importância de cada um.
```

```text
# TABELA-RESUMO
Condense "{TEMA}" em uma tabela com colunas: Conceito | Definição | Exemplo | Fonte.
```

---

## 🔴 5. Revisão e verificação

```text
# CAÇADOR DE LACUNAS
Considerando os objetivos "{LISTA DE OBJETIVOS}", aponte quais tópicos as fontes cobrem mal
ou não cobrem e sugira o que estudar a seguir.
```

```text
# VERIFICAÇÃO ANTIALUCINAÇÃO
Responda "{PERGUNTA}" usando SOMENTE as fontes. Cite o trecho. Se a informação não estiver
nas fontes, responda exatamente "não consta nas fontes".
```

```text
# REVISÃO RELÂMPAGO (SPACED REPETITION)
Faça-me 5 perguntas rápidas sobre o que estudei aqui para revisão. Após eu responder
(na próxima mensagem), corrija e explique os erros citando a fonte.
```

---

## 🧩 Como usar bem

1. **Comece amplo, depois refine** (2–3 iterações por pergunta).
2. **Peça citações** sempre que precisar de precisão.
3. **Padronize o idioma:** adicione *"responda em português do Brasil"*.
4. **Salve as melhores respostas** como Notas no NotebookLM — elas viram novas fontes.
