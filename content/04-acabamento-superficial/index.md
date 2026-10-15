---
title: 04 · Acabamento superficial
tags: [indice, acabamento]
---

**Resumo:** Rugosidade e textura da superfície: como medir, especificar e indicar no desenho.

## Por que este módulo importa
Superfície de assento de rolamento, pista de retentor e face de vedação exigem acabamentos diferentes. Especificar Ra baixo onde não precisa só aumenta custo de usinagem.

## Tópicos
Ordem sugerida de estudo: de cima para baixo.

- [x] [[Textura superficial|Textura superficial: rugosidade, ondulação e forma]]
- [x] [[Parâmetros de rugosidade|Parâmetros Ra, Rz e outros]]
- [x] [[Símbolos de acabamento|Símbolos de acabamento no desenho]]
- [x] [[Rugosidade por processo|Rugosidade obtida por processo de fabricação]]
- [x] [[Rugosidade pela função|Rugosidade exigida pela função]]
- [x] [[Medição de rugosidade|Medição com rugosímetro]]

## Normas principais
Lista de partida, para conferir no documento original. Nenhum trecho de norma é reproduzido aqui.

- ISO 21920 (série) — textura de superfície: perfil ⚠️ verificar se substituiu a ISO 4287 e a ISO 1302
- ISO 1302 — indicação da textura no desenho
- ABNT NBR 8404 — indicação do estado de superfície ⚠️ verificar edição vigente

## Módulos relacionados
- [[03-gdt/index|03 · GD&T]]
- [[07-processos-fabricacao/index|07 · Processos de fabricação]]
- [[08-unioes-vedacoes/index|08 · Uniões e vedações]]

## Revisão rápida

Tente responder antes de abrir a resposta.

> [!question] 1. Quais são os três componentes da textura de uma superfície e qual a causa típica de cada um?
>
> > [!success]- Resposta
> >
> > **Forma** (deflexões, desalinhamentos, tensões), **ondulação** (vibrações, desbalanceamento do rebolo) e **rugosidade** (marcas da ferramenta, avanço e raio de ponta). Ver [[Textura superficial]].

> [!question] 2. Por que o Ra sozinho pode ser insuficiente para especificar uma superfície de vedação dinâmica?
>
> > [!success]- Resposta
> >
> > Porque o Ra é uma **média** e esconde riscos ou picos isolados. Uma vedação que desliza é sensível a esses defeitos. Complementa-se com **Rz máximo** ou parâmetros de razão de material (Rmr). Ver [[Parâmetros de rugosidade]].

> [!question] 3. Qual a diferença entre o símbolo de acabamento com traço fechando o V e o com um círculo no V?
>
> > [!success]- Resposta
> >
> > Com **traço**: remoção de material **obrigatória** (usinar). Com **círculo**: remoção de material **proibida** (a superfície fica como veio do processo anterior). Ver [[Símbolos de acabamento]].

> [!question] 4. O que significa a indicação geral 'Ra 6,3 (√)' perto da legenda?
>
> > [!success]- Resposta
> >
> > Que todas as superfícies **sem indicação própria** devem ter Ra máximo de 6,3 µm, e que **há superfícies com indicação individual** no desenho (o símbolo entre parênteses). Ver [[Símbolos de acabamento]].

> [!question] 5. No torneamento, o que acontece com o Ra teórico se o avanço dobrar? E se o raio de ponta dobrar?
>
> > [!success]- Resposta
> >
> > Como $Ra \approx 0{,}032\,f^2/r$: dobrar o **avanço** multiplica o Ra por **4**; dobrar o **raio de ponta** divide o Ra por **2**. Ver [[Rugosidade por processo]].

> [!question] 6. Qual processo você escolheria para obter Ra 0,4 num eixo de aço? E para Ra 3,2?
>
> > [!success]- Resposta
> >
> > Ra 0,4: **retificação** (torneamento fino pode chegar perto, mas sem garantia). Ra 3,2: **torneamento de acabamento** comum. Ver [[Rugosidade por processo]].

> [!question] 7. Por que a pista de um retentor de lábio deve ser retificada de mergulho, e não torneada?
>
> > [!success]- Resposta
> >
> > Porque o torneamento (e a retificação com avanço axial) deixa **marcas helicoidais**, que funcionam como uma rosca e **bombeiam** o fluido para fora através do lábio, causando vazamento. A retificação de mergulho deixa marcas só circunferenciais. Ver [[Rugosidade pela função]].

> [!question] 8. Como o acabamento superficial entra no cálculo de fadiga de um eixo?
>
> > [!success]- Resposta
> >
> > Pelo **fator de superfície** $k_a = a\,S_{ut}^{\,b}$, que reduz o limite de fadiga do corpo de prova polido. Quanto mais rugosa a superfície e mais resistente o aço, menor o $k_a$. Ver [[Rugosidade pela função]].

> [!question] 9. Qual cut-off (λc) e comprimento de avaliação usar para medir uma superfície com Ra esperado de 1,6 µm?
>
> > [!success]- Resposta
> >
> > **λc = 0,8 mm** e comprimento de avaliação de **4 mm** (5 × λc). Ver [[Medição de rugosidade]].

> [!question] 10. Em que direção se mede a rugosidade de uma superfície torneada? Por quê?
>
> > [!success]- Resposta
> >
> > Na direção **perpendicular às marcas**, ou seja, **axial** num eixo torneado. Ao longo das marcas, a rugosidade aparente é muito menor que a real. Ver [[Medição de rugosidade]].

