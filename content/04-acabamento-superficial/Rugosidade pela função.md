---
title: Rugosidade exigida pela função
tags: [acabamento, projeto]
fontes: [Catálogos técnicos de rolamentos (seção de assentos e acabamento), catálogos técnicos de retentores e vedações (seção de superfícies de contato), Parker O-Ring Handbook (seção de acabamento de alojamentos), Budynas e Nisbett Elementos de Máquinas de Shigley (cap. de fadiga — fator de superfície), Niemann Elementos de Máquinas]
status: rascunho
---

**Resumo:** a rugosidade certa é a mais grossa que ainda atende a função. Esta nota reúne valores de referência por aplicação (rolamentos, vedações, mancais, engrenagens, ajustes, fadiga), sempre como ponto de partida para conferir no catálogo do componente.

## O que é

### Valores de referência de Ra (µm)

| Aplicação | Ra típico | Observações |
|---|---|---|
| Assento de rolamento no eixo (até cerca de Ø80) | 0,8 | Catálogos indicam valores em função do diâmetro e da classe de tolerância |
| Assento de rolamento no eixo (diâmetros maiores) | 1,6 | |
| Alojamento de rolamento | 1,6 – 3,2 | |
| Faces de encosto de rolamento | 1,6 – 3,2 | |
| Pista de retentor de lábio (eixo) | 0,2 – 0,8 | Retificado de mergulho, sem marcas helicoidais; dureza mínima indicada pelo fabricante |
| Alojamento do retentor | 1,6 – 3,2 | |
| O-ring estático: fundo e laterais do canal | 1,6 – 3,2 | |
| O-ring dinâmico: superfície de deslizamento | 0,1 – 0,4 | |
| Faces de flange com junta plana | 3,2 – 6,3 | Algumas juntas pedem acabamento ranhurado espiral; seguir o fabricante da junta |
| Munhão de mancal de deslizamento | 0,2 – 0,8 | Muito menor que a espessura do filme de óleo |
| Bucha de mancal de deslizamento | 0,8 – 1,6 | |
| Flancos de engrenagem retificados | 0,4 – 0,8 | |
| Flancos de engrenagem fresados (geração) | 1,6 – 3,2 | |
| Ajuste com interferência (eixo) | 0,8 – 1,6 | Rugosidade reduz a interferência efetiva |
| Rasgos de chaveta (laterais) | 1,6 – 3,2 | |
| Superfícies de apoio e encosto usinadas | 3,2 – 6,3 | |
| Superfícies sem função (usinadas) | 6,3 – 12,5 | |

⚠️ todos os valores são referências compiladas de catálogos e manuais; verificar no catálogo do componente específico.

### Rugosidade e fadiga

No cálculo de fadiga de eixos, o limite de fadiga do material medido em corpos de prova polidos é reduzido por um **fator de superfície** $k_a$:

$$
k_a = a \, S_{ut}^{\,b}
$$

com $S_{ut}$ em MPa e $a$, $b$ dependentes do acabamento (Shigley):

| Acabamento | $a$ | $b$ |
|---|---|---|
| Retificado | 1,58 | −0,085 |
| Usinado ou laminado a frio | 4,51 | −0,265 |
| Laminado a quente | 57,7 | −0,718 |
| Forjado | 272 | −0,995 |

⚠️ verificar os coeficientes na edição do livro utilizada. Ver [[05-elementos-de-maquinas/index|Eixos — fadiga]].

### Rugosidade e interferência

Na montagem de um ajuste com interferência, os picos da rugosidade são parcialmente amassados. Uma regra prática usada na literatura alemã é descontar da interferência medida cerca de **0,8 × (Rz do eixo + Rz do furo)** para obter a interferência efetiva. ⚠️ verificar o fator na referência adotada.

## Por que importa no projeto

- **Componentes comprados exigem a superfície certa:** rolamentos, retentores e o-rings só atingem a vida de catálogo se o acabamento das peças vizinhas estiver dentro do recomendado.
- **Fadiga:** um eixo usinado de aço com $S_{ut}$ = 800 MPa perde quase 30 % do limite de fadiga em relação ao corpo de prova polido.
- **Custo:** cada superfície especificada fina demais custa mais e não melhora nada.

## Como aplicar (passo a passo / regras práticas)

1. **Liste as superfícies com função** (assentos, pistas de vedação, faces de junta, flancos).
2. **Consulte o catálogo do componente** que vai trabalhar sobre cada uma.
3. **Use a tabela acima** como referência inicial quando não houver catálogo.
4. **Para eixos sob fadiga**, inclua o fator $k_a$ coerente com o acabamento especificado, principalmente nos raios de concordância.
5. **Confira o processo** necessário para cada Ra (ver [[Rugosidade por processo]]).

## Norma relacionada

Não há norma que fixe a rugosidade por aplicação: os valores vêm de **catálogos de fabricantes** e da **literatura de elementos de máquinas**. A indicação no desenho segue a **ISO 21920-1**.

## Exemplo prático

**Situação:** calcular a redução do limite de fadiga de um eixo de aço SAE 1045 laminado e normalizado ($S_{ut} \approx 630$ MPa ⚠️ verificar) em dois acabamentos.

- **Usinado:** $k_a = 4{,}51 \times 630^{-0{,}265} \approx 4{,}51 \times 0{,}181 \approx 0{,}82$
- **Retificado:** $k_a = 1{,}58 \times 630^{-0{,}085} \approx 1{,}58 \times 0{,}578 \approx 0{,}91$

Retificar a região crítica aumenta o limite de fadiga em cerca de 11 % em relação à usinagem convencional, só pelo acabamento.

> [!question] Exercício
>
> Calcule $k_a$ para um eixo de aço com $S_{ut} = 1000$ MPa nas condições "usinado" e "laminado a quente". O que isso diz sobre usar aços de alta resistência sem usinar a superfície?
>
> > [!success]- Resolução
> >
> > - Usinado: $k_a = 4{,}51 \times 1000^{-0{,}265} = 4{,}51 \times 0{,}160 \approx 0{,}72$
> > - Laminado a quente: $k_a = 57{,}7 \times 1000^{-0{,}718} = 57{,}7 \times 0{,}00704 \approx 0{,}41$
> >
> > Com superfície laminada a quente, o aço de alta resistência perde quase **60 %** do limite de fadiga. Quanto mais resistente o aço, mais sensível ele é ao acabamento; usar aço nobre sem cuidar da superfície desperdiça a resistência comprada.

## Erros comuns

- **Pista de retentor torneada** com marcas helicoidais.
- **Assentos de rolamento com Ra grosso**, que se desgastam e afrouxam o ajuste.
- **Eixos de aço de alta resistência** com raios de concordância mal acabados.
- **Especificar Ra fino em faces de junta** que exigem certa rugosidade para a junta "agarrar".

## Ver também

- [[Rugosidade por processo]]
- [[Parâmetros de rugosidade]]
- [[Ajustes recomendados]]
- [[08-unioes-vedacoes/index|Uniões e vedações]]
- [[04-acabamento-superficial/index|Índice do módulo 04]]
