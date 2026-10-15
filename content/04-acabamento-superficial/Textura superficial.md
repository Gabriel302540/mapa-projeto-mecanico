---
title: "Textura superficial: rugosidade, ondulação e forma"
tags: [acabamento, fundamentos]
fontes: [ISO 21920-2:2021, ISO 4287:1997 (histórica), Whitehouse Surfaces and their Measurement (cap. 1), Agostinho, Rodrigues e Lirani Tolerâncias, Ajustes, Desvios e Análise de Dimensões (cap. de estado de superfície)]
status: rascunho
---

**Resumo:** toda superfície real tem irregularidades em várias escalas. As maiores e mais espaçadas formam o erro de forma; as intermediárias, a ondulação; as menores e mais próximas, a rugosidade. Elas têm causas e efeitos diferentes e são separadas na medição por filtros de comprimento de onda.

## O que é

Olhe para o perfil de uma superfície usinada, cortado perpendicularmente a ela e muito ampliado na vertical. Ele é uma soma de três componentes:

| Componente | Escala (espaçamento) | Causa típica | Controlada por |
|---|---|---|---|
| **Forma** | Comprimento da peça inteira | Deflexão da peça e da máquina, desalinhamento, tensões residuais, aquecimento | Tolerâncias geométricas (planeza, cilindricidade...). Ver [[Tolerâncias de forma]] |
| **Ondulação** | Milímetros a centímetros | Vibração da máquina, desbalanceamento do rebolo, avanço irregular, folgas | Parâmetros W (Wa, Wt...), menos usados |
| **Rugosidade** | Micrômetros a décimos de milímetro | Marca da ferramenta (avanço e raio de ponta), arrancamento de material, grãos do rebolo | Parâmetros R (Ra, Rz...). Ver [[Parâmetros de rugosidade]] |

### Perfis e filtros

Na medição, um apalpador (agulha) percorre a superfície e registra o **perfil total**. Filtros matemáticos separam as componentes pelo comprimento de onda:

- **Filtro λs:** remove ruídos muito curtos (menores que a resolução útil).
- **Filtro λc (*cut-off*):** separa **rugosidade** (ondas menores que λc) de **ondulação** (maiores).
- **Filtro λf:** separa ondulação de forma.

O valor de λc mais comum é **0,8 mm**. Ver [[Medição de rugosidade]].

### Orientação das marcas (*lay*)

A direção predominante das marcas deixadas pelo processo também faz parte da textura: paralelas (torneamento visto de lado, retificação), cruzadas (brunimento), circulares (faceamento), radiais, multidirecionais (lapidação, jateamento). Ela pode ser especificada no desenho. Ver [[Símbolos de acabamento]].

## Por que importa no projeto

- **Desgaste e atrito:** superfícies rugosas desgastam mais rápido as peças que deslizam sobre elas (por exemplo, o lábio de um retentor sobre o eixo).
- **Fadiga:** os vales da rugosidade são pequenos entalhes que concentram tensão. Eixos submetidos a flexão rotativa têm limite de fadiga menor quando a superfície é rugosa (fator de superfície $k_a$ no critério de fadiga; ver [[05-elementos-de-maquinas/index|Eixos — fadiga]]).
- **Vedação:** juntas, o-rings e selos dependem de superfícies com rugosidade adequada.
- **Ajustes com interferência:** as pontas da rugosidade são "amassadas" na montagem, reduzindo a interferência efetiva.
- **Lubrificação:** em mancais de deslizamento, a rugosidade precisa ser bem menor que a espessura do filme de óleo.
- **Custo:** cada classe de rugosidade mais fina pode exigir uma operação a mais (retificação, brunimento).

## Como aplicar (passo a passo / regras práticas)

1. **Identifique as superfícies funcionais** (que deslizam, vedam, montam, suportam fadiga).
2. **Especifique rugosidade só nelas**; as demais ficam com uma indicação geral (por exemplo, Ra 6,3).
3. **Controle a forma com tolerância geométrica**, e não pela rugosidade.
4. **Escolha o processo** compatível com a rugosidade exigida. Ver [[Rugosidade por processo]].

## Norma relacionada

- **ISO 21920-2:2021**: termos, definições e parâmetros de textura de perfil. Substitui a ISO 4287, a ISO 13565-2 e a ISO 13565-3.
- **ISO 21920-3:2021**: operadores de especificação (filtros, comprimentos). Substitui a ISO 4288 e parte da ISO 3274 ⚠️ verificar.
- **ISO 4287:1997**: norma anterior de parâmetros, ainda muito citada em desenhos e instrumentos.

## Exemplo prático

**Situação:** um eixo de bomba apresentou desgaste rápido do retentor (vazamentos em poucas semanas) e, mais tarde, trinca por fadiga num rebaixo.

- **Retentor:** a pista estava torneada com Ra 3,2 µm e marcas helicoidais do avanço do torno, que "bombeiam" o fluido para fora. Correção: Ra 0,2–0,8 µm, **retificação de mergulho** (sem marcas helicoidais) e dureza mínima conforme o catálogo do retentor. ⚠️ verificar.
- **Fadiga:** o rebaixo estava com marcas profundas de ferramenta (Ra 6,3). Correção: acabamento fino no raio de concordância (Ra ≤ 1,6) e raio maior.

## Erros comuns

- **Exigir rugosidade fina em todas as superfícies**, encarecendo a peça.
- **Tentar controlar ovalização ou conicidade pela rugosidade** (são erros de forma).
- **Esquecer a direção das marcas** em pistas de vedação.
- **Ignorar o efeito da rugosidade na fadiga** de eixos.

## Ver também

- [[Parâmetros de rugosidade]]
- [[Símbolos de acabamento]]
- [[Rugosidade pela função]]
- [[04-acabamento-superficial/index|Índice do módulo 04]]
