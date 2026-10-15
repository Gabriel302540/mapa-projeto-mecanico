---
title: Furação e mandrilamento
tags: [fabricacao, usinagem]
fontes: [Diniz, Marcondes e Coppini Tecnologia da Usinagem dos Materiais (cap. de furação), Ferraresi Fundamentos da Usinagem dos Metais, Kalpakjian e Schmid Manufacturing Engineering and Technology (cap. de furação e mandrilamento), Machinery's Handbook (tabelas de brocas e alargadores)]
status: rascunho
---

**Resumo:** furos são feitos com brocas helicoidais (precisão de IT11 a IT13), e os furos de precisão recebem acabamento com alargador (IT7–IT8) ou mandrilamento (furos grandes, IT6–IT8, posição precisa). Roscas internas são feitas com machos sobre furos de broca. O projeto deve usar diâmetros padronizados e prever a sequência de operações.

## O que é

### Sequência típica para um furo de precisão

1. **Furo de centro** (ou pré-furo com broca de centro) para guiar a broca.
2. **Furação** com broca helicoidal (ângulo de ponta ≈ 118°), deixando sobremetal.
3. **Alargamento** (furos pequenos e médios) ou **mandrilamento** (furos grandes) até a medida final (por exemplo, H7).

| Operação | Precisão típica | Ra típico (µm) |
|---|---|---|
| Furação | IT11 – IT13 | 3,2 – 12,5 |
| Furação com broca de metal duro (CNC) | IT9 – IT10 | 1,6 – 3,2 |
| Alargamento | IT7 – IT8 | 0,8 – 3,2 |
| Mandrilamento | IT6 – IT8 | 0,8 – 3,2 |
| Brunimento (após mandrilar) | IT5 – IT6 | 0,1 – 0,4 |

⚠️ verificar com a capacidade da oficina.

### Parâmetros

- **Rotação:** $n = 1000\,v_c/(\pi D)$. Brocas de aço rápido em aço comum: $v_c$ ≈ 20–30 m/min; brocas de metal duro: ≈ 80–150 m/min. ⚠️ verificar.
- **Avanço:** cresce com o diâmetro (ordem de 0,1 a 0,4 mm/volta para brocas de 10 a 40 mm).
- **Furos profundos** (profundidade > 5 × D): exigem brocas especiais, ciclos de retirada de cavaco ou furação profunda com refrigeração interna.

### Furos para roscas

Diâmetro da broca para rosca métrica (regra prática): $D_{\text{broca}} \approx d - P$. Ver [[Cotagem de elementos]].

### Mandrilamento

Uma barra com uma ferramenta de ponta única gira dentro de um furo existente, ajustando o diâmetro e **corrigindo a posição e o alinhamento** do furo. É o processo para alojamentos de rolamentos em carcaças, furos grandes de flanges e buchas de mancais. Em peças muito grandes, existem mandriladoras portáteis (*line boring*) que usinam no próprio local da montagem, alinhando vários mancais.

## Por que importa no projeto

- **Furos com H7** pedem alargador ou mandrilamento: não especifique tolerância apertada em furos que podem ser só furados.
- **Diâmetros padronizados de brocas e alargadores** economizam ferramentas especiais.
- **Alinhamento de mancais** em estruturas grandes muitas vezes só é atingido por mandrilamento em linha após a soldagem e o alívio de tensões.

## Como aplicar (passo a passo / regras práticas)

1. **Use diâmetros padronizados** (inteiros e meios milímetros para brocas; diâmetros nominais com H7 para alargadores comuns).
2. **Furos de passagem de parafusos:** use as séries normalizadas (fina, média, grossa) e não tolerâncias apertadas. ⚠️ verificar a ISO 273.
3. **Evite furos que começam ou terminam em superfícies inclinadas** (a broca desvia): prever um rebaixo plano.
4. **Furos cegos:** prever profundidade a mais para a ponta da broca e a saída do macho.
5. **Alojamentos alinhados:** usinar na mesma fixação ou por mandrilamento em linha.

## Norma relacionada

- **ISO 273**: furos de passagem para parafusos. ⚠️ verificar.
- **ISO 286**: tolerâncias de furos (H7 etc.).
- **ISO 235 / DIN 338**: brocas helicoidais. ⚠️ verificar.

## Exemplo prático

**Situação:** fazer um furo **Ø20 H7** (20,000 a 20,021) passante numa chapa de 30 mm.

1. Broca de centro.
2. Broca Ø19,7 (sobremetal de 0,3 mm no diâmetro para o alargador). ⚠️ verificar sobremetal recomendado pelo fabricante do alargador.
3. Alargador de máquina Ø20 H7.
4. Inspeção com calibrador tampão Ø20 H7 (lado "passa" e lado "não passa").

> [!question] Exercício
>
> Qual broca usar para roscas M10 e M24 (passo grosso)?
>
> > [!success]- Resolução
> >
> > - M10 (P = 1,5): $10 - 1{,}5 =$ **8,5 mm**.
> > - M24 (P = 3): $24 - 3 =$ **21 mm**.

## Erros comuns

- **Especificar H7 num furo de passagem de parafuso.**
- **Furos iniciando em superfície inclinada** sem rebaixo.
- **Furos cegos roscados sem profundidade extra.**
- **Alojamentos de rolamentos em linha usinados separadamente.**

## Ver também

- [[Torneamento]]
- [[Tolerâncias por processo]]
- [[Cotagem de elementos]]
- [[07-processos-fabricacao/index|Índice do módulo 07]]
