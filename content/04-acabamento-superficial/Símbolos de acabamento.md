---
title: Símbolos de acabamento no desenho
tags: [acabamento, desenho]
fontes: [ISO 21920-1:2021, ISO 1302:2002 (histórica), ABNT NBR 8404:1984 (histórica) ⚠️ verificar, Agostinho, Rodrigues e Lirani Tolerâncias, Ajustes, Desvios e Análise de Dimensões (cap. de estado de superfície)]
status: rascunho
---

**Resumo:** a textura de uma superfície é indicada no desenho por um símbolo em forma de "V" assimétrico, que diz se a remoção de material é exigida ou proibida, e por anotações em volta dele: parâmetro e valor (Ra 1,6), processo, direção das marcas e sobremetal. Uma indicação geral perto da legenda vale para todas as superfícies sem símbolo próprio.

## O que é

### O símbolo básico e suas variações

| Símbolo | Significado |
|---|---|
| **√** (dois traços desiguais a 60°) | Símbolo básico: qualquer processo é permitido. Sozinho, não tem significado; precisa de complemento |
| **√ com traço horizontal fechando o V** | **Remoção de material obrigatória** (usinagem) |
| **√ com um pequeno círculo no V** | **Remoção de material proibida**: a superfície fica como veio do processo anterior (fundida, forjada, laminada) |
| **Traço longo horizontal sobre o símbolo** | Espaço para escrever requisitos complementares |
| **Pequeno círculo no canto do traço** | O requisito vale para **todas as superfícies em torno** do contorno indicado |

### Posições das anotações (ISO 1302, ainda muito usada)

Em torno do símbolo completo, cada posição tem um papel:

| Posição | Conteúdo | Exemplo |
|---|---|---|
| Sobre o traço longo, primeira linha | Parâmetro e valor-limite (requisito principal) | Ra 1,6 |
| Segunda linha | Segundo requisito, se houver | Rz 6,3 |
| Acima do traço, à direita | Processo de fabricação, tratamento ou revestimento | retificado |
| Ao lado do V, embaixo | Direção das marcas (*lay*) | ⊥, =, X, M, C, R, P |
| À esquerda do V | Sobremetal para usinagem | 2 |

A ISO 21920-1 manteve o símbolo e passou a permitir indicar no desenho também as **condições de medição** (filtros, comprimentos) ou uma **classe de ajuste** dos filtros. ⚠️ verificar os detalhes na ISO 21920-1.

### Símbolos de direção das marcas

| Símbolo | Marcas |
|---|---|
| = | Paralelas ao plano de projeção da vista |
| ⊥ | Perpendiculares ao plano de projeção |
| X | Cruzadas em duas direções oblíquas |
| M | Multidirecionais |
| C | Aproximadamente circulares em relação ao centro |
| R | Aproximadamente radiais |
| P | Não direcionais, com partículas ou protuberâncias |

### Indicação geral

Perto da legenda, escreve-se o requisito que vale para **todas as superfícies sem indicação própria**, seguido entre parênteses do símbolo básico (ou da lista dos valores especiais usados no desenho):

$$
\sqrt{Ra\,6{,}3}\ \left(\sqrt{\ }\right)
$$

Significa: "todas as superfícies Ra 6,3, exceto as indicadas individualmente no desenho".

### Notação antiga

Desenhos brasileiros antigos usam triângulos (▽ a ▽▽▽▽) e o til (~) para superfícies em bruto, com significado definido pela antiga NBR 8404 e por padrões de empresas. Ao revisar ou copiar desenhos antigos, **converta para Ra** pela tabela da norma ou da empresa. ⚠️ verificar a correspondência.

## Por que importa no projeto

- **Especificação inequívoca:** "liso" ou "bem acabado" não são especificações. O símbolo com parâmetro e valor é.
- **Proibir remoção de material** evita que a oficina usine superfícies que devem ficar como laminadas (por exemplo, faces de chapa que serão soldadas sem necessidade de usinagem).
- **Direção das marcas** é decisiva em pistas de retentores e superfícies de deslizamento.

## Como aplicar (passo a passo / regras práticas)

1. **Coloque uma indicação geral** perto da legenda (por exemplo Ra 6,3 ou Ra 12,5 para peças de caldeiraria usinadas parcialmente).
2. **Indique individualmente** só as superfícies com exigência diferente.
3. **O símbolo toca a superfície** (ou uma linha auxiliar dela) pelo lado de fora do material, legível de baixo ou da direita da folha.
4. **Não repita** o mesmo requisito em várias vistas para a mesma superfície.
5. **Inclua o processo** só quando ele for obrigatório para a função (por exemplo "retificado sem avanço axial" numa pista de retentor).
6. **Em CAD**, use o bloco de símbolo de rugosidade com atributos.

## Norma relacionada

- **ISO 21920-1:2021**: indicação da textura de perfil em desenhos. Substitui a **ISO 1302:2002**.
- **ABNT NBR 8404**: antiga norma brasileira de indicação do estado de superfície. ⚠️ verificar se foi cancelada ou se há adoção ABNT NBR ISO.

## Exemplo prático

**Situação:** desenho de detalhe de um **eixo** com assentos de rolamento, pista de retentor e corpo livre.

- **Indicação geral:** Ra 3,2 (√) — todas as superfícies torneadas.
- **Assentos dos rolamentos:** √ com remoção obrigatória, **Ra 0,8**, "retificado".
- **Pista do retentor:** √ com remoção obrigatória, **Ra 0,4**, "retificado de mergulho", sem direção helicoidal; dureza conforme catálogo do retentor. ⚠️ verificar.
- **Faces das pontas (cortadas e faceadas):** cobertas pela indicação geral.

> [!question] Exercício
>
> Numa base soldada de chapas, as faces de apoio do motor devem ser fresadas com Ra 3,2 e o restante das chapas não deve ser usinado. Como indicar?
>
> > [!success]- Resolução
> >
> > - **Indicação geral** perto da legenda: símbolo com **círculo** (remoção proibida), significando que as superfícies ficam como laminadas, seguido de "(√)" para lembrar que há exceções.
> > - **Faces de apoio do motor:** símbolo com **traço fechando o V** (remoção obrigatória) e **Ra 3,2**, eventualmente com "fresado".
> > - Se as faces precisarem de sobremetal (chapa mais grossa para usinar depois), indicar o valor à esquerda do símbolo.

## Erros comuns

- **Símbolo básico sem valor**, que não significa nada.
- **Valores fora da série** ou sem parâmetro ("1,6" sozinho: é Ra? Rz?).
- **Esquecer a indicação geral**, deixando superfícies sem critério.
- **Converter triângulos antigos "de cabeça"**, sem a tabela de correspondência.

## Ver também

- [[Parâmetros de rugosidade]]
- [[Rugosidade por processo]]
- [[Rugosidade pela função]]
- [[04-acabamento-superficial/index|Índice do módulo 04]]
