---
title: 02 · Tolerâncias e ajustes
tags: [indice, tolerancias]
---

**Resumo:** Nenhuma peça sai com a medida exata. Tolerância é o quanto a medida pode variar; ajuste é o resultado de montar um furo com um eixo.

## Por que este módulo importa
Define se o rolamento entra no eixo com interferência ou se a bucha gira livre. Tolerância apertada demais encarece a usinagem; folgada demais gera folga, vibração e desgaste.

## Tópicos
Ordem sugerida de estudo: de cima para baixo.

- [x] [[Conceitos de tolerância|Dimensão nominal, desvios e tolerância]]
- [x] [[Graus IT|Graus de tolerância IT]]
- [x] [[Posições de tolerância|Posições de tolerância (letras)]]
- [x] [[Sistema furo-base]]
- [x] [[Sistema eixo-base]]
- [x] [[Tipos de ajuste|Tipos de ajuste: folga, incerto e interferência]]
- [x] [[Ajustes recomendados|Ajustes recomendados por aplicação]]
- [x] [[Tolerâncias gerais]]
- [x] [[Empilhamento de tolerâncias|Cadeia de tolerâncias (empilhamento)]]
- [x] [[Indicação de tolerâncias|Indicação de tolerâncias no desenho]]

## Normas principais
Lista de partida, para conferir no documento original. Nenhum trecho de norma é reproduzido aqui.

- ISO 286-1 e ISO 286-2 — sistema ISO de tolerâncias e ajustes
- ABNT NBR 6158 — sistema de tolerâncias e ajustes ⚠️ verificar edição vigente
- ISO 2768-1 — tolerâncias gerais lineares e angulares

## Módulos relacionados
- [[01-desenho-tecnico/index|01 · Desenho técnico]]
- [[03-gdt/index|03 · GD&T]]
- [[05-elementos-de-maquinas/index|05 · Elementos de máquinas]]

## Revisão rápida

Tente responder antes de abrir a resposta.

> [!question] 1. Qual a diferença entre desvio e tolerância? Um deles pode ser negativo?
>
> > [!success]- Resposta
> >
> > O **desvio** é a diferença entre um limite e a dimensão nominal e pode ser positivo, negativo ou zero. A **tolerância** é a diferença entre os limites máximo e mínimo (desvio superior − desvio inferior) e é sempre positiva. Ver [[Conceitos de tolerância]].

> [!question] 2. Na classe Ø40 g6, o que indica a letra e o que indica o número?
>
> > [!success]- Resposta
> >
> > A **letra g** (minúscula, eixo) indica a **posição** da faixa: abaixo da linha zero, com $es = -9$ µm para Ø40. O **número 6** indica o **grau IT6**, ou seja, o tamanho da faixa: 16 µm para Ø40. Ver [[Posições de tolerância]] e [[Graus IT]].

> [!question] 3. Por que, nos ajustes de precisão, o furo costuma ter um grau IT a mais que o eixo (H7 com eixo 6)?
>
> > [!success]- Resposta
> >
> > Porque furos são mais difíceis de fabricar e de medir com precisão do que eixos. Dar um grau a mais ao furo equilibra a dificuldade de fabricação das duas peças. Ver [[Graus IT]].

> [!question] 4. Por que o sistema furo-base é o mais usado?
>
> > [!success]- Resposta
> >
> > Porque furos de precisão são feitos com ferramentas de diâmetro fixo (alargadores, brochas) e verificados com calibradores tampão. Fixando o furo em H, uma ferramenta e um calibrador servem para todos os ajustes daquele diâmetro; o ajuste é obtido variando o eixo, que é fácil de ajustar no torno ou na retífica. Ver [[Sistema furo-base]].

> [!question] 5. Cite duas situações em que o sistema eixo-base é mais vantajoso.
>
> > [!success]- Resposta
> >
> > (1) Quando o eixo é uma **barra calibrada** comprada pronta (h9, h11). (2) Quando um **eixo liso** recebe várias peças com ajustes diferentes. Também em peças padronizadas como **chavetas** (largura h9) e pinos. Ver [[Sistema eixo-base]].

> [!question] 6. Calcule a folga máxima e mínima de um ajuste Ø50 H7/g6 (IT7 = 25 µm, IT6 = 16 µm, g: es = −9 µm).
>
> > [!success]- Resposta
> >
> > Furo: 50,000 a 50,025. Eixo: 49,975 a 49,991. $F_{\max} = 50{,}025 - 49{,}975 = 50$ µm; $F_{\min} = 50{,}000 - 49{,}991 = 9$ µm. Ajuste **com folga**. Ver [[Tipos de ajuste]].

> [!question] 7. Num rolamento cujo eixo gira e a carga tem direção fixa, qual anel deve ter ajuste com interferência e por quê?
>
> > [!success]- Resposta
> >
> > O **anel interno**, porque ele gira em relação à direção da carga. Com folga, ele desliza (*creep*) e desgasta o assento. O anel externo, parado em relação à carga, pode ter ajuste com folga ou incerto (H7). Ver [[Ajustes recomendados]].

> [!question] 8. O que significa a nota 'ISO 2768-m' e qual a tolerância de uma cota de 250 mm nessa classe?
>
> > [!success]- Resposta
> >
> > É a **tolerância geral** para cotas sem tolerância individual, classe média. Para 250 mm (faixa > 120 a 400): **±0,5 mm**. Ver [[Tolerâncias gerais]].

> [!question] 9. Uma cadeia tem quatro cotas com ±0,05, ±0,08, ±0,10 e ±0,02 mm. Qual a variação da resultante pelo pior caso e pelo RSS?
>
> > [!success]- Resposta
> >
> > Pior caso: $0{,}05 + 0{,}08 + 0{,}10 + 0{,}02 = \pm 0{,}25$ mm. RSS: $\sqrt{0{,}0025 + 0{,}0064 + 0{,}01 + 0{,}0004} = \sqrt{0{,}0193} \approx \pm 0{,}14$ mm. Ver [[Empilhamento de tolerâncias]].

> [!question] 10. No desenho de conjunto aparece 'Ø60 H7/k6'. O que deve aparecer no desenho de detalhe do eixo e no do cubo?
>
> > [!success]- Resposta
> >
> > No **eixo**: Ø60 k6 (de preferência com os desvios entre parênteses). No **cubo**: Ø60 H7. Cada desenho de detalhe traz a classe da própria peça; o ajuste completo fica no conjunto. Ver [[Indicação de tolerâncias]].

