---
title: Tolerâncias de orientação
tags: [gdt, orientacao]
fontes: [ISO 1101:2017, ISO 5459:2011, Henzold Geometrical Dimensioning and Tolerancing for Design, Manufacturing and Inspection, Krulikowski Fundamentals of Geometric Dimensioning and Tolerancing]
status: rascunho
---

**Resumo:** tolerâncias de orientação controlam o ângulo de um elemento em relação a uma referência: paralelismo (0°), perpendicularidade (90°) e inclinação (qualquer outro ângulo). Elas não controlam a posição, só a "direção", e incluem automaticamente o controle de forma do elemento.

## O que é

| Símbolo | Característica | Ângulo em relação à referência |
|---|---|---|
| ∥ | **Paralelismo** | 0° |
| ⊥ | **Perpendicularidade** | 90° |
| ∠ | **Inclinação** | Qualquer ângulo, dado por cota teoricamente exata em caixa |

### Zonas de tolerância

Dependem do elemento controlado e do uso de Ø:

| Elemento controlado | Zona |
|---|---|
| Superfície plana | Entre dois planos paralelos afastados de t, orientados em relação à referência |
| Eixo (com Ø no valor) | Dentro de um cilindro Ø t, orientado em relação à referência |
| Eixo (sem Ø) | Entre dois planos paralelos (controla a orientação só numa direção) |

### Relação com outras tolerâncias

- A orientação **contém a forma**: se uma face tem paralelismo de 0,05 com A, sua planeza também é no máximo 0,05.
- A orientação **não contém a posição**: uma face pode ser perfeitamente paralela a A e estar fora da distância nominal; a distância é controlada pela tolerância dimensional ou de posição.

## Por que importa no projeto

- **Perpendicularidade entre face e furo:** furos de mancais e alojamentos precisam ser perpendiculares à face de apoio, senão o eixo fica inclinado e os rolamentos trabalham desalinhados.
- **Paralelismo entre faces de encosto:** espaçadores, calços e anéis que suportam carga axial.
- **Paralelismo entre eixos:** em redutores e transmissões por engrenagens, o paralelismo entre os furos dos rolamentos dos dois eixos define o contato dos dentes.
- **Inclinação:** faces de apoio inclinadas, assentos cônicos, guias em ângulo.

## Como aplicar (passo a passo / regras práticas)

1. **Escolha a referência** que representa a montagem (normalmente a face de apoio).
2. **Defina o elemento controlado:** superfície (seta na face) ou eixo (seta alinhada à cota de diâmetro).
3. **Use Ø** quando o eixo puder inclinar em qualquer direção e isso importar igualmente.
4. **Para inclinação**, cote o ângulo nominal **em caixa** (cota teoricamente exata).
5. **Valor:** menor que a tolerância de posição ou de tamanho correspondente; maior que a tolerância de forma, se houver.

## Norma relacionada

- **ISO 1101:2017**: definição das zonas de orientação.
- **ISO 5459:2011**: referências.

## Exemplo prático

**Situação:** a carcaça de um **redutor de engrenagens cilíndricas** tem dois pares de furos de rolamento (eixo de entrada e eixo de saída). O contato entre os dentes exige que os eixos sejam paralelos.

- **Referência A:** eixo comum dos dois furos do eixo de entrada.
- **Paralelismo** do eixo comum dos furos do eixo de saída em relação a A:

<span class="fcf"><span>∥</span><span>Ø0,04</span><span>A</span></span>

Num comprimento entre mancais de 400 mm, um erro de paralelismo de 0,04 mm representa uma inclinação de $0{,}04/400 = 0{,}0001$ rad. Em engrenagens com 100 mm de largura de face, isso gera um desvio de alinhamento dos dentes de $100 \times 0{,}0001 = 0{,}01$ mm ao longo da face. ⚠️ verificar os limites de desalinhamento admitidos na ISO 1328 e no projeto da engrenagem.

> [!question] Exercício
>
> Um furo de Ø30 numa placa de 50 mm de espessura tem perpendicularidade Ø0,02 em relação à face A. Qual o maior ângulo de inclinação possível do eixo do furo?
>
> > [!success]- Resolução
> >
> > O eixo deve ficar dentro de um cilindro de Ø0,02 perpendicular a A, ao longo dos 50 mm do furo. A maior inclinação ocorre com o eixo indo de um lado do cilindro numa face ao lado oposto na outra:
> > $$\tan\theta = \frac{0{,}02}{50} = 0{,}0004 \Rightarrow \theta \approx 0{,}023°$$
> > (cerca de 1,4 minutos de arco).

## Erros comuns

- **Esperar que paralelismo controle a distância** entre as faces.
- **Inclinação sem o ângulo em caixa** (com tolerância angular ±, há duas tolerâncias para a mesma coisa).
- **Perpendicularidade de furo sem Ø**, quando a função exige controle em todas as direções.
- **Referência escolhida longe da função**, por exemplo uma face bruta.

## Ver também

- [[Tolerâncias de forma]]
- [[Tolerâncias de localização]]
- [[Referências geométricas]]
- [[03-gdt/index|Índice do módulo 03]]
