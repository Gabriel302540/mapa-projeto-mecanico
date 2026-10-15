---
title: Tolerâncias alcançáveis por processo
tags: [fabricacao, tolerancias]
fontes: [ISO 286-1:2010 (graus IT), ISO 2768-1, ISO 8062-3 (tolerâncias de fundidos) ⚠️ verificar, ISO 9013 (corte térmico), Kalpakjian e Schmid Manufacturing Engineering and Technology (cap. de tolerâncias e acabamento), Machinery's Handbook (tabela de graus IT por processo)]
status: rascunho
---

**Resumo:** cada processo de fabricação alcança, de forma econômica, uma faixa de graus IT e de rugosidade. Especificar uma tolerância é, na prática, escolher o processo final. Esta nota reúne as faixas típicas e a lógica de custo, para que tolerância e processo sejam coerentes no desenho.

## O que é

### Graus IT alcançáveis (faixa econômica típica)

| Processo | IT típico | Ra típico (µm) |
|---|---|---|
| Lapidação | IT3 – IT5 | 0,025 – 0,2 |
| Brunimento | IT4 – IT6 | 0,05 – 0,4 |
| Retificação cilíndrica e plana | IT5 – IT7 | 0,2 – 1,6 |
| Torneamento fino / mandrilamento fino | IT6 – IT8 | 0,4 – 1,6 |
| Alargamento | IT7 – IT8 | 0,8 – 3,2 |
| Brochamento | IT7 – IT8 | 0,8 – 3,2 |
| Torneamento de acabamento | IT7 – IT9 | 0,8 – 3,2 |
| Fresamento | IT8 – IT10 | 1,6 – 6,3 |
| Torneamento de desbaste | IT11 – IT13 | 6,3 – 25 |
| Furação | IT11 – IT13 | 3,2 – 12,5 |
| Corte a laser | ≈ IT11 – IT13 (em chapas finas) | 1,6 – 6,3 |
| Corte a plasma | ≈ IT13 – IT15 | 6,3 – 25 |
| Oxicorte | ≈ IT14 – IT16 | 12,5 – 50 |
| Fundição em areia | IT14 – IT16 | 12,5 – 50 |
| Forjamento a quente | IT14 – IT16 | 3,2 – 12,5 |

Faixas compiladas de manuais de fabricação; dependem do tamanho da peça, da máquina e do material. ⚠️ verificar com a capacidade real da oficina. Ver [[Graus IT]] e [[Rugosidade por processo]].

### Custo × tolerância

O custo de fabricação cresce de forma aproximadamente exponencial quando a tolerância diminui. Cada vez que a tolerância exige uma **operação a mais** (retificar depois de tornear, brunir depois de mandrilar), o custo dá um salto. Por isso:

- **Grau IT e Ra devem ser coerentes:** IT6 com Ra 3,2 não faz sentido (a rugosidade já consome parte da tolerância); IT11 com Ra 0,4 desperdiça dinheiro.
- **Uma regra prática:** a altura total da rugosidade (Rz) não deve passar de cerca de 1/4 a 1/3 da tolerância dimensional.

### Peças grandes

Para dimensões grandes, a mesma classe IT corresponde a valores absolutos maiores, mas as máquinas grandes também têm menor precisão absoluta e a **temperatura** passa a pesar: uma peça de aço de 1 m dilata cerca de **12 µm por °C**. Medições de precisão em peças grandes exigem controle de temperatura ou correção.

## Por que importa no projeto

- **Tolerância incoerente com o processo** gera refugo, retrabalho ou custo desnecessário.
- **Peças soldadas** têm tolerâncias próprias (ISO 13920): especificar IT7 em cotas de uma estrutura soldada sem usinagem é impossível.
- **Conversa com a oficina:** conhecer a faixa de cada processo ajuda a negociar soluções (por exemplo, aceitar IT8 com seleção na montagem, em vez de IT6).

## Como aplicar (passo a passo / regras práticas)

1. Defina a tolerância **pela função** (ver [[Ajustes recomendados]]).
2. Verifique na tabela **qual processo** atinge essa tolerância de forma econômica.
3. Confira se o processo é **viável** para o tamanho e o material da peça e se está disponível.
4. Ajuste Ra para ser **coerente** com o grau IT.
5. Deixe o restante na **tolerância geral** (ISO 2768 ou ISO 13920). Ver [[Tolerâncias gerais]].

## Norma relacionada

- **ISO 286-1**: graus IT.
- **ISO 2768-1** e **ISO 13920**: tolerâncias gerais (usinados e soldados).
- **ISO 8062-3**: tolerâncias de peças fundidas. ⚠️ verificar.
- **ISO 9013**: qualidade de corte térmico.

## Exemplo prático

**Situação:** o desenho de uma **tampa de mancal** pede Ø180 g6 no ressalto de centralização, Ra 3,2.

- Ø180 g6 → IT6 (25 µm na faixa 120–180) → exige **torneamento fino ou retificação**.
- Ra 3,2 → rugosidade de **torneamento comum**: Rz pode chegar a ≈ 15–20 µm, quase toda a tolerância.
- **Incoerência.** A função (centralizar a tampa num alojamento H7) é atendida com folga por **Ø180 h7 ou g7** e Ra 1,6, obtidos no torno com bom acabamento, sem retífica. A revisão reduz custo sem perder função.

> [!question] Exercício
>
> Um projetista especifica um furo de Ø25 H7 obtido "por furação". O que está errado e qual a sequência correta?
>
> > [!success]- Resolução
> >
> > A furação atinge cerca de **IT11–IT13**; H7 exige **IT7**. Sequência correta: furo de centro → broca (≈ Ø24,7) → **alargador Ø25 H7** (ou mandrilamento, conforme o tamanho e a posição exigida).

## Erros comuns

- **Tolerâncias de usinagem em peças soldadas ou cortadas** sem usinagem posterior.
- **Grau IT e Ra incoerentes.**
- **Ignorar a temperatura** na medição de peças grandes.
- **Apertar todas as tolerâncias** "por segurança".

## Ver também

- [[Graus IT]]
- [[Rugosidade por processo]]
- [[Projeto para fabricação]]
- [[07-processos-fabricacao/index|Índice do módulo 07]]
