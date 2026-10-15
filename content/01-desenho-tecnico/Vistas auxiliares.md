---
title: Vistas auxiliares
tags: [desenho-tecnico, vistas]
fontes: [ABNT NBR 10067:1995, French e Vierck Desenho Técnico e Tecnologia Gráfica (cap. de vistas auxiliares), Silva et al. Desenho Técnico Moderno (cap. de vistas auxiliares)]
status: rascunho
---

**Resumo:** quando uma face da peça é inclinada em relação aos planos de projeção, ela aparece deformada (encurtada) nas vistas normais. A vista auxiliar é uma projeção feita perpendicularmente a essa face, que mostra sua forma e suas medidas em verdadeira grandeza.

## O que é

Nas [[Projeções ortográficas|vistas principais]], uma face só aparece em **verdadeira grandeza (VG)** quando é **paralela** ao plano de projeção. Se a face está inclinada, a vista mostra uma versão "achatada" dela:

- Um furo redondo numa face inclinada aparece como **elipse**.
- Uma aresta de comprimento $L$ inclinada de um ângulo $\alpha$ em relação ao plano de projeção aparece com comprimento $L\cos\alpha$.

A **vista auxiliar** resolve isso criando um **plano de projeção paralelo à face inclinada**. Olhando perpendicularmente para esse plano, a face aparece com a forma e as medidas reais.

### Tipos

- **Vista auxiliar primária:** a face é perpendicular a um dos planos principais (aparece como uma linha inclinada em uma das vistas). É o caso mais comum.
- **Vista auxiliar secundária:** a face é oblíqua a todos os planos principais. Exige primeiro uma vista auxiliar que mostre a face "de topo" e, a partir dela, uma segunda vista auxiliar. Rara em desenho mecânico do dia a dia.
- **Vista auxiliar parcial:** mostra **só** a face inclinada, sem o resto da peça (que apareceria deformado e inútil). É o uso mais comum na prática.

## Por que importa no projeto

- **Permite cotar corretamente.** Cotar o diâmetro de um furo em uma elipse, ou o comprimento de uma aresta encurtada, é impossível ou ambíguo.
- **Mostra a forma real** de abas, suportes e chapas dobradas em ângulo.
- **É comum em caldeiraria:** calhas inclinadas, bicas, tremonhas e chapas de desgaste, que raramente são paralelas aos planos principais.

## Como aplicar (passo a passo / regras práticas)

1. **Encontre a vista em que a face inclinada aparece como uma linha** (de topo). É a partir dela que se projeta.
2. **Trace linhas de projeção perpendiculares a essa linha.** A vista auxiliar fica sobre essas linhas, como se o plano tivesse sido "girado" para ficar de frente.
3. **Transfira as profundidades** de outra vista principal (com compasso ou, em CAD, com linhas de construção). Elas são as distâncias que não aparecem na vista de topo.
4. **Desenhe só a face inclinada** (vista parcial), limitada por linha de interrupção.
5. **Se a vista não puder ficar na posição projetada**, desenhe-a em outro lugar e identifique-a com seta e letra ("VISTA A") na vista de origem.
6. **Cote os elementos da face inclinada só na vista auxiliar**, onde estão em verdadeira grandeza.

Em CAD 3D, a vista auxiliar é gerada automaticamente: basta selecionar a aresta que define a direção de observação.

## Norma relacionada

- **ABNT NBR 10067:1995**: trata das vistas auxiliares e da identificação de vistas fora de posição. ⚠️ verificar edição vigente.

## Exemplo prático

**Situação:** uma **bica de alimentação** de chapa, inclinada a 30° em relação à horizontal, tem na face inclinada um flange retangular de 400 × 250 mm com quatro furos Ø14 para fixação.

- Na vista frontal, a face aparece de topo, como uma linha inclinada a 30°.
- Na vista superior, o comprimento de 400 mm da face aparece encurtado: $400\cos 30° \approx 346$ mm. Os furos aparecem como elipses de eixo menor $14\cos 30° \approx 12{,}1$ mm.
- **Solução:** vista auxiliar parcial projetada perpendicularmente à linha de 30° da vista frontal, mostrando o flange 400 × 250 em VG e os furos como círculos de Ø14, onde são cotados.

> [!question] Exercício
>
> Uma aresta de 250 mm está inclinada a 60° em relação ao plano horizontal e é paralela ao plano frontal. Que comprimento ela tem na vista frontal e na vista superior?
>
> > [!success]- Resolução
> >
> > - **Vista frontal:** a aresta é paralela ao plano frontal, então aparece em **verdadeira grandeza: 250 mm**.
> > - **Vista superior:** ela é projetada no plano horizontal, com o qual faz 60°. Comprimento aparente: $250\cos 60° = 125$ mm.
> >
> > Por isso a cota de 250 deve ser colocada na vista frontal, nunca na superior.

## Erros comuns

- **Cotar a elipse** de um furo em face inclinada, em vez de fazer a vista auxiliar.
- **Desenhar a vista auxiliar completa**, com o resto da peça deformado, quando uma parcial bastaria.
- **Vista auxiliar fora de posição sem seta e letra.**
- **Transferir profundidades da vista errada**, o que gera uma face espelhada.

## Ver também

- [[Projeções ortográficas]]
- [[Escolha de vistas]]
- [[Cortes e seções]]
- [[01-desenho-tecnico/index|Índice do módulo 01]]
