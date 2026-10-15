---
title: "Rolamentos: tipos e seleção"
tags: [elementos, rolamentos]
fontes: [ISO 15 (dimensões gerais de rolamentos radiais), ISO 281:2007, catálogos técnicos gerais de rolamentos (seções de seleção de tipo e arranjo), Budynas e Nisbett Elementos de Máquinas de Shigley (cap. 11), Harris e Kotzalas Rolling Bearing Analysis]
status: rascunho
---

**Resumo:** rolamentos substituem o deslizamento por rolamento de esferas ou rolos, com atrito baixo e vida previsível. Cada tipo tem pontos fortes: carga radial, carga axial, desalinhamento, rotação alta, rigidez. Escolher o tipo certo vem antes de calcular a vida.

## O que é

### Principais tipos

| Tipo | Carga radial | Carga axial | Desalinhamento | Rotação | Uso típico |
|---|---|---|---|---|---|
| **Rígido de esferas** | Média | Média, dois sentidos | Baixo | Muito alta | Motores elétricos, máquinas em geral |
| **De contato angular de esferas** | Média | Alta, um sentido (pares para dois) | Baixo | Alta | Bombas, fusos, eixos com carga combinada |
| **Autocompensador de esferas** | Baixa a média | Baixa | **Alto** | Alta | Eixos longos com flexão, transmissões leves |
| **De rolos cilíndricos** | **Alta** | Nenhuma ou baixa (conforme o modelo) | Muito baixo | Alta | Redutores, motores grandes, lado livre de eixos |
| **De rolos cônicos** | Alta | **Alta**, um sentido (montados em pares) | Baixo | Média | Rodas, redutores, eixos com carga axial alta |
| **Autocompensador de rolos** | **Muito alta** | Média, dois sentidos | **Alto** | Média | Equipamentos pesados, transportadores, britadores, peneiras, mancais de rolos e eixos grandes |
| **Axial de esferas** | Nenhuma | Média | Baixo | Média | Cargas axiais puras |
| **Axial autocompensador de rolos** | Baixa | **Muito alta** | Alto | Média | Prensas, roscas sem-fim pesadas |
| **De agulhas** | Alta (para o tamanho) | Nenhuma | Baixo | Média | Espaço radial reduzido |

### Designação

A designação básica (por exemplo **6208**, **22220**, **32210**) indica o **tipo** (primeiro dígito ou grupo), a **série de dimensões** (largura e diâmetro externo) e o **furo** (os dois últimos dígitos × 5 mm, para furos de 20 a 480 mm: "08" → 40 mm; "20" → 100 mm). Sufixos indicam vedação (2RS, 2Z), folga interna (C3), gaiola, furo cônico (K) etc. ⚠️ verificar os sufixos no catálogo do fabricante, que variam entre marcas.

### Folga interna

Folga entre as esferas ou rolos e as pistas. Classes: C2 (menor), CN (normal), **C3** (maior), C4, C5. Usa-se C3 quando o ajuste com interferência ou a diferença de temperatura entre anéis "come" a folga em operação (motores elétricos, mancais aquecidos).

### Arranjos de rolamentos num eixo

- **Fixo-livre:** um rolamento fixa o eixo axialmente nos dois sentidos; o outro deixa o eixo se dilatar. O mais usado em eixos longos.
- **Ajustado (cruzado):** cada rolamento fixa um sentido (rolos cônicos, contato angular). Eixos curtos.
- **Flutuante:** os dois permitem pequeno deslocamento axial; o eixo é guiado por outro elemento.

Ver [[Montagem de rolamentos]].

## Por que importa no projeto

- **Desalinhamento é comum** em equipamentos pesados (estruturas soldadas, eixos longos, bases que se deformam): autocompensadores toleram isso; rolos cilíndricos não.
- **Carga axial** de engrenagens helicoidais e cônicas exige rolamentos que a suportem.
- **Padronização:** usar poucos tipos e tamanhos reduz estoque de sobressalentes.
- **Ambiente:** sujeira e água exigem vedações, caixas com labirinto e relubrificação.

## Como aplicar (passo a passo / regras práticas)

1. **Levante as cargas** (radial, axial), a rotação, o espaço e o desalinhamento esperado.
2. **Escolha o tipo** pela tabela.
3. **Defina o arranjo** (fixo-livre ou ajustado).
4. **Calcule a vida** com as cargas equivalentes. Ver [[Vida de rolamentos]].
5. **Defina ajustes**, folga interna e fixação. Ver [[Ajustes recomendados]] e [[Montagem de rolamentos]].
6. **Defina lubrificação e vedação** (graxa ou óleo; vedações integradas, labirintos).

## Norma relacionada

- **ISO 15**: dimensões gerais de rolamentos radiais.
- **ISO 281:2007**: capacidade de carga dinâmica e vida nominal.
- **ISO 76**: capacidade de carga estática.
- **ISO 492**: tolerâncias de rolamentos radiais.

## Exemplo prático

**Situação:** escolher os rolamentos do eixo de um **rolo de transportador de correia pesado**: eixo longo, carga radial alta, rotação baixa, estrutura soldada sujeita a deformações, ambiente sujo.

- **Tipo:** autocompensador de rolos — suporta carga alta e desalinhamento da estrutura.
- **Arranjo:** fixo-livre — um mancal fixo (lado acionamento) e um livre (dilatação do eixo).
- **Montagem:** com **bucha de fixação** em eixo liso h9/h10, facilitando a troca no campo.
- **Caixa:** bipartida, com vedação labirinto e graxeira para relubrificação.

> [!question] Exercício
>
> Decodifique as designações 6208-2RS C3 e 22220 EK. (Use a regra do furo; os sufixos são os mais comuns.)
>
> > [!success]- Resolução
> >
> > - **6208-2RS C3:** rolamento **rígido de esferas** (6), série 2, furo **40 mm** (08 × 5), **vedado dos dois lados** com retentores de borracha (2RS), **folga C3** (maior que a normal).
> > - **22220 EK:** **autocompensador de rolos** (222), furo **100 mm** (20 × 5), projeto interno reforçado (E, conforme o fabricante) e **furo cônico** (K), para montagem em bucha de fixação ou eixo cônico.

## Erros comuns

- **Rolos cilíndricos com desalinhamento**, que gera carga nas bordas e falha precoce.
- **Dois rolamentos fixos** num eixo longo, impedindo a dilatação térmica e criando carga axial enorme.
- **Folga interna normal** quando o ajuste com interferência e a temperatura exigiam C3.
- **Ignorar a carga axial** de engrenagens helicoidais.

## Ver também

- [[Vida de rolamentos]]
- [[Montagem de rolamentos]]
- [[Ajustes recomendados]]
- [[Mancais de deslizamento]]
- [[05-elementos-de-maquinas/index|Índice do módulo 05]]
