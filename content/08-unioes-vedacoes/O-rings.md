---
title: "O-rings: alojamento"
tags: [vedacoes]
fontes: [ISO 3601-1 (dimensões e tolerâncias), ISO 3601-2 (alojamentos para aplicações gerais), Parker O-Ring Handbook (seções de projeto de alojamentos), Müller e Nau Fluid Sealing Technology]
status: rascunho
---

**Resumo:** o o-ring é um anel de elastômero de seção circular, montado num canal (alojamento) e comprimido entre duas superfícies. É a vedação mais simples e versátil. O projeto do canal define a compressão (aperto da seção), o enchimento do canal e a folga de extrusão — e é isso que decide se ele veda e por quanto tempo.

## O que é

### Designação

O o-ring é definido pelo **diâmetro interno** ($d_1$) e pelo **diâmetro da seção** ($d_2$): por exemplo, 50 × 3,53. Existem séries métricas e a série em polegadas (AS568), com seções de 1,78; 2,62; 3,53; 5,33; 6,99 mm.

### Tipos de aplicação

- **Estática:** sem movimento relativo (tampas, flanges, conexões).
- **Dinâmica alternativa:** hastes e êmbolos de cilindros.
- **Rotativa:** limitada a velocidades baixas.

E quanto à direção da compressão: **radial** (em eixos e furos) ou **axial** (em faces).

### Parâmetros do alojamento

| Parâmetro | Definição | Valores de referência |
|---|---|---|
| **Compressão** | $\dfrac{d_2 - h}{d_2}$ ($h$ = altura do canal, incluindo a folga) | Estática: ≈ 15–30 %; dinâmica: ≈ 10–20 % |
| **Enchimento do canal** | Área da seção do o-ring / área do canal | ≈ 70–85 % (deixar espaço para expansão térmica e inchamento) |
| **Estiramento** na montagem (diâmetro interno esticado) | | Até ≈ 5 % |
| **Folga de extrusão** | Folga entre as peças, por onde o o-ring pode ser "puxado" pela pressão | Depende da pressão e da dureza; acima de ≈ 10 MPa, usar **anéis de apoio** (*backup rings*) |

⚠️ verificar todos os valores na ISO 3601-2 ou no manual do fabricante.

**Acabamento:** superfícies de vedação estáticas ≈ Ra 1,6; dinâmicas ≈ Ra 0,1–0,4. Cantos do canal levemente arredondados. Ver [[Rugosidade pela função]].

### Materiais

| Material | Compatível com | Incompatível com |
|---|---|---|
| **NBR** (nitrílica) | Óleos minerais, graxas, água fria | Ozônio, intempérie, fluidos de freio |
| **FKM** | Óleos, combustíveis, temperatura alta (≈ 200 °C) | Vapor, cetonas |
| **EPDM** | Água, vapor, intempérie, fluidos de freio | **Óleos minerais** |
| **Silicone** | Faixa ampla de temperatura, alimentos | Abrasão, aplicações dinâmicas |

Dureza usual: **70 Shore A**; 90 Shore A para pressões altas. ⚠️ verificar compatibilidade química nas tabelas do fabricante.

## Por que importa no projeto

- **Tampas, flanges, conexões hidráulicas, cilindros e válvulas** usam o-rings em grande quantidade.
- **Canal mal dimensionado** é a causa mais comum de vazamento: pouca compressão (não veda) ou canal cheio demais (o anel é esmagado ou extrudado).
- **Material errado** (EPDM com óleo, NBR com vapor) destrói o anel em pouco tempo.

## Como aplicar (passo a passo / regras práticas)

1. **Defina o tipo** (estático ou dinâmico; radial ou axial), a pressão, a temperatura e o fluido.
2. **Escolha o material** e a dureza.
3. **Escolha a seção** $d_2$ (maiores são mais tolerantes a variações).
4. **Dimensione o canal** (altura e largura) pela tabela da ISO 3601-2 ou do fabricante, conferindo compressão e enchimento.
5. **Verifique a folga de extrusão** e use anel de apoio se necessário.
6. **Preveja chanfros de montagem** (≈ 15°–20°) para o anel não ser cortado.

## Norma relacionada

- **ISO 3601-1**: dimensões e tolerâncias dos o-rings.
- **ISO 3601-2**: dimensões de alojamentos.
- **AS568**: série de dimensões em polegadas (muito usada).

## Exemplo prático

**Situação:** vedação **estática radial** com o-ring de seção **5,33 mm** num canal de **4,2 mm** de altura (já incluindo a folga) e **7,1 mm** de largura.

- Compressão: $\dfrac{5{,}33 - 4{,}2}{5{,}33} \approx 21\ \%$ → dentro da faixa estática ✔
- Área da seção do o-ring: $\dfrac{\pi \times 5{,}33^2}{4} \approx 22{,}3$ mm²
- Área do canal: $4{,}2 \times 7{,}1 \approx 29{,}8$ mm²
- Enchimento: $22{,}3/29{,}8 \approx 75\ \%$ → adequado ✔

> [!question] Exercício
>
> Um o-ring de seção 3,53 mm é montado num canal de 3,1 mm de altura. Qual a compressão? É adequada para vedação estática?
>
> > [!success]- Resolução
> >
> > Compressão $= (3{,}53 - 3{,}1)/3{,}53 \approx 12\ \%$. Para vedação **estática**, está **abaixo** da faixa usual (≈ 15–30 %): pode vazar em baixa pressão ou com o anel envelhecido. Seria melhor reduzir a altura do canal para ≈ 2,7–2,9 mm.

## Erros comuns

- **Canal cheio demais** (sem espaço para inchamento e dilatação).
- **Compressão baixa** em vedações estáticas.
- **Sem anel de apoio** em pressões altas com folga grande.
- **EPDM em contato com óleo mineral.**
- **Montagem sem chanfro**, cortando o anel em roscas e cantos.

## Ver também

- [[Retentores]]
- [[Juntas planas]]
- [[Rugosidade pela função]]
- [[08-unioes-vedacoes/index|Índice do módulo 08]]
