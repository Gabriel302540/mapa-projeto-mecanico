---
title: Por que usar tolerâncias geométricas
tags: [gdt, fundamentos]
fontes: [ISO 1101:2017, ISO 8015:2011, ASME Y14.5-2018, Henzold Geometrical Dimensioning and Tolerancing for Design, Manufacturing and Inspection (cap. 1), Krulikowski Fundamentals of Geometric Dimensioning and Tolerancing (cap. 1)]
status: rascunho
---

**Resumo:** tolerâncias dimensionais (±, H7, g6) controlam tamanhos, mas não controlam forma, orientação e posição. Uma peça pode ter todos os diâmetros dentro da tolerância e mesmo assim estar torta, ovalizada ou com furos fora de lugar. As tolerâncias geométricas (GD&T, ou GPS no vocabulário ISO) definem zonas exatas onde cada superfície ou eixo deve ficar, a partir de referências claras.

## O que é

**GD&T** (*Geometric Dimensioning and Tolerancing*) é a linguagem de símbolos para especificar a **geometria** da peça: forma, orientação, localização e batimento. No sistema ISO, faz parte do conjunto **GPS** (*Geometrical Product Specifications*), com a ISO 1101 como norma central.

### O que as cotas com ± não resolvem

1. **Forma:** "Ø50 ± 0,02" garante que cada medição de dois pontos fique entre 49,98 e 50,02, mas não impede que o eixo seja levemente cônico, ovalizado ou curvado.
2. **Referência:** "furo a 100 ± 0,1 da borda" não diz **qual** borda usar se ela não for perfeitamente reta, nem como apoiar a peça para medir.
3. **Zona quadrada:** cotar a posição de um furo com ± em X e Y cria uma zona de tolerância **quadrada**. Um furo deslocado na diagonal pode estar a 0,14 mm do centro e ser aprovado, enquanto outro a 0,11 mm na horizontal é reprovado, sem nenhuma lógica funcional.
4. **Acúmulo:** cadeias de cotas com ± acumulam erros (ver [[Empilhamento de tolerâncias]]).

### As quatro famílias de tolerâncias geométricas

| Família | Características | Precisa de referência? |
|---|---|---|
| **Forma** | Retitude, planeza, circularidade, cilindricidade | Não |
| **Orientação** | Paralelismo, perpendicularidade, inclinação | Sim |
| **Localização** | Posição, coaxialidade/concentricidade, simetria | Sim (posição pode ser sem, em padrões de furos) |
| **Batimento** | Batimento circular, batimento total | Sim |
| **Perfil** (linha e superfície) | Pode atuar como forma, orientação ou localização | Depende do uso |

Ver [[Tolerâncias de forma]], [[Tolerâncias de orientação]], [[Tolerâncias de localização]], [[Batimento]] e [[Tolerância de perfil]].

### Zona de tolerância

Cada tolerância geométrica define uma **zona** no espaço onde o elemento deve estar contido: entre dois planos paralelos, dentro de um cilindro, entre dois cilindros coaxiais, entre dois círculos concêntricos etc. A peça está aprovada se o elemento real cabe inteiro dentro da zona.

## Por que importa no projeto

- **Função:** o que faz um rolamento durar não é só o diâmetro do assento, mas a **circularidade**, a **cilindricidade** e o **batimento** desse assento em relação ao eixo de rotação.
- **Montabilidade:** a **tolerância de posição** de um padrão de furos é o que garante que os parafusos entrem.
- **Custo:** zonas cilíndricas para furos dão cerca de **57 % mais área** que zonas quadradas equivalentes, aprovando peças funcionais que seriam refugadas com ±.
- **Inspeção sem ambiguidade:** as referências definem como apoiar a peça para medir, de modo que projetista, fabricante e inspetor medem a mesma coisa.

## Como aplicar (passo a passo / regras práticas)

1. **Identifique as superfícies funcionais:** onde a peça apoia, centraliza, gira, veda ou recebe outras peças.
2. **Defina as referências** (datums) a partir de como a peça é montada. Ver [[Referências geométricas]].
3. **Controle a forma** das referências quando a função exigir (planeza de uma face de apoio, cilindricidade de um assento).
4. **Controle orientação, posição ou batimento** dos demais elementos em relação às referências.
5. **Use cotas teoricamente exatas** (em caixa) para localizar elementos controlados por posição ou perfil.
6. **Deixe o restante na tolerância geral**. Ver [[Tolerâncias gerais]].

## Norma relacionada

- **ISO 1101:2017**: tolerâncias geométricas — tolerâncias de forma, orientação, localização e batimento. Revisada e confirmada em 2022, portanto vigente.
- **ISO 8015:2011**: conceitos fundamentais, princípios e regras do sistema GPS (inclui o princípio da independência).
- **ISO 5459**: referências e sistemas de referência.
- **ASME Y14.5-2018**: equivalente americano, com diferenças importantes (por exemplo, a "Regra nº 1" da envoltória vale por padrão). Ver [[Independência e envoltória]].

## Exemplo prático

**Situação:** um eixo de transmissão com dois assentos de rolamento (Ø60 k6) e um assento de acoplamento (Ø55 k6). O eixo foi fabricado com todos os diâmetros aprovados, mas na montagem o acoplamento apresentou batimento de 0,25 mm e os rolamentos aqueceram.

**Diagnóstico:** os diâmetros estavam corretos, mas o assento do acoplamento estava **excêntrico** em relação ao eixo definido pelos dois assentos de rolamento (o torneiro virou a peça entre as fixações sem cuidar do alinhamento). Nada no desenho proibia isso.

**Correção no desenho:**

- Referências **A** e **B** nos dois assentos de rolamento; referência comum **A–B** (o eixo real de rotação).
- **Batimento circular** de 0,02 mm no assento do acoplamento em relação a A–B.
- **Cilindricidade** de 0,005 mm nos assentos de rolamento. ⚠️ verificar valores recomendados pelo fabricante do rolamento.

## Erros comuns

- **Achar que a tolerância dimensional controla a forma** (ver [[Independência e envoltória]]).
- **Colocar tolerâncias geométricas em tudo**, encarecendo a peça sem necessidade.
- **Referências que não correspondem à montagem**, fazendo o inspetor medir de um jeito diferente do funcionamento real.
- **Misturar regras ISO e ASME** no mesmo desenho sem declarar qual norma vale.

## Ver também

- [[Quadro de tolerância]]
- [[Referências geométricas]]
- [[Independência e envoltória]]
- [[03-gdt/index|Índice do módulo 03]]
