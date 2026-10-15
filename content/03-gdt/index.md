---
title: 03 · GD&T
tags: [indice, gdt]
---

**Resumo:** Tolerâncias de forma, orientação, posição e batimento: controlam a geometria da peça, não só o tamanho.

## Por que este módulo importa
Um eixo pode estar com o diâmetro certo e mesmo assim estar torto ou excêntrico. Em eixos de moenda, redutores e mancais, o batimento e a coaxialidade decidem a vida dos rolamentos e das vedações.

## Tópicos
Ordem sugerida de estudo: de cima para baixo.

- [x] [[Por que GD&T|Por que usar tolerâncias geométricas]]
- [x] [[Independência e envoltória|Princípio da independência e requisito de envoltória]]
- [x] [[Quadro de tolerância]]
- [x] [[Referências geométricas|Referências (datums)]]
- [x] [[Tolerâncias de forma]]
- [x] [[Tolerâncias de orientação]]
- [x] [[Tolerâncias de localização]]
- [x] [[Batimento|Batimento circular e total]]
- [x] [[Tolerância de perfil]]
- [x] [[Requisito de máximo material|Modificadores de material (MMR e LMR)]]
- [x] [[Leitura de GD&T|Leitura de um desenho com GD&T]]

## Normas principais
Lista de partida, para conferir no documento original. Nenhum trecho de norma é reproduzido aqui.

- ISO 1101 — tolerâncias geométricas
- ISO 5459 — referências e sistemas de referência
- ISO 8015 — conceitos fundamentais (princípio da independência)
- ISO 2692 — requisitos de máximo e mínimo material
- ASME Y14.5 — equivalente americano (comparação)

## Módulos relacionados
- [[02-tolerancias-ajustes/index|02 · Tolerâncias e ajustes]]
- [[04-acabamento-superficial/index|04 · Acabamento superficial]]

## Revisão rápida

Tente responder antes de abrir a resposta.

> [!question] 1. Por que uma tolerância de diâmetro (por exemplo Ø50 h6) não garante que um eixo esteja reto, num desenho ISO?
>
> > [!success]- Resposta
> >
> > Porque, pelo **princípio da independência** (ISO 8015), a tolerância de tamanho controla só o **tamanho local** (medidas de dois pontos). A forma (retitude, circularidade) precisa de tolerância geométrica própria ou do requisito de envoltória Ⓔ. Ver [[Independência e envoltória]].

> [!question] 2. Quais são as quatro famílias de tolerâncias geométricas e quais delas nunca têm referência?
>
> > [!success]- Resposta
> >
> > **Forma, orientação, localização e batimento** (mais o perfil, que pode atuar como qualquer uma delas). As de **forma** (retitude, planeza, circularidade, cilindricidade) nunca têm referência. Ver [[Por que GD&T]].

> [!question] 3. Qual a diferença entre apontar a seta do quadro para a superfície de um cilindro e alinhá-la com a cota de diâmetro?
>
> > [!success]- Resposta
> >
> > Na **superfície**, a tolerância controla a própria superfície. **Alinhada à cota**, controla o elemento derivado: o **eixo** do cilindro. Ver [[Quadro de tolerância]].

> [!question] 4. Num sistema de referências A | B | C com planos, quantos pontos de contato e graus de liberdade cada referência trava?
>
> > [!success]- Resposta
> >
> > **A (primária):** 3 pontos, 3 graus de liberdade. **B (secundária):** 2 pontos, 2 graus. **C (terciária):** 1 ponto, 1 grau. Total: 6 graus de liberdade. Ver [[Referências geométricas]].

> [!question] 5. Uma face tem paralelismo de 0,05 com A. Qual a máxima planeza possível dessa face? E a distância até A fica controlada?
>
> > [!success]- Resposta
> >
> > A planeza fica limitada a **0,05 mm** (a orientação contém a forma). A **distância** até A **não** é controlada pelo paralelismo; ela depende da cota de tamanho ou de uma tolerância de posição. Ver [[Tolerâncias de orientação]].

> [!question] 6. Um furo deveria estar em (40, 25) e foi medido em (40,08; 25,06). Qual o diâmetro da zona de posição que ele ocupa?
>
> > [!success]- Resposta
> >
> > $\varnothing = 2\sqrt{0{,}08^2 + 0{,}06^2} = 2 \times 0{,}10 = 0{,}20$ mm. Ver [[Tolerâncias de localização]].

> [!question] 7. Duas peças são unidas por parafusos M10 com porca (fixador flutuante), com furos de Ø11 no mínimo. Qual a tolerância de posição de cada peça?
>
> > [!success]- Resposta
> >
> > $t = H - F = 11 - 10 = 1{,}0$ mm → **Ø1,0 Ⓜ** em cada peça. Ver [[Tolerâncias de localização]].

> [!question] 8. Um relógio comparador sobre um diâmetro marca de −0,02 a +0,04 mm ao girar a peça. Qual o batimento e a excentricidade aproximada?
>
> > [!success]- Resposta
> >
> > Batimento: $0{,}04 - (-0{,}02) = 0{,}06$ mm. Excentricidade ≈ $0{,}06/2 = 0{,}03$ mm. Ver [[Batimento]].

> [!question] 9. Qual a diferença entre usar um perfil de superfície sem referência e com referências A, B, C?
>
> > [!success]- Resposta
> >
> > **Sem referência**, controla só a **forma** do perfil (ele pode estar deslocado ou inclinado). **Com A, B, C**, controla **forma, orientação e posição**. Ver [[Tolerância de perfil]].

> [!question] 10. Furos 4× Ø16 +0,4/0 têm posição Ø0,3 Ⓜ. Qual a tolerância de posição de um furo medido com Ø16,25? E qual o limite virtual para o calibrador?
>
> > [!success]- Resposta
> >
> > Bônus: $16{,}25 - 16{,}00 = 0{,}25$ → tolerância **Ø0,55**. Limite virtual: $16{,}0 - 0{,}3 =$ **Ø15,7** (diâmetro dos pinos do calibrador funcional). Ver [[Requisito de máximo material]].

