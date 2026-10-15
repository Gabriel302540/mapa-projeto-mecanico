---
title: Perspectivas
tags: [desenho-tecnico, perspectivas]
fontes: [ABNT NBR 8403 e NBR 10067 (históricas), ISO 5456-3 (representações axonométricas), French e Vierck Desenho Técnico e Tecnologia Gráfica (cap. de desenho axonométrico e oblíquo), Silva et al. Desenho Técnico Moderno (cap. de perspectivas)]
status: rascunho
---

**Resumo:** perspectivas mostram a peça em três dimensões numa única imagem. Em desenho técnico usam-se perspectivas paralelas (sem ponto de fuga), principalmente a isométrica e a cavaleira. Servem para entender a forma, não para fabricar: as medidas vêm sempre das vistas ortográficas.

## O que é

Uma perspectiva representa as três dimensões da peça (largura, altura e profundidade) num só desenho. As usadas em engenharia são **perspectivas paralelas**: as linhas paralelas na peça continuam paralelas no desenho, o que permite medir ao longo dos eixos.

### Isométrica

- Os três eixos (largura, altura, profundidade) aparecem a **120°** entre si; o eixo vertical fica vertical e os outros dois a **30°** da horizontal.
- Os três eixos sofrem a **mesma redução**. Na projeção isométrica verdadeira, o fator é $\sqrt{2/3} \approx 0{,}816$.
- Na prática, faz-se o **desenho isométrico**, com as medidas reais (fator 1) nos três eixos. A imagem fica cerca de 22 % maior, mas com a mesma forma, e fica muito mais fácil de desenhar.
- **Círculos** viram **elipses** em todas as faces.

### Cavaleira (oblíqua)

- A face frontal é desenhada em **verdadeira grandeza**, igual à vista frontal.
- A profundidade é desenhada num eixo inclinado (normalmente 45°, também 30° ou 60°), com redução para não parecer "esticada": é comum usar **1/2** (perspectiva de gabinete) ou 2/3.
- Vantagem: **círculos da face frontal continuam círculos**. Ótima para peças com muitos furos ou arcos numa face.

### Dimétrica e trimétrica

Variações em que dois (dimétrica) ou três (trimétrica) eixos têm escalas diferentes. Dão aparência mais natural, mas são mais trabalhosas à mão. Em CAD 3D, qualquer orientação é obtida girando o modelo.

### Comparação

| Perspectiva | Ângulos dos eixos | Escalas | Ponto forte |
|---|---|---|---|
| Isométrica | 30° / 30° / vertical | Iguais nos três eixos | Visão equilibrada, todas as faces com a mesma importância |
| Cavaleira | Frontal em VG + fuga a 45° | Profundidade reduzida (1/2 ou 2/3) | Face frontal sem deformação; círculos fáceis |
| Dimétrica | Dois ângulos iguais | Duas escalas | Aparência mais natural |

## Por que importa no projeto

- **Comunicação:** perspectivas ajudam quem não lê vistas com facilidade (montadores, compradores, manutenção) a entender a peça ou o conjunto.
- **Desenhos de montagem e manuais:** a **vista explodida** em perspectiva mostra a ordem de montagem das peças.
- **Croquis rápidos:** na discussão de uma solução, uma perspectiva isométrica à mão livre é o jeito mais rápido de mostrar uma ideia.
- **Leitura de desenho:** treinar perspectivas desenvolve a visão espacial necessária para ler [[Projeções ortográficas|vistas ortográficas]].

## Como aplicar (passo a passo / regras práticas)

1. **Desenhe a "caixa envolvente"** da peça nos três eixos, com as medidas máximas.
2. **Recorte a caixa:** marque as faces, rebaixos e chanfros medindo **sempre ao longo dos eixos**. Medidas inclinadas na peça não podem ser transferidas diretamente; localize os extremos pelos eixos.
3. **Círculos:** na isométrica, construa a elipse dentro de um quadrado isométrico (losango) do tamanho do diâmetro. Na cavaleira, desenhe-os em verdadeira grandeza na face frontal.
4. **Não use tracejadas** em perspectiva, salvo se indispensáveis.
5. **Não cote perspectivas** para fabricação. Se cotar, é só para referência.
6. **Em CAD 3D,** gere a vista isométrica do modelo e, para montagens, a vista explodida com balões de numeração.

## Norma relacionada

- **ISO 5456-3**: representações axonométricas (isométrica, dimétrica, trimétrica). **ISO 5456-2** trata das ortográficas.
- No Brasil, as perspectivas aparecem nas normas gerais de representação. ⚠️ verificar se há norma ABNT específica vigente.

## Exemplo prático

**Situação:** instrução de manutenção para a **troca do rolamento de um mancal**: o montador precisa ver a ordem das peças (tampa, retentor, porca de fixação, arruela de trava, rolamento, bucha de fixação, caixa do mancal).

- Uma **vista explodida em isométrica**, com as peças afastadas ao longo do eixo na ordem de montagem.
- Cada peça com um **balão numerado** correspondente à lista de peças.
- As medidas e tolerâncias continuam nos desenhos de detalhe; a perspectiva só mostra a sequência.

> [!question] Exercício
>
> Um cubo de 100 mm de aresta é desenhado em isométrica. Qual o comprimento das arestas no desenho isométrico (medidas reais) e na projeção isométrica verdadeira?
>
> > [!success]- Resolução
> >
> > - **Desenho isométrico:** usa-se a medida real, **100 mm** em cada eixo.
> > - **Projeção isométrica verdadeira:** $100 \times \sqrt{2/3} \approx 81{,}6$ mm.
> >
> > As duas imagens têm a mesma forma; só o tamanho muda. Por isso, na prática, usa-se o desenho isométrico.

## Erros comuns

- **Medir ao longo de linhas inclinadas** da peça em vez de ao longo dos eixos.
- **Desenhar círculos como círculos** nas faces da isométrica (devem ser elipses).
- **Cavaleira sem redução da profundidade**, que deixa a peça com aparência alongada.
- **Usar a perspectiva como desenho de fabricação.**

## Ver também

- [[Projeções ortográficas]]
- [[Desenho de conjunto e de detalhe]]
- [[01-desenho-tecnico/index|Índice do módulo 01]]
