# 01 · Contexto e Objetivos (versão expandida)

> Detalhamento do **porquê** deste caderno temático. Versão resumida no
> [README principal](../README.md#-1-contexto-e-objetivos).

## 🎯 Tema escolhido

**Fundamentos de IA Generativa e Grandes Modelos de Linguagem (LLMs).**

## 💬 Motivação

Eu já usava ferramentas de IA generativa no dia a dia, mas de forma "mágica" — sem entender
o que acontece por dentro. Quis fechar essa lacuna e construir uma **base conceitual sólida**,
que me permita: (1) usar as ferramentas com mais critério, (2) conversar com propriedade sobre
o tema em entrevistas e (3) ter fundamento para evoluir para tópicos avançados (RAG, agentes).

## 🧭 Escopo

**Dentro do escopo:**
- O que é IA generativa e como difere da IA discriminativa.
- Como LLMs representam e geram texto (tokens, embeddings, próximo token).
- Arquitetura Transformer e mecanismo de atenção (visão conceitual).
- Etapas de treino (pré-treino, fine-tuning, RLHF).
- Engenharia de prompt e RAG (fundamentos práticos).
- Limitações e riscos (alucinação, viés, contexto).

**Fora do escopo (por enquanto):**
- Implementar um Transformer do zero / matemática pesada de gradientes.
- Treinar ou fazer fine-tuning de modelos na prática.
- Comparação comercial entre provedores de modelos.

## ✅ Objetivos de estudo (detalhados)

| # | Objetivo | Resultado esperado | Evidência |
|---|----------|--------------------|-----------|
| O1 | Diferenciar IA generativa de discriminativa | Explicar com 1 exemplo de cada | Resumo A do miniguia |
| O2 | Entender Transformer e atenção | Descrever o fluxo token→saída | Resumo C + quiz |
| O3 | Mapear etapas de treino | Explicar o que cada etapa adiciona | Resumo D |
| O4 | Aplicar engenharia de prompt | Ter prompts reutilizáveis que funcionam | Biblioteca de prompts |
| O5 | Compreender RAG | Saber quando usar RAG vs. fine-tuning | Resumo F |
| O6 | Reconhecer limitações | Listar 5 riscos e mitigações | Resumo G |

## ⏱️ Plano de estudo sugerido (4 dias)

| Dia | Foco | Fontes | Entregável |
|-----|------|--------|------------|
| 1 | Panorama + generativa vs. discriminativa | F4, F3 | Resumos A e B |
| 2 | Transformer e atenção | F1, F2 | Resumo C + 1 print |
| 3 | Treino + engenharia de prompt | F3, F5 | Resumos D e E |
| 4 | RAG, limitações e revisão | F3, F5 | Resumos F e G + quiz |

## 🙋 Público-alvo e pré-requisitos

- **Público:** iniciantes e devs em transição para IA.
- **Pré-requisitos:** lógica de programação básica; **não** exige cálculo/álgebra avançada.
