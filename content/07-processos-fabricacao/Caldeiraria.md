---
title: "Caldeiraria: traçagem e planificação"
tags: [fabricacao, caldeiraria]
fontes: [Provenza Desenhista de Máquinas (cap. de planificação) ⚠️ verificar capítulo, French e Vierck Desenho Técnico e Tecnologia Gráfica (cap. de desenvolvimento de superfícies), Telecurso 2000 Caldeiraria ⚠️ verificar, Kalpakjian e Schmid Manufacturing Engineering and Technology (cap. de conformação de chapas)]
status: rascunho
---

**Resumo:** caldeiraria é a fabricação de peças a partir de chapas: tanques, dutos, tremonhas, chutes, transições, cones. Antes de cortar, é preciso "abrir" a forma 3D na chapa plana — a planificação (desenvolvimento) —, usando a linha neutra da chapa para que, depois de calandrada ou dobrada, a peça tenha as medidas certas.

## O que é

### Linha neutra

Ao curvar uma chapa, o lado de fora estica e o de dentro encurta. Há uma linha no interior da espessura que **não muda de comprimento**: a **linha neutra**. Para calandragem (raios grandes em relação à espessura), ela fica praticamente no **meio da espessura**. O desenvolvimento é calculado pelo **diâmetro médio**.

### Cilindro (virola)

$$
L = \pi\,D_m = \pi\,(D_e - t) = \pi\,(D_i + t)
$$

com $D_e$ o diâmetro externo, $D_i$ o interno e $t$ a espessura.

### Cone e tronco de cone

Um tronco de cone com raios $R$ (maior) e $r$ (menor) e altura $h$ (medidos na linha média) planifica-se num **setor de coroa circular**:

- Geratriz do tronco: $s = \sqrt{h^2 + (R - r)^2}$
- Geratriz do cone completo (até o vértice): $G = \dfrac{R\,s}{R - r}$
- Raio menor do setor: $g = G - s$
- Ângulo do setor: $\theta = 360° \times \dfrac{R}{G}$

### Formas sem desenvolvimento exato

**Transições** (quadrado para redondo, retangular para circular) e **interseções de tubos** (boca de lobo, derivações) são planificadas por **triangulação** (dividir a superfície em triângulos pequenos, medir seus lados em verdadeira grandeza e montá-los na chapa) ou por **linhas paralelas** (para interseções de cilindros). Hoje, programas de CAD de chapas fazem isso automaticamente, mas entender o método ajuda a conferir.

### Etapas típicas

1. **Traçagem:** marcar na chapa o desenvolvimento, as linhas de dobra, os furos e as referências.
2. **Corte:** térmico (oxicorte, plasma, laser), guilhotina ou serra. Ver [[Corte térmico]].
3. **Conformação:** calandragem (cilindros e cones), dobra em prensa dobradeira. Ver [[Dobra de chapas]].
4. **Montagem e ponteamento:** posicionar com gabaritos e soldar provisoriamente.
5. **Soldagem final** e controle dimensional.

## Por que importa no projeto

- **Chutes, tremonhas, tanques, dutos e caixas** são peças de caldeiraria comuns em equipamentos industriais.
- **Projeto com chapas padrão** (comprimentos e larguras comerciais, ex.: 2000 × 6000 mm, ⚠️ verificar com fornecedores) reduz emendas e perdas.
- **Desenhos de caldeiraria** devem indicar se as cotas são internas, externas ou na linha média.

## Como aplicar (passo a passo / regras práticas)

1. **Use a linha média** para desenvolvimentos de calandragem; para dobras com raio pequeno, use o fator K (ver [[Dobra de chapas]]).
2. **Indique no desenho** a referência das cotas (interna ou externa) e a espessura.
3. **Posicione as emendas** longe de regiões de maior tensão ou desgaste e defasadas entre virolas.
4. **Aproveite chapas padrão** no arranjo (*nesting*) das peças.
5. **Preveja tolerâncias de caldeiraria** (ISO 13920), e não de usinagem. Ver [[Tolerâncias por processo]].

## Norma relacionada

- **ISO 13920**: tolerâncias gerais para construções soldadas.
- **ASME Seção VIII / NR-13**: quando a peça for vaso de pressão. ⚠️ verificar.
- Os métodos de planificação vêm da **geometria descritiva**, não de norma.

## Exemplo prático

**Situação 1 — virola:** tanque com **Ø1000 externo**, chapa de **12,5 mm**.

$$
L = \pi\,(1000 - 12{,}5) = \pi \times 987{,}5 \approx 3102{,}3\ \text{mm}
$$

Se fosse usado o diâmetro externo, a chapa sairia com 3141,6 mm, cerca de 39 mm a mais: a virola não fecharia no diâmetro correto.

**Situação 2 — tronco de cone (tremonha):** $R$ = 400 mm, $r$ = 200 mm, $h$ = 500 mm (linha média).

- $s = \sqrt{500^2 + 200^2} \approx 538{,}5$ mm
- $G = 400 \times 538{,}5/200 \approx 1077$ mm
- $g = 1077 - 538{,}5 \approx 538{,}5$ mm
- $\theta = 360° \times 400/1077 \approx 133{,}7°$

Na chapa, traça-se um setor de coroa circular com raios de 1077 e 538,5 mm e ângulo de 133,7°.

> [!question] Exercício
>
> Qual o comprimento da chapa para uma virola de Ø600 **interno** em chapa de 8 mm?
>
> > [!success]- Resolução
> >
> > Diâmetro médio: $600 + 8 = 608$ mm. $L = \pi \times 608 \approx 1910{,}1$ mm.

## Erros comuns

- **Desenvolver pelo diâmetro externo ou interno** em vez do médio.
- **Desenho sem indicar** se as cotas são internas ou externas.
- **Emendas alinhadas** em virolas sobrepostas.
- **Tolerâncias de usinagem** em peças de caldeiraria.

## Ver também

- [[Dobra de chapas]]
- [[Corte térmico]]
- [[Juntas e chanfros]]
- [[07-processos-fabricacao/index|Índice do módulo 07]]
