---
title: Tratamentos superficiais
tags: [materiais, tratamento-termico, desgaste]
fontes: [Chiaverini Tratamentos Térmicos das Ligas Metálicas (caps. de cementação, nitretação e têmpera superficial), ASM Handbook vol. 4 e vol. 5 (engenharia de superfícies), ISO 2639 e ISO 3754 (profundidade de camada cementada e temperada) ⚠️ verificar, Budynas e Nisbett Elementos de Máquinas de Shigley]
status: rascunho
---

**Resumo:** tratamentos superficiais endurecem só a camada externa da peça, mantendo o núcleo tenaz. Combinam resistência ao desgaste e à fadiga de contato na superfície com resistência a choques no núcleo. Os principais são cementação, nitretação, têmpera por indução ou chama, cromo duro, aspersão térmica e jateamento com granalha.

## O que é

### Comparação

| Tratamento | Como funciona | Aços típicos | Dureza superficial | Profundidade típica | Distorção |
|---|---|---|---|---|---|
| **Cementação + têmpera** | Enriquece a superfície de carbono a ≈ 900–930 °C e tempera | Baixo carbono: 1020, **8620**, 16MnCr5 | 58 – 62 HRC | 0,5 – 2 mm | Média a alta |
| **Carbonitretação** | Carbono + nitrogênio, temperatura menor | Baixo carbono | 58 – 62 HRC | 0,1 – 0,7 mm | Média |
| **Nitretação** (gasosa, plasma) | Difunde nitrogênio a ≈ 500–550 °C, **sem têmpera** | **4140**, aços para nitretação | 50 – 70 HRC equivalente (depende do aço) | 0,1 – 0,6 mm | **Muito baixa** |
| **Têmpera por indução** | Aquece só a superfície por corrente induzida e resfria | Médio carbono: **1045, 4140** | 50 – 58 HRC | 1 – 6 mm | Baixa a média |
| **Têmpera por chama** | Igual, aquecendo com maçarico | Médio carbono | 50 – 58 HRC | 2 – 8 mm | Média; controle menor |
| **Cromo duro** (eletrodeposição) | Camada de cromo depositada | Qualquer aço | ≈ 65–70 HRC (cromo) | 0,02 – 0,5 mm | Nenhuma (processo a frio); risco de fragilização por hidrogênio |
| **Aspersão térmica / metalização** | Partículas fundidas projetadas na superfície | Qualquer metal | Conforme o revestimento (carbonetos, ligas Ni-Cr) | 0,1 – 2 mm | Baixa |
| **Jateamento com granalha** (*shot peening*) | Impacto de esferas cria tensões de compressão | Qualquer aço | Pouca mudança | ≈ 0,1 – 0,5 mm de tensões residuais | Pouca |

⚠️ verificar valores com o fornecedor de tratamento e nas fichas dos aços.

### Profundidade de camada

Especifica-se a **profundidade efetiva de camada**: a distância da superfície até onde a dureza cai a um valor de referência (por exemplo, 550 HV na cementação, ou 80 % da dureza superficial mínima na têmpera por indução). ⚠️ verificar os critérios nas normas ISO 2639 e ISO 3754.

## Por que importa no projeto

- **Engrenagens:** cementação ou nitretação aumentam muito a resistência ao pitting. Ver [[Dimensionamento de engrenagens]].
- **Eixos e pinos:** têmpera por indução nos assentos de buchas e retentores combate o desgaste; o núcleo beneficiado resiste à fadiga.
- **Recuperação de peças:** cromo duro e aspersão térmica recuperam diâmetros desgastados (mas não substituem material estrutural).
- **Fadiga:** nitretação e jateamento criam **tensões residuais de compressão**, que retardam o início das trincas e aumentam o limite de fadiga.

## Como aplicar (passo a passo / regras práticas)

1. **Desgaste + choque:** núcleo tenaz + camada dura (cementação ou indução).
2. **Peças acabadas que não podem distorcer:** nitretação.
3. **Regiões localizadas** (assento, pista de vedação): têmpera por indução só na região, com faixa de transição fora das zonas de tensão alta.
4. **Especifique:** dureza superficial (faixa), profundidade efetiva de camada, região a tratar (cotada no desenho), dureza do núcleo, e a sequência com a usinagem (retificar depois).
5. **Evite terminar a zona temperada** exatamente num raio de concordância ou rasgo de chaveta (a transição é uma região de tensões residuais de tração).

## Norma relacionada

- **ISO 2639**: determinação da profundidade de camada cementada. ⚠️ verificar.
- **ISO 3754**: profundidade efetiva de camada temperada por chama ou indução. ⚠️ verificar.
- **ISO 6508 / ISO 6507**: dureza Rockwell e Vickers.

## Exemplo prático

**Situação:** um **eixo de acionamento** de 4140 beneficiado (28–32 HRC) desgasta rapidamente na região onde trabalha o lábio do retentor.

- **Solução:** **têmpera por indução** da faixa do retentor (dureza ≥ 50 HRC, profundidade efetiva de 1,5–2,5 mm), seguida de **retificação de mergulho** (Ra 0,2–0,8). Ver [[Rugosidade pela função]].
- **Alternativa para recuperação** de eixo já gasto: luva de desgaste (*speedi-sleeve*) prensada ou aspersão térmica e retificação.
- **Cuidado:** manter a zona temperada afastada do raio do ressalto vizinho.

> [!question] Exercício
>
> Uma engrenagem de 4140 já usinada e retificada precisa de maior dureza superficial, mas não pode ter distorção (as tolerâncias já estão no limite). Qual tratamento escolher?
>
> > [!success]- Resolução
> >
> > **Nitretação** (gasosa ou a plasma). É feita a cerca de 500–550 °C, **abaixo** da temperatura de revenido do beneficiamento e **sem têmpera**, por isso a distorção é mínima. O 4140 nitretado ganha camada dura, boa resistência ao desgaste e à fadiga de contato. Cementação ou indução causariam distorção maior.

## Erros comuns

- **Cementar aço de médio carbono** (a camada fica frágil demais).
- **Nitretar sem beneficiamento prévio** (o núcleo mole não sustenta a camada).
- **Zona temperada terminando num raio de concordância.**
- **Cromo duro em peças sob fadiga** sem desidrogenação (reduz o limite de fadiga).
- **Não especificar profundidade de camada.**

## Ver também

- [[Têmpera e revenido]]
- [[Revestimento duro]]
- [[Rugosidade pela função]]
- [[06-materiais/index|Índice do módulo 06]]
