---
title: Análise de modos de falha (FMEA)
tags: [metodologia, confiabilidade]
fontes: [IEC 60812:2018 (FMEA), AIAG e VDA FMEA Handbook (2019), Pahl, Beitz, Feldhusen e Grote Projeto na Engenharia (cap. de avaliação de riscos e falhas), Kardec e Nascif Manutenção: Função Estratégica (caps. de confiabilidade e análise de falhas)]
status: rascunho
---

**Resumo:** a FMEA (análise dos modos de falha e seus efeitos) examina, componente por componente ou função por função, como o sistema pode falhar, quais as consequências, quais as causas e como a falha é prevenida ou detectada. Prioriza ações de melhoria antes que as falhas aconteçam. Complementa a análise de falhas reais (análise de causa raiz) feita depois que algo quebra.

## O que é

### Estrutura de uma FMEA

| Coluna | Pergunta |
|---|---|
| Item / função | O que o componente deve fazer? |
| **Modo de falha** | Como ele pode deixar de cumprir a função? (quebra, desgaste, vazamento, travamento) |
| **Efeito** | Qual a consequência para o sistema, a segurança, a produção? |
| **Severidade (S)** | Quão grave é o efeito? (1 a 10) |
| **Causa** | Por que o modo de falha ocorreria? |
| **Ocorrência (O)** | Qual a probabilidade dessa causa? (1 a 10) |
| **Controles atuais** | O que previne ou detecta hoje? |
| **Detecção (D)** | Quão provável é detectar antes de causar o efeito? (1 = detecta certamente; 10 = não detecta) |
| **Prioridade** | RPN ou AP |
| **Ações recomendadas** | O que fazer, quem, quando |

### Priorização

- **RPN (número de prioridade de risco):** $RPN = S \times O \times D$ (de 1 a 1000). Método tradicional.
- **AP (prioridade de ação):** introduzido no manual AIAG-VDA de 2019; usa tabelas que dão mais peso à severidade, porque um RPN igual pode esconder uma severidade 10 com baixa ocorrência. ⚠️ verificar as tabelas no manual.

**Regra prática:** qualquer item com **severidade 9 ou 10** (segurança, falha catastrófica) exige ação, independentemente do RPN.

### Tipos

- **FMEA de projeto (DFMEA):** falhas decorrentes do projeto (dimensionamento, material, tolerâncias).
- **FMEA de processo (PFMEA):** falhas de fabricação e montagem.
- **FMECA:** acrescenta a análise de criticidade (muito usada em manutenção).

### Relação com a análise de falhas reais

Depois que uma peça quebra, a **análise de causa raiz** (5 porquês, diagrama de Ishikawa, análise da superfície de fratura) identifica a causa. Os aprendizados devem **alimentar a FMEA** e os padrões de projeto, para que a mesma falha não se repita em outros equipamentos.

## Por que importa no projeto

- **Antecipar falhas** de equipamentos críticos, onde uma parada custa muito.
- **Priorizar** onde investir: material melhor, redundância, monitoramento (vibração, temperatura), inspeção.
- **Justificar** decisões de projeto e de estoque de sobressalentes críticos.

## Como aplicar (passo a passo / regras práticas)

1. **Monte a equipe** (projeto, manutenção, operação).
2. **Divida o sistema** em itens ou funções.
3. **Liste modos de falha, efeitos e causas** com base em histórico e experiência.
4. **Pontue S, O e D** com escalas definidas antes.
5. **Priorize** (RPN ou AP; severidade alta sempre).
6. **Defina ações** com responsável e prazo; repontue depois de implementadas.
7. **Mantenha a FMEA viva:** atualize com falhas reais.

## Norma relacionada

- **IEC 60812:2018**: análise de modos de falha e efeitos (FMEA e FMECA).
- **Manual AIAG-VDA FMEA (2019)**: método amplamente usado na indústria, com a priorização por AP.

## Exemplo prático

**Situação:** FMEA de projeto (trecho) do **eixo de um acionamento de rolo**.

| Modo de falha | Efeito | S | Causa | O | Controle atual | D | RPN | Ação |
|---|---|---|---|---|---|---|---|---|
| Fratura por fadiga no ressalto do mancal | Parada longa, risco de dano ao redutor | 9 | Raio de concordância pequeno | 5 | Nenhum | 8 | 360 | Aumentar raio (canal de alívio), 4140 beneficiado, ensaio por ultrassom na fabricação |
| Desgaste do assento do rolamento | Folga, vibração, perda do rolamento | 6 | Anel interno girando no eixo (ajuste folgado) | 4 | Análise de vibração mensal | 4 | 96 | Revisar ajuste (k6/m6) |
| Vazamento no retentor | Contaminação do rolamento | 5 | Pista do retentor gasta | 6 | Inspeção visual | 5 | 150 | Têmpera por indução da pista; luva de desgaste |

O primeiro item tem severidade 9 e RPN alto: ação prioritária.

> [!question] Exercício
>
> Dois modos de falha têm o mesmo RPN = 120: (a) S = 10, O = 2, D = 6; (b) S = 4, O = 6, D = 5. Qual deve ser tratado primeiro e por quê?
>
> > [!success]- Resolução
> >
> > O **(a)**, por causa da **severidade 10** (provavelmente risco à segurança ou falha catastrófica). O RPN igual esconde essa diferença. É exatamente essa limitação que levou o manual AIAG-VDA a substituir o RPN pela **prioridade de ação (AP)**, que dá mais peso à severidade.

## Erros comuns

- **Pontuar sem escala definida**, tornando os números arbitrários.
- **Olhar só o RPN** e ignorar severidades altas.
- **FMEA feita uma vez e esquecida.**
- **Não alimentar a FMEA** com as falhas que realmente aconteceram.

## Ver também

- [[Segurança de máquinas]]
- [[Fadiga de eixos]]
- [[Etapas do projeto]]
- [[09-metodologia-de-projeto/index|Índice do módulo 09]]
