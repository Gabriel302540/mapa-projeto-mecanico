---
title: Tipos de linha
tags: [desenho-tecnico, linhas]
fontes: [ABNT NBR 16861:2020, ISO 128-2, ISO 128-24 (desenho mecânico), French e Vierck Desenho Técnico e Tecnologia Gráfica (cap. de linhas e técnicas de desenho), Telecurso 2000 Leitura e Interpretação de Desenho Técnico Mecânico]
status: rascunho
---

**Resumo:** cada tipo de linha num desenho técnico tem um significado. Contínua larga é aresta visível, tracejada é aresta oculta, traço e ponto é linha de centro, e assim por diante. Saber ler e aplicar as linhas é o que permite entender a forma da peça sem ambiguidade.

## O que é

Um desenho técnico usa poucas linhas, mas cada uma é uma "palavra" com significado fixo. Elas se diferenciam por duas características:

1. **Traçado:** contínua, tracejada, traço e ponto, traço e dois pontos, à mão livre ou em ziguezague.
2. **Largura (espessura):** **larga** ou **estreita**. A larga tem o dobro da largura da estreita.

### As linhas usadas em desenho mecânico

| Linha | Aspecto | Onde se usa |
|---|---|---|
| **Contínua larga** | ━━━━━━ | Arestas e contornos **visíveis**; quadro da folha |
| **Contínua estreita** | ────── | Linhas de cota e de chamada (auxiliares); hachuras; linhas de centro curtas; fundo de rosca; contorno de seção rebatida; diagonais que indicam face plana |
| **Contínua estreita à mão livre** ou **em ziguezague** | 〰〰〰 | Limite de vista parcial, de corte parcial ou de peça interrompida |
| **Tracejada** | ─ ─ ─ ─ | Arestas e contornos **não visíveis** (ocultos) |
| **Traço e ponto estreita** | ── · ── · ── | **Linhas de centro**, eixos de simetria, círculos de furação (diâmetro primitivo), trajetórias |
| **Traço e ponto estreita, larga nas pontas e nas mudanças de direção** | ━━ · ── · ━━ | **Plano de corte**, indicado com letras e setas (A–A) |
| **Traço e ponto larga** | ━━ · ━━ · ━━ | Superfícies com **requisito especial** (por exemplo, região com tratamento térmico localizado) |
| **Traço e dois pontos estreita** | ── ·· ── ·· ── | Contorno de **peças vizinhas**; **posições extremas** de partes móveis; contorno da peça antes da conformação; linha de centro de gravidade |

Na versão antiga da norma brasileira (NBR 8403) a tracejada tinha versões larga e estreita. Na prática de desenho mecânico atual usa-se uma só. ⚠️ verificar na NBR 16861 a classificação e a numeração dos tipos de linha.

### Larguras

As larguras seguem uma série em que cada valor é cerca de $\sqrt{2}$ vezes o anterior, a mesma lógica dos [[Formatos de folha|formatos de folha]]. Assim, ao reduzir um A1 para A3, uma linha de 0,5 mm vira 0,25 mm, que também é um valor da série:

$$
0{,}13 \;\to\; 0{,}18 \;\to\; 0{,}25 \;\to\; 0{,}35 \;\to\; 0{,}5 \;\to\; 0{,}7 \;\to\; 1{,}0 \;\to\; 1{,}4 \;\to\; 2{,}0\ \text{mm}
$$

Em desenho mecânico, o par mais usado é **0,5 mm (larga) com 0,25 mm (estreita)**, ou **0,7 mm com 0,35 mm** em folhas grandes. ⚠️ verificar na NBR 16861 a série de larguras e a razão entre larga e estreita.

### Prioridade quando as linhas coincidem

Muitas vezes duas linhas caem no mesmo lugar, por exemplo uma aresta visível na frente de uma aresta oculta. Desenha-se só a de **maior prioridade**:

1. Aresta e contorno visível (contínua larga)
2. Aresta e contorno oculto (tracejada)
3. Plano de corte
4. Linha de centro (traço e ponto)
5. Linha de centro de gravidade (traço e dois pontos)
6. Linha de chamada (contínua estreita)

## Por que importa no projeto

- **É assim que se lê a forma da peça.** Um furo cego aparece na vista lateral como duas tracejadas paralelas mais o cone da ponta da broca. Se a tracejada for desenhada como contínua, a pessoa da oficina entende que é um rasgo passante.
- **Linha de centro define a referência de medição.** Furos de um flange são localizados pelo círculo de furação (traço e ponto). Sem ele, cada um mede de um lugar diferente.
- **Legibilidade em cópias reduzidas.** Com contraste certo entre linha larga e estreita, o contorno da peça "salta" aos olhos e as cotas ficam em segundo plano, mesmo numa cópia A3 de um desenho A1.
- **Desenho de conjunto.** O traço e dois pontos mostra as peças vizinhas (por exemplo, a posição do rolo em relação à bagaceira) sem que elas façam parte do desenho daquela peça.

## Como aplicar (passo a passo / regras práticas)

1. **Defina o par de larguras pela folha:** 0,5/0,25 mm para A2 a A4 e 0,7/0,35 mm para A0 e A1 é uma regra prática comum. Em CAD, isso é feito por **layer**: um layer por tipo de linha, com cor e espessura definidas. Ver [[10-cad/index|CAD]].
2. **Desenhe primeiro as linhas de centro** de furos, eixos e simetrias. Elas devem passar alguns milímetros (2 a 5 mm é usual) além do contorno, e não terminar exatamente na aresta.
3. **Linhas de centro se cruzam em traços**, nunca em pontos ou em espaços: o cruzamento marca o centro do furo.
4. **Tracejadas: só as necessárias.** Mostre arestas ocultas quando ajudarem a entender a peça. Se houver muitas, faça um **corte** (ver [[01-desenho-tecnico/index|Cortes e seções]] no índice do módulo).
5. **Tracejada que continua uma contínua começa com um espaço**, para deixar claro onde termina a aresta visível. Quando uma tracejada encontra outra num canto, as duas se tocam com traços.
6. **Espaçamento mínimo entre linhas paralelas:** deixe pelo menos duas vezes a largura da linha mais larga (na prática, não menos que 0,7 mm), para que não se fundam na impressão. ⚠️ verificar o valor na NBR 16861.
7. **Plano de corte:** traço e ponto estreita, com trechos largos nas extremidades, setas indicando a direção de observação e letras (A–A).

## Norma relacionada

- **ABNT NBR 16861:2020**, *Desenho técnico: requisitos para representação de linhas e escrita*. Define tipos de linha, larguras e a escrita (caligrafia técnica). Substituiu a **NBR 8403** (cancelada em 01/2021) e foi confirmada pela ABNT em 2025. ⚠️ verificar se também substituiu a NBR 8402 (caracteres para escrita).
- **ISO 128-2** (convenções básicas para linhas) e **ISO 128-24** (linhas em desenho mecânico): referências internacionais equivalentes. A ISO 128-24 está sendo substituída por novas partes da ISO 128; ⚠️ verificar a parte vigente.

## Exemplo prático

**Situação:** vista lateral de um **mancal de deslizamento bipartido** de rolo de moenda, com bucha de bronze, furo de lubrificação e parafusos de fechamento da tampa.

Que linha usar em cada elemento:

| Elemento | Linha |
|---|---|
| Contorno externo do corpo do mancal | Contínua larga |
| Diâmetro interno da bucha, visto pela lateral | Tracejada (está dentro do corpo) |
| Eixo de simetria vertical do mancal | Traço e ponto estreita |
| Centro do furo de lubrificação e dos parafusos | Traço e ponto estreita, cruzando nos traços |
| Contorno do eixo do rolo (peça vizinha, não faz parte deste desenho) | Traço e dois pontos estreita |
| Indicação do corte A–A pelo plano dos parafusos | Traço e ponto com extremidades largas, setas e letras |
| Cotas e linhas de chamada | Contínua estreita |

Repare que, sem o corte, a vista lateral teria muitas tracejadas (bucha, canal de óleo, furos dos parafusos) sobrepostas. É o sinal clássico de que um **corte A–A** vai deixar o desenho bem mais claro.

> [!question] Exercício
>
> Numa vista, uma aresta visível coincide com uma linha de centro. Qual delas é desenhada? E se uma aresta oculta coincidir com uma linha de centro?
>
> > [!success]- Resolução
> >
> > Pela ordem de prioridade, desenha-se a **aresta visível** no primeiro caso e a **aresta oculta (tracejada)** no segundo. A linha de centro só aparece nos trechos em que não coincide com nenhuma aresta, ou prolongada além do contorno.

## Erros comuns

- **Linha de centro contínua** ou terminando exatamente na aresta.
- **Cruzar linhas de centro nos espaços ou nos pontos**, deixando o centro do furo indefinido.
- **Todas as linhas com a mesma espessura**, comum em CAD quando todos os objetos ficam num único layer. O desenho perde contraste e fica difícil de ler.
- **Excesso de tracejadas** em vez de usar um corte.
- **Desenhar peça vizinha com linha contínua larga**, o que faz parecer que ela faz parte da peça.
- **Hachura com linha larga**: a hachura é sempre contínua estreita.

## Ver também

- [[Formatos de folha]]
- [[Projeções ortográficas]] (onde as arestas ocultas aparecem)
- [[Escalas]]
- [[01-desenho-tecnico/index|Índice do módulo 01]]
