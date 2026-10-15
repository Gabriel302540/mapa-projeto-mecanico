---
title: Cortes e seções
tags: [desenho-tecnico, cortes]
fontes: [ABNT NBR 10067:1995, ABNT NBR 12298:1995, ISO 128-40 e ISO 128-44 (cortes e seções), French e Vierck Desenho Técnico e Tecnologia Gráfica (cap. de vistas em corte), Telecurso 2000 Leitura e Interpretação de Desenho Técnico Mecânico]
status: rascunho
---

**Resumo:** um corte é uma vista em que parte da peça é "removida" por um plano imaginário, para mostrar o interior sem as linhas tracejadas. Uma seção mostra apenas o que fica exatamente no plano de corte. São os recursos mais usados para tornar claros furos, canais, paredes e cavidades.

## O que é

Imagine serrar a peça com um plano, retirar a parte que fica entre você e o plano e olhar o que sobrou. O que você vê é o **corte**. As superfícies que foram "tocadas" pela serra recebem [[Hachuras|hachura]].

**Corte × seção:**

- **Corte:** mostra a superfície cortada **e tudo o que se vê atrás dela**.
- **Seção:** mostra **só a superfície cortada**, como uma "fatia" fina. É usada para mostrar o perfil de braços, nervuras, perfis e rasgos.

### Indicação

O **plano de corte** é marcado na vista onde ele aparece de topo, com linha traço e ponto estreita, **larga nas extremidades e nas mudanças de direção**, setas indicando a direção de observação e letras maiúsculas (A–A, B–B). O corte resultante recebe o título "CORTE A–A". Ver [[Tipos de linha]].

Se o plano de corte coincide com um eixo de simetria e a posição do corte é óbvia, a indicação pode ser omitida. ⚠️ verificar as condições na norma.

### Tipos de corte

| Tipo | Como é | Quando usar |
|---|---|---|
| **Corte total (pleno)** | O plano atravessa a peça inteira. Pode ser longitudinal ou transversal | Peças com interior complexo e não simétricas |
| **Meio corte** | Em peça simétrica, metade é desenhada em corte e metade em vista, separadas pela linha de simetria | Peças simétricas: mostra o exterior e o interior na mesma vista. Na metade em vista, **não** se desenham tracejadas |
| **Corte parcial** | Só uma pequena região é cortada, limitada por linha contínua estreita à mão livre | Para mostrar um detalhe interno isolado (um furo roscado, um canal) sem cortar a peça toda |
| **Corte em desvio (composto)** | O plano muda de direção em degraus, passando por elementos que não estão alinhados | Quando os detalhes estão em planos paralelos diferentes; desenha-se como se fosse um plano único |
| **Corte rebatido (alinhado)** | Parte do plano é inclinada e "girada" até ficar alinhada com o resto | Peças circulares com furos ou braços em ângulo (flanges, polias, cubos) |

### Tipos de seção

| Tipo | Como é |
|---|---|
| **Seção rebatida dentro da vista** | A fatia é girada 90° e desenhada sobre a própria vista, com contorno em linha contínua estreita |
| **Seção fora da vista** | A fatia é desenhada ao lado, ligada ao plano por linha traço e ponto, ou identificada por letras; contorno em linha contínua larga |
| **Seções sucessivas** | Várias seções ao longo da peça, para mostrar como o perfil varia (por exemplo, num braço de polia) |

### Elementos que não são cortados longitudinalmente

Em cortes **longitudinais** (pelo eixo), alguns elementos são desenhados **sem hachura**, como se não tivessem sido cortados, porque cortá-los não acrescenta informação e confunde a leitura:

- eixos, pinos, cavilhas, chavetas, rebites;
- parafusos, porcas e arruelas;
- esferas e roletes de rolamentos;
- **nervuras** e braços (cortados no sentido do comprimento);
- dentes de engrenagem.

Em cortes **transversais** (perpendiculares ao eixo), eles são hachurados normalmente.

## Por que importa no projeto

- **Elimina tracejadas confusas.** Uma carcaça com furos, canais de óleo e alojamentos fica ilegível só com linhas ocultas.
- **Permite cotar o interior** sobre arestas visíveis. A regra é **não cotar arestas ocultas**; o corte transforma o oculto em visível.
- **Mostra espessuras de parede**, informação essencial para peças fundidas e soldadas.
- **Em conjuntos**, o corte mostra como as peças se encaixam: o rolamento no alojamento, o retentor na tampa, a bucha no mancal.

## Como aplicar (passo a passo / regras práticas)

1. **Pergunte: há muita tracejada nesta vista?** Se sim, substitua a vista por um corte.
2. **Escolha o tipo:** peça simétrica → meio corte; detalhe isolado → corte parcial; elementos desalinhados → corte em desvio; elementos em ângulo numa peça circular → corte rebatido.
3. **Indique o plano** na vista adjacente, com letras e setas.
4. **Posicione o corte** onde estaria a vista correspondente, respeitando o diedro. Se não houver espaço, posicione em outro lugar com o título "CORTE A–A".
5. **Hachure só o que foi cortado**, com o mesmo padrão em todos os cortes da mesma peça. Ver [[Hachuras]].
6. **Não hachure** eixos, parafusos, nervuras etc. em cortes longitudinais.
7. **Não desenhe tracejadas** na parte em corte (o interior já está visível), salvo se forem indispensáveis.

## Norma relacionada

- **ABNT NBR 10067:1995**: princípios de representação, incluindo cortes e seções. ⚠️ verificar edição vigente.
- **ABNT NBR 12298:1995**: representação de área de corte por meio de hachuras. ⚠️ verificar se continua vigente.
- **ISO 128-40 / ISO 128-44**: convenções para cortes e seções (geral e em desenho mecânico). ⚠️ verificar as partes vigentes da ISO 128.

## Exemplo prático

**Situação:** representar a **tampa de mancal** de um redutor: peça circular, simétrica, com um furo central onde aloja um retentor, um rebaixo para centralização e seis furos de fixação no flange.

- **Vista frontal:** a face da tampa, mostrando o círculo de furação com os seis furos.
- **Vista lateral em meio corte:** metade mostra o exterior da tampa; a outra metade mostra, cortados, o alojamento do retentor, o rebaixo de centralização e a espessura do flange.
- O **retentor**, se o desenho for de conjunto, aparece cortado com hachura própria (outra direção).
- Os **parafusos de fixação**, se aparecerem no plano do corte, ficam **sem hachura**.

> [!question] Exercício 1
>
> Um eixo com rasgo de chaveta é desenhado em vista longitudinal. Você precisa mostrar a profundidade do rasgo. Que recurso usa?
>
> > [!success]- Resolução
> >
> > Uma **seção transversal** no meio do rasgo, rebatida dentro da vista ou desenhada fora dela. A seção mostra o círculo do eixo com o "entalhe" do rasgo, onde se cota a profundidade. Cortar o eixo longitudinalmente não serviria: pela regra, eixos não são hachurados em corte longitudinal, e a profundidade não ficaria clara.

> [!question] Exercício 2
>
> Num corte longitudinal de um conjunto (mancal com eixo, rolamento, bucha espaçadora, porca de fixação e nervuras no corpo do mancal), quais elementos ficam sem hachura?
>
> > [!success]- Resolução
> >
> > Ficam **sem hachura**: o **eixo**, as **esferas ou roletes** do rolamento, a **porca** e as **nervuras** (cortadas no sentido do comprimento). Ficam **com hachura**: o corpo do mancal, os anéis do rolamento e a bucha espaçadora, cada peça com direção ou espaçamento de hachura diferente da vizinha.

## Erros comuns

- **Hachurar o eixo** em corte longitudinal.
- **Plano de corte sem letras ou setas**, ou com a direção de observação invertida.
- **Meio corte com tracejadas** na metade em vista.
- **Hachuras diferentes para a mesma peça** em cortes distintos.
- **Esquecer as arestas visíveis atrás do plano de corte**: no corte, tudo o que se vê além do plano também é desenhado.

## Ver também

- [[Hachuras]]
- [[Tipos de linha]]
- [[Escolha de vistas]]
- [[Desenho de conjunto e de detalhe]]
- [[01-desenho-tecnico/index|Índice do módulo 01]]
