---
title: Sistema eixo-base
tags: [tolerancias, ajustes]
fontes: [ISO 286-1:2010, ABNT NBR 6158:1995, Budynas e Nisbett Elementos de Máquinas de Shigley (cap. de tolerâncias e ajustes)]
status: rascunho
---

**Resumo:** no sistema eixo-base, o eixo tem sempre a posição h (desvio superior zero) e os ajustes são obtidos variando a letra do furo. É menos comum que o furo-base, mas é a escolha natural quando o eixo é um material comprado já calibrado, ou quando várias peças com ajustes diferentes montam num mesmo eixo liso.

## O que é

No **eixo-base**, o eixo é sempre **h** ($es = 0$): nunca maior que o nominal. O ajuste é definido pela letra do **furo**:

$$
\underbrace{\text{A ... G}}_{\text{folga}} \;\; \underbrace{\text{H}}_{\text{folga mín. zero}} \;\; \underbrace{\text{JS, J, K, M, N}}_{\text{incerto}} \;\; \underbrace{\text{P, R, S...}}_{\text{interferência}}
$$

É o espelho do [[Sistema furo-base]]. Para os ajustes preferenciais, os resultados são praticamente equivalentes: H7/g6 e G7/h6 dão folgas muito parecidas.

## Por que importa no projeto

Há situações em que o eixo-base é mais vantajoso:

- **Barras calibradas (trefiladas ou retificadas)** compradas prontas, normalmente na classe **h** (h9, h11, ou h6/h7 em barras retificadas). Usar a barra sem usinar o diâmetro economiza muito.
- **Eixo liso com várias peças de ajustes diferentes**, por exemplo um eixo de transmissão longo com mancais (folga), polias (incerto) e colares (interferência). Com furo-base, o eixo teria de ser escalonado para cada ajuste; com eixo-base, o eixo é um cilindro único e cada furo é feito no ajuste necessário.
- **Componentes padronizados com eixo fixo:** pinos, cavilhas e rolamentos (o anel externo do rolamento é tratado como um "eixo" de tolerância própria, e o ajuste é escolhido pela classe do **alojamento**).
- **Larguras de chavetas:** a chaveta paralela é fabricada em **h9** de largura, e o ajuste com o rasgo é escolhido pela classe do rasgo (N9, P9, JS9, D10). Ver [[05-elementos-de-maquinas/index|Elementos de máquinas]].

## Como aplicar (passo a passo / regras práticas)

1. **Use eixo-base quando o eixo for comprado calibrado** ou for uma peça padronizada (pino, chaveta, anel externo de rolamento).
2. **Fixe o eixo em h** (h6, h7, h9 conforme a precisão).
3. **Escolha a letra do furo** pelo ajuste desejado.
4. **Leia os desvios do furo na ISO 286-2** (para K a ZC, os valores têm correções e não devem ser calculados pela regra simples).
5. **Confira folga e interferência** máximas e mínimas.

## Norma relacionada

- **ISO 286-1:2010**: define o sistema eixo-base e os ajustes preferenciais.
- **ISO 286-2:2010**: tabelas dos desvios de furos.
- **ABNT NBR 6158:1995**: equivalente brasileira. ⚠️ verificar edição vigente.

## Exemplo prático

**Situação:** pino de articulação de Ø20 feito de barra retificada **h7** (19,979 a 20,000 mm), montado em três peças:

| Peça | Função | Furo | Ajuste |
|---|---|---|---|
| Garfo fixo | Prender o pino sem girar | P7 | Interferência |
| Olhal da biela | Girar livre sobre o pino | F8 | Folga |
| Arruela de encosto | Posicionar | H8 | Folga pequena |

O pino não é usinado no diâmetro: corta-se a barra no comprimento, faz-se chanfro e, se necessário, o furo da cupilha. ⚠️ verificar os desvios de P7 e F8 na ISO 286-2 para Ø20.

> [!question] Exercício
>
> Por que a largura de uma chaveta paralela é fabricada em h9, e o ajuste é escolhido pela tolerância do rasgo?
>
> > [!success]- Resolução
> >
> > Porque a chaveta é uma **peça padronizada, comprada pronta** (barra de chaveta trefilada em h9). Como o "eixo" (a chaveta) é fixo, o ajuste é definido variando o "furo" (o rasgo): N9 no eixo para ajuste firme, JS9 no cubo para ajuste normal, D10 para ajuste deslizante, P9 para ajuste forçado. É o sistema eixo-base aplicado a uma largura.

## Erros comuns

- **Usinar uma barra já calibrada** só para colocá-la no furo-base.
- **Calcular desvios de furos K, M, N, P** pela regra simples, sem a correção da tabela.
- **Esquecer que o anel externo do rolamento** já tem tolerância própria (negativa) e escolher o alojamento como se fosse um eixo h.

## Ver também

- [[Sistema furo-base]]
- [[Tipos de ajuste]]
- [[Posições de tolerância]]
- [[02-tolerancias-ajustes/index|Índice do módulo 02]]
