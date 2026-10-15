---
title: Acoplamentos rígidos e elásticos
tags: [elementos, transmissao]
fontes: [AGMA 9002 (furos e rasgos de acoplamentos) ⚠️ verificar, API 671 (acoplamentos para serviço especial) ⚠️ verificar, catálogos técnicos de acoplamentos (seções de seleção e alinhamento), Niemann Elementos de Máquinas (cap. de acoplamentos), Piotrowski Shaft Alignment Handbook]
status: rascunho
---

**Resumo:** acoplamentos ligam dois eixos e transmitem torque entre eles, por exemplo do motor ao redutor e do redutor à máquina. Os rígidos exigem alinhamento perfeito; os flexíveis (elásticos e de engrenagens, de grade, de discos) acomodam desalinhamentos e, em parte, amortecem choques. A seleção usa o torque com fator de serviço, a rotação, os diâmetros dos eixos e o desalinhamento a acomodar.

## O que é

### Tipos de desalinhamento

- **Paralelo (radial):** eixos paralelos, mas deslocados.
- **Angular:** eixos se cruzam formando um ângulo.
- **Axial:** variação da distância entre as pontas (dilatação, folgas).

Na prática, existe sempre uma combinação dos três.

### Tipos de acoplamento

| Tipo | Desalinhamento admissível | Amortecimento | Uso típico |
|---|---|---|---|
| **Rígido** (flanges, luva bipartida) | Praticamente nenhum | Não | Eixos longos de transmissão apoiados em mancais próprios; alinhamento muito preciso |
| **Elástico de garras (*jaw*)** com elemento de elastômero | Pequeno | Sim | Motores e bombas de pequeno e médio porte |
| **Elástico de pinos e buchas** | Pequeno a médio | Sim | Acionamentos industriais gerais |
| **De pneu (elastômero)** | Grande | Sim, alto | Acionamentos com choques e desalinhamento difícil de controlar |
| **De grade (molas em grade)** | Médio | Algum | Acionamentos médios e pesados |
| **De engrenagens (dentes abaulados)** | Médio (angular por dente) | Não | **Torques muito altos** em dimensões compactas; acionamentos pesados; exige lubrificação |
| **De discos/lamelas** | Médio angular e axial | Não | Bombas e compressores de alta rotação; sem lubrificação |
| **Cardan (cruzetas)** | Ângulos grandes | Não | Distâncias e ângulos grandes; laminadores |
| **Hidráulico** | Pequeno | Partida suave | Partidas pesadas (transportadores longos, moinhos) |

### Seleção

$$
T_{\text{seleção}} = T_{\text{nominal}} \times f_s \le T_{\text{catálogo}}
$$

Também se verifica:

- **Torque de pico** (partida, travamento) contra o torque máximo do acoplamento.
- **Rotação máxima.**
- **Furo máximo** de cada cubo (os eixos têm de caber).
- **Desalinhamentos** esperados contra os admissíveis.

### Alinhamento

Mesmo acoplamentos flexíveis duram muito mais com bom alinhamento. Os admissíveis do catálogo são limites de operação, **não metas de montagem**. O alinhamento é feito com relógios comparadores (método do relógio reverso, face e borda) ou com alinhador a laser, considerando o **crescimento térmico** das máquinas em operação.

## Por que importa no projeto

- **Desalinhamento é uma das principais causas** de falha de rolamentos, retentores e acoplamentos.
- **Acoplamentos de engrenagens** mal lubrificados desgastam rapidamente os dentes.
- **Acoplamentos elásticos funcionam como fusível**: o elemento elástico é a peça barata que falha.
- **O espaço entre pontas de eixo** (DBSE) deve permitir a troca do elemento elástico sem mover os equipamentos.

## Como aplicar (passo a passo / regras práticas)

1. **Torque nominal** pelo motor ou pela máquina: $T = 9550\,P/n$.
2. **Fator de serviço** pelo tipo de máquina e motor (catálogo).
3. **Escolha o tipo** pelo torque, rotação, desalinhamento e necessidade de amortecimento.
4. **Escolha o tamanho** pelo torque de seleção e confira furos máximos e rotação.
5. **Defina furos, rasgos e ajustes** dos cubos (normalmente k6/H7 com chaveta, ou interferência em torques altos). Ver [[Chavetas]] e [[Ajustes recomendados]].
6. **Especifique o alinhamento** de montagem (tolerâncias de paralelo e angular) e a distância entre pontas.

## Norma relacionada

- **Catálogos de fabricantes**: fatores de serviço, capacidades, furos máximos e desalinhamentos.
- **AGMA 9002**: furos e rasgos de acoplamentos. ⚠️ verificar.
- **API 671**: acoplamentos para serviço especial (petróleo e gás). ⚠️ verificar.

## Exemplo prático

**Situação:** ligar o eixo de saída de um redutor (**25 kN·m nominais**, 25 rpm) ao eixo de um tambor de transportador, com choques moderados e uma base sujeita a pequenas deformações.

- Fator de serviço: 1,5 → torque de seleção **37,5 kN·m**.
- Tipo: **acoplamento de engrenagens** (alto torque em dimensões compactas, acomoda desalinhamento angular e paralelo moderados) ou **de grade** para amortecer choques.
- Verificar: furos máximos ≥ diâmetros dos eixos (por exemplo, Ø160 e Ø180), desalinhamento admissível e lubrificação (graxa específica para acoplamentos).
- Alinhamento de montagem bem abaixo do admissível do catálogo, conferido após o aperto dos chumbadores.

> [!question] Exercício
>
> Um motor de 30 kW a 1770 rpm aciona uma bomba centrífuga (carga uniforme, fator de serviço 1,0) e, em outro caso, um britador (fator 2,0). Qual o torque de seleção do acoplamento em cada caso?
>
> > [!success]- Resolução
> >
> > $T = 9550 \times 30/1770 \approx 162$ N·m.
> > - Bomba: $162 \times 1{,}0 = 162$ N·m.
> > - Britador: $162 \times 2{,}0 = 324$ N·m.
> >
> > O mesmo motor exige um acoplamento com o dobro da capacidade quando aciona uma máquina com choques pesados.

## Erros comuns

- **Selecionar só pelo diâmetro do eixo**, sem verificar o torque.
- **Usar o desalinhamento admissível como tolerância de montagem.**
- **Ignorar o crescimento térmico** (motor e bomba quentes mudam de altura).
- **Acoplamento rígido entre máquinas com mancais próprios**, que força os rolamentos.
- **Esquecer a lubrificação** de acoplamentos de engrenagens.

## Ver também

- [[Redutores]]
- [[Chavetas]]
- [[Batimento]]
- [[05-elementos-de-maquinas/index|Índice do módulo 05]]
