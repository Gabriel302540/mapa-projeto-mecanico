---
title: Graus de tolerância IT
tags: [tolerancias, iso-286]
fontes: [ISO 286-1:2010, ABNT NBR 6158:1995, Budynas e Nisbett Elementos de Máquinas de Shigley (cap. de tolerâncias e ajustes), Agostinho, Rodrigues e Lirani Tolerâncias, Ajustes, Desvios e Análise de Dimensões]
status: rascunho
---

**Resumo:** o grau de tolerância IT define o **tamanho** da faixa de tolerância, de IT01 (a mais estreita) a IT18 (a mais larga). O valor em micrômetros depende do grau e da faixa de diâmetro: peças maiores têm tolerâncias maiores no mesmo grau, porque é mais difícil fabricá-las com a mesma precisão absoluta.

## O que é

A ISO 286 define **20 graus de tolerância normalizados**: IT01, IT0, IT1, IT2, ..., IT18. Quanto maior o número, maior a tolerância.

### De onde vêm os valores

Para dimensões até 500 mm, os graus IT5 a IT18 são múltiplos de uma **unidade de tolerância** $i$, que cresce com o diâmetro (é uma lei empírica, baseada na dificuldade real de fabricar e medir):

$$
i = 0{,}45\,\sqrt[3]{D} + 0{,}001\,D \qquad (i \text{ em µm},\ D \text{ em mm})
$$

onde $D$ é a média geométrica dos limites da faixa de diâmetros. Os graus são:

| Grau | IT5 | IT6 | IT7 | IT8 | IT9 | IT10 | IT11 | IT12 | IT13 |
|---|---|---|---|---|---|---|---|---|---|
| Múltiplo de $i$ | 7 | 10 | 16 | 25 | 40 | 64 | 100 | 160 | 250 |

Repare na progressão: a cada **5 graus**, a tolerância é multiplicada por **10** (IT6 = 10 i, IT11 = 100 i). Isso vem da série de números preferenciais R5, com razão $\sqrt[5]{10} \approx 1{,}6$ entre graus vizinhos.

### Tabela de valores (µm)

| Faixa (mm) | IT5 | IT6 | IT7 | IT8 | IT9 | IT10 | IT11 |
|---|---|---|---|---|---|---|---|
| até 3 | 4 | 6 | 10 | 14 | 25 | 40 | 60 |
| > 3 a 6 | 5 | 8 | 12 | 18 | 30 | 48 | 75 |
| > 6 a 10 | 6 | 9 | 15 | 22 | 36 | 58 | 90 |
| > 10 a 18 | 8 | 11 | 18 | 27 | 43 | 70 | 110 |
| > 18 a 30 | 9 | 13 | 21 | 33 | 52 | 84 | 130 |
| > 30 a 50 | 11 | 16 | 25 | 39 | 62 | 100 | 160 |
| > 50 a 80 | 13 | 19 | 30 | 46 | 74 | 120 | 190 |
| > 80 a 120 | 15 | 22 | 35 | 54 | 87 | 140 | 220 |
| > 120 a 180 | 18 | 25 | 40 | 63 | 100 | 160 | 250 |
| > 180 a 250 | 20 | 29 | 46 | 72 | 115 | 185 | 290 |
| > 250 a 315 | 23 | 32 | 52 | 81 | 130 | 210 | 320 |
| > 315 a 400 | 25 | 36 | 57 | 89 | 140 | 230 | 360 |
| > 400 a 500 | 27 | 40 | 63 | 97 | 155 | 250 | 400 |

⚠️ verificar os valores na ISO 286-1 antes de usar em projeto. A norma vai até 3150 mm.

**Atenção às faixas:** cada faixa inclui o limite superior. Um diâmetro de exatamente 50 mm está na faixa "> 30 a 50"; um de 50,5 mm está em "> 50 a 80".

### Graus e processos de fabricação

| Graus | Aplicação típica | Processos que alcançam |
|---|---|---|
| IT01 a IT4 | Calibradores, padrões, instrumentos | Lapidação, retificação de precisão |
| IT5 a IT7 | Ajustes de precisão: rolamentos, engrenagens, pinos | Retificação, torneamento e mandrilamento finos, alargamento |
| IT8 a IT11 | Ajustes comuns e folgados | Torneamento, fresamento, furação seguida de alargador (IT8-IT9), furação (IT11 a IT13) |
| IT12 a IT18 | Medidas livres, peças brutas | Corte térmico, estampagem, fundição, forjamento, laminação |

Essas faixas são aproximadas e dependem da máquina, do tamanho da peça e do operador. Ver [[07-processos-fabricacao/index|Processos de fabricação]].

## Por que importa no projeto

- **Escolher o grau é escolher o processo.** IT6 no eixo praticamente obriga retificação ou torneamento muito fino; IT9 sai no torno comum.
- **Furos são mais difíceis que eixos.** Por isso, num ajuste, o furo costuma ter um grau a mais: **H7 com eixo 6** (H7/g6, H7/k6...). O furo é medido e corrigido com mais dificuldade.
- **Peças grandes:** em diâmetros acima de 300 mm, mesmo IT7 já são dezenas de micrômetros, e a dilatação térmica (cerca de 12 µm por metro por °C no aço) começa a pesar na medição.

## Como aplicar (passo a passo / regras práticas)

1. **Ajustes de rolamentos e engrenagens:** eixo IT5-IT6, alojamento IT6-IT7 (seguir o catálogo do rolamento).
2. **Ajustes gerais de máquinas:** furo IT7-IT8, eixo IT6-IT7.
3. **Ajustes folgados, sem precisão:** IT9-IT11.
4. **Medidas livres:** tolerância geral (IT12-IT16 equivalente). Ver [[Tolerâncias gerais]].
5. **Encontre o valor:** localize a faixa do diâmetro na tabela e leia a coluna do grau.

## Norma relacionada

- **ISO 286-1:2010**: define os graus IT e a tabela de valores até 3150 mm.
- **ABNT NBR 6158:1995**: versão brasileira do sistema. ⚠️ verificar edição vigente.

## Exemplo prático

**Situação:** comparar a tolerância de grau IT7 para dois diâmetros de uma mesma transmissão: a ponta de eixo de um redutor pequeno (Ø40) e o munhão de um eixo grande (Ø400).

- Ø40 IT7: faixa "> 30 a 50" → **25 µm**.
- Ø400 IT7: faixa "> 315 a 400" → **57 µm**.

A tolerância é cerca de 2,3 vezes maior, embora o diâmetro seja 10 vezes maior. Isso mostra que a precisão **relativa** é melhor nas peças grandes ($57/400\,000 \approx 0{,}014\ \%$ contra $25/40\,000 \approx 0{,}063\ \%$), o que reflete a maior dificuldade de fabricá-las.

Conferência pela fórmula para a faixa de 30 a 50 mm: $D = \sqrt{30 \times 50} \approx 38{,}7$ mm, $i = 0{,}45\sqrt[3]{38{,}7} + 0{,}001 \times 38{,}7 \approx 1{,}56$ µm, e $IT7 = 16\,i \approx 25$ µm. ✔

> [!question] Exercício 1
>
> Qual a tolerância IT6 e IT8 para um diâmetro de 65 mm?
>
> > [!success]- Resolução
> >
> > Faixa "> 50 a 80": **IT6 = 19 µm** e **IT8 = 46 µm**.

> [!question] Exercício 2
>
> Usando a fórmula da unidade de tolerância, estime IT9 para a faixa de 80 a 120 mm e compare com a tabela.
>
> > [!success]- Resolução
> >
> > $D = \sqrt{80 \times 120} \approx 98{,}0$ mm.
> > $i = 0{,}45\sqrt[3]{98} + 0{,}001 \times 98 \approx 0{,}45 \times 4{,}61 + 0{,}098 \approx 2{,}17$ µm.
> > $IT9 = 40\,i \approx 86{,}9$ µm → arredondado, **87 µm**, igual à tabela.

## Erros comuns

- **Ler a faixa errada** nos limites (50 mm pertence a "> 30 a 50").
- **Usar o mesmo grau para furo e eixo** em ajustes de precisão, quando o furo deveria ter um grau a mais.
- **Especificar IT5-IT6 sem necessidade**, encarecendo a peça.
- **Esquecer a temperatura de medição** (a referência é 20 °C) em peças grandes.

## Ver também

- [[Conceitos de tolerância]]
- [[Posições de tolerância]]
- [[Ajustes recomendados]]
- [[02-tolerancias-ajustes/index|Índice do módulo 02]]
