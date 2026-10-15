---
title: Projeções ortográficas (1º e 3º diedro)
tags: [desenho-tecnico, vistas]
fontes: [ABNT NBR 10067:1995, ISO 128-30 (vistas), ISO 5456-2 (projeções ortográficas), French e Vierck Desenho Técnico e Tecnologia Gráfica (cap. de projeções ortográficas), Silva et al. Desenho Técnico Moderno (cap. de vistas), Telecurso 2000 Leitura e Interpretação de Desenho Técnico Mecânico]
status: rascunho
---

**Resumo:** a projeção ortográfica representa uma peça 3D por meio de vistas 2D, cada uma olhando a peça de frente para uma de suas faces. A posição das vistas na folha depende do método: no **1º diedro** (padrão no Brasil e na Europa) a vista de cima fica **embaixo** da vista frontal; no **3º diedro** (padrão nos EUA) ela fica **em cima**.

## O que é

Imagine a peça dentro de uma caixa de vidro. Olhando **perpendicularmente** para cada face da caixa, você vê uma vista da peça, sem perspectiva: linhas paralelas continuam paralelas e as medidas na direção da vista aparecem em verdadeira grandeza. Essa é a **projeção ortográfica** ("orto" = reto, perpendicular).

São seis vistas possíveis. A NBR 10067 identifica cada uma por uma letra:

| Letra | Vista | Direção de observação |
|---|---|---|
| A | Frontal (principal) | De frente |
| B | Superior | De cima |
| C | Lateral esquerda | Da esquerda |
| D | Lateral direita | Da direita |
| E | Inferior | De baixo |
| F | Posterior | De trás |

### O que é um diedro

Dois planos perpendiculares (um vertical e um horizontal) dividem o espaço em quatro regiões, os **diedros**. A diferença entre os métodos é **onde a peça fica em relação aos planos de projeção**:

- **1º diedro:** a peça fica **entre o observador e o plano**. A vista é "empurrada" para o plano que está **atrás** da peça. Resultado: o que se vê de cima é desenhado **embaixo**; o que se vê da esquerda é desenhado à **direita**.
- **3º diedro:** o plano fica **entre o observador e a peça**, como uma janela. A vista é desenhada na janela pela qual se olha. Resultado: o que se vê de cima é desenhado **em cima**; o que se vê da esquerda é desenhado à **esquerda**.

### Posição das vistas na folha

Em torno da vista frontal (A):

**1º diedro**

|   |   |   |   |
|---|---|---|---|
|   | **E** (inferior) |   |   |
| **D** (lat. direita) | **A** (frontal) | **C** (lat. esquerda) | **F** (posterior) |
|   | **B** (superior) |   |   |

**3º diedro**

|   |   |   |   |
|---|---|---|---|
|   | **B** (superior) |   |   |
| **C** (lat. esquerda) | **A** (frontal) | **D** (lat. direita) | **F** (posterior) |
|   | **E** (inferior) |   |   |

A vista posterior (F) pode ser colocada tanto à direita quanto à esquerda do conjunto.

**Como lembrar:** no 3º diedro cada vista fica do lado de onde foi observada (é o mais intuitivo). No 1º diedro é o contrário: cada vista fica do lado **oposto** ao de onde foi observada.

### Correspondência entre vistas

As vistas estão **alinhadas**: a frontal e a superior têm a mesma largura e ficam na mesma vertical; a frontal e as laterais têm a mesma altura e ficam na mesma horizontal. Por isso se diz que "a largura vem da frontal e da superior, a altura vem da frontal e da lateral, a profundidade vem da superior e da lateral". É essa correspondência que permite reconstruir mentalmente a peça.

### Símbolo do método

O método usado é indicado na [[Legenda]] por um **símbolo normalizado**: um tronco de cone desenhado em duas vistas (um trapézio e dois círculos concêntricos). A posição dos círculos em relação ao trapézio mostra se o desenho está no 1º ou no 3º diedro. ⚠️ verificar o desenho exato do símbolo na NBR 10067 / ISO 5456-2 e copiar o bloco oficial do *template* da empresa, em vez de desenhá-lo de memória.

## Por que importa no projeto

- **É a base de todo desenho de fabricação.** Cotas, tolerâncias, cortes e acabamentos são aplicados sobre as vistas ortográficas.
- **Evita fabricar a peça espelhada.** Ler um desenho do 3º diedro como se fosse do 1º troca as vistas laterais de lugar, e um furo que está à direita é feito à esquerda. Isso é comum com equipamentos e catálogos americanos (redutores, acoplamentos, bombas) usados nas usinas.
- **Escolher bem as vistas economiza trabalho.** Um eixo precisa de uma vista só (com o símbolo de diâmetro); desenhar três vistas de um eixo só ocupa espaço e cria cotas duplicadas.

## Como aplicar (passo a passo / regras práticas)

1. **Escolha a vista frontal:** deve ser a que **mais mostra a forma** da peça, com o menor número de arestas ocultas. Sempre que possível, coloque a peça na **posição de trabalho** (como é montada) ou na **posição de fabricação** (como é usinada; eixos na horizontal, como no torno).
2. **Escolha o mínimo de vistas** que defina a peça sem ambiguidade:
   - **Uma vista:** peças de revolução (eixos, pinos, buchas), usando o símbolo Ø nas cotas, ou peças planas de espessura constante, indicando a espessura numa nota.
   - **Duas vistas:** a maioria das peças simples (flanges, tampas, chapas dobradas).
   - **Três vistas:** peças prismáticas com detalhes em várias faces (blocos, suportes, carcaças).
3. **Posicione as vistas pelo método da legenda** (1º diedro, no Brasil) e mantenha o alinhamento entre elas.
4. **Use cortes** quando o interior tiver muitos detalhes, em vez de encher a vista de tracejadas. Ver [[Tipos de linha]].
5. **Use vistas auxiliares ou parciais** para faces inclinadas, que nas vistas principais aparecem deformadas.
6. **Confira o símbolo do diedro** de todo desenho que vier de fora (fornecedor, catálogo, cliente) antes de ler.
7. **Em CAD 3D**, confira a configuração de projeção do *template* de detalhamento. Alguns programas vêm com o 3º diedro como padrão em *templates* ANSI. ⚠️ verificar no seu programa (SolidWorks, Inventor etc.).

## Norma relacionada

- **ABNT NBR 10067:1995**, *Princípios gerais de representação em desenho técnico*: define as vistas, suas denominações e posições, e admite o 1º e o 3º diedro, com o método indicado na legenda. Baseada na ISO 128 de 1982. ⚠️ verificar a edição vigente e se a ABNT recomenda o 1º diedro como preferencial.
- **ISO 5456-2**: métodos de projeção ortográfica e símbolos.
- **ISO 128-30**: convenções básicas para vistas.

## Exemplo prático

**Situação:** detalhar a **caixa de mancal (chumaceira) de um rolo de moenda**, uma peça fundida que apoia o munhão do eixo, com furo para a bucha, abas para os parafusos de fixação no castelo e furo de lubrificação no topo.

**Escolha das vistas:**

1. **Vista frontal (A):** olhando ao longo do eixo do rolo. Mostra o furo da bucha como um círculo, o perfil externo e as abas. É a vista que mais informa sobre a forma.
2. **Vista superior (B):** mostra a posição dos furos das abas e do furo de lubrificação. No 1º diedro, vai **embaixo** da frontal.
3. **Vista lateral:** quase não acrescenta informação além de um contorno retangular com muitas tracejadas (bucha e furos). Em vez dela, faz-se um **corte A–A** pelo plano vertical do eixo, que mostra a espessura das paredes, o comprimento da bucha e o canal de lubrificação. O corte é posicionado onde ficaria a vista lateral correspondente.

**Erro a evitar aqui:** se esse mancal for comprado de um fabricante americano, o desenho do catálogo estará provavelmente no 3º diedro. A vista superior aparecerá **em cima** da frontal. Lida como 1º diedro, a posição do furo de lubrificação seria interpretada como estando embaixo, um erro que só aparece na montagem.

> [!question] Exercício 1
>
> Você recebe um desenho de catálogo em que a vista lateral direita está desenhada à direita da vista frontal e a vista superior está acima dela. Em que diedro está o desenho?
>
> > [!success]- Resolução
> >
> > **3º diedro.** No 3º diedro cada vista fica do mesmo lado de onde foi observada: a superior em cima e a lateral direita à direita. No 1º diedro seria o contrário.

> [!question] Exercício 2
>
> Um bloco tem um furo passante vertical (de cima a baixo). Como esse furo aparece na vista frontal e na vista superior, no 1º diedro?
>
> > [!success]- Resolução
> >
> > - **Vista superior** (desenhada abaixo da frontal): o furo aparece como um **círculo** em linha contínua larga, com linhas de centro cruzadas.
> > - **Vista frontal:** o furo está dentro do bloco, então aparece como **duas linhas tracejadas verticais** (as geratrizes do furo), com uma linha de centro traço e ponto entre elas.

## Erros comuns

- **Misturar os métodos:** colocar a vista superior em cima e a lateral esquerda à direita no mesmo desenho.
- **Vistas desalinhadas**, que impedem a leitura por correspondência.
- **Excesso de vistas**: três vistas de um eixo cilíndrico.
- **Vista frontal mal escolhida**, mostrando a face com menos detalhes e obrigando a usar muitas tracejadas nas outras.
- **Omitir o símbolo do diedro**, deixando o leitor adivinhar o método.
- **Copiar vistas de um catálogo estrangeiro** para um desenho brasileiro sem reposicioná-las.

## Ver também

- [[Tipos de linha]]
- [[Legenda]]
- [[Escalas]]
- [[01-desenho-tecnico/index|Índice do módulo 01]]
