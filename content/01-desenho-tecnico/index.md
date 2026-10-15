---
title: 01 · Desenho técnico
tags: [indice, desenho-tecnico]
---

**Resumo:** A linguagem do projeto: como representar uma peça de forma que qualquer pessoa da fábrica entenda exatamente o que fabricar.

## Por que este módulo importa
Todo o resto do site depende disto. Um desenho ambíguo vira peça errada, retrabalho e parada de máquina. Na moenda, um desenho de detalhe de eixo ou de bagaceira mal cotado chega à oficina e volta como dúvida, ou pior, como peça fora de medida.

## Tópicos
Ordem sugerida de estudo: de cima para baixo.

- [x] [[Formatos de folha|Formatos e folhas de desenho]]
- [x] [[Legenda|Legenda (carimbo)]]
- [x] [[Tipos de linha]]
- [x] [[Caligrafia técnica]]
- [x] [[Escalas]]
- [x] [[Projeções ortográficas|Projeções ortográficas (1º e 3º diedro)]]
- [x] [[Escolha de vistas]]
- [x] [[Vistas auxiliares]]
- [x] [[Cortes e seções]]
- [x] [[Hachuras]]
- [x] [[Cotagem|Cotagem: princípios]]
- [x] [[Cotagem de elementos|Cotagem: furos, raios, chanfros e roscas]]
- [x] [[Representação de roscas]]
- [x] [[Perspectivas]]
- [x] [[Desenho de conjunto e de detalhe]]

## Normas principais
Lista de partida, para conferir no documento original. Nenhum trecho de norma é reproduzido aqui.

- ABNT NBR 16752:2020 — apresentação em folhas de desenho (formatos, legenda, dobramento e escalas); substituiu a NBR 10582 ⚠️ verificar se também cancelou a NBR 10068 e a NBR 13142
- ABNT NBR 16861:2020 — linhas e escrita; substituiu a NBR 8403 ⚠️ verificar se também substituiu a NBR 8402
- ABNT NBR 10067 — princípios gerais de representação
- ABNT NBR 10126 — cotagem
- ABNT NBR 8196 — escalas ⚠️ verificar: indicada como cancelada em 2016, com o assunto agora na NBR 16752
- ABNT NBR 12298 — hachuras
- ISO 128 (série) — princípios gerais de representação (128-2 linhas, 128-30 vistas)
- ISO 216 e ISO 5457 — formatos e leiaute da folha
- ISO 5455 — escalas
- ISO 5456-2 — projeções ortográficas
- ISO 129-1 — cotagem
- ISO 7200 — campos da legenda

## Módulos relacionados
- [[02-tolerancias-ajustes/index|02 · Tolerâncias e ajustes]]
- [[05-elementos-de-maquinas/index|05 · Elementos de máquinas]]
- [[10-cad/index|10 · CAD]]

## Revisão rápida

Tente responder antes de abrir a resposta.

> [!question] 1. Por que uma folha A1 cortada ao meio resulta exatamente numa A2, com a mesma proporção?
>
> > [!success]- Resposta
> >
> > Porque a série A usa a proporção $\sqrt{2}$ entre os lados. Cortando a folha ao meio no lado maior, os novos lados são $b$ e $a/2$, e $b/(a/2) = 2b/a = 2/\sqrt{2} = \sqrt{2}$. A proporção se mantém. Ver [[Formatos de folha]].

> [!question] 2. Quais informações da legenda impedem que a oficina fabrique uma versão desatualizada da peça?
>
> > [!success]- Resposta
> >
> > O **número do desenho** e a **revisão**, junto com o **quadro de revisões** que registra o que mudou em cada versão. Ver [[Legenda]].

> [!question] 3. Que tipo de linha representa: (a) aresta oculta, (b) linha de centro, (c) peça vizinha num desenho de detalhe, (d) plano de corte?
>
> > [!success]- Resposta
> >
> > (a) Tracejada; (b) traço e ponto estreita; (c) traço e dois pontos estreita; (d) traço e ponto estreita, larga nas extremidades e nas mudanças de direção, com setas e letras. Ver [[Tipos de linha]].

> [!question] 4. Um eixo de 600 mm é desenhado em escala 1:5. Quanto ele mede no papel e qual valor é escrito na cota?
>
> > [!success]- Resposta
> >
> > No papel: $600/5 = 120$ mm. A cota escrita é **600**, porque a cota é sempre o valor real. Ver [[Escalas]].

> [!question] 5. No 1º diedro, onde fica a vista superior em relação à frontal? E no 3º diedro?
>
> > [!success]- Resposta
> >
> > No **1º diedro**, a vista superior fica **abaixo** da frontal. No **3º diedro**, fica **acima**. Ver [[Projeções ortográficas]].

> [!question] 6. Quantas vistas são necessárias para definir um eixo escalonado com dois rasgos de chaveta? Que recursos complementam essa vista?
>
> > [!success]- Resposta
> >
> > **Uma vista** longitudinal, com cotas de diâmetro (Ø). Complementam: **seções transversais** nos rasgos (para a profundidade) e **detalhes ampliados** dos raios de concordância. Ver [[Escolha de vistas]] e [[Cortes e seções]].

> [!question] 7. Num corte longitudinal de um conjunto, por que o eixo e os parafusos não são hachurados?
>
> > [!success]- Resposta
> >
> > Porque são peças maciças, sem detalhes internos; cortá-los não acrescenta informação e confunde a leitura. A convenção é representá-los inteiros em cortes longitudinais. Ver [[Cortes e seções]].

> [!question] 8. Quatro furos estão cotados em cadeia, com três intervalos de ±0,1 mm. Qual o erro máximo da posição do último furo em relação ao primeiro? Como reduzir esse erro sem apertar as tolerâncias?
>
> > [!success]- Resposta
> >
> > Pior caso: $3 \times 0{,}1 = \pm 0{,}3$ mm. Para reduzir sem apertar as tolerâncias, **cote em paralelo** (todas as posições a partir do primeiro furo ou de uma referência comum), e cada posição fica com só ±0,1 mm. Ver [[Cotagem]].

> [!question] 9. Como se cota a profundidade de um rasgo de chaveta num eixo de Ø40 com $t_1 = 5$ mm? Por quê?
>
> > [!success]- Resposta
> >
> > Cota-se $d - t_1 = 40 - 5 = 35$ mm, do fundo do rasgo até a geratriz oposta do eixo, porque é uma medida que se consegue tomar com paquímetro ou micrômetro entre duas superfícies. Ver [[Cotagem de elementos]].

> [!question] 10. Na representação de uma rosca externa M20, qual diâmetro é desenhado em linha larga e qual em linha estreita? Na vista de topo, como aparece o fundo da rosca?
>
> > [!success]- Resposta
> >
> > A **crista** (Ø20) em linha **larga** e o **fundo** (≈ Ø17) em linha **estreita**. Na vista de topo, o fundo aparece como um **arco de cerca de 3/4 de circunferência** em linha estreita. Ver [[Representação de roscas]].

