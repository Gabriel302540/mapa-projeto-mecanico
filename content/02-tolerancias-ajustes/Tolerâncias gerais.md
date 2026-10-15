---
title: Tolerâncias gerais
tags: [tolerancias, iso-2768]
fontes: [ISO 2768-1:1989, ISO 2768-2:1989, ISO 22081:2021, ABNT NBR ISO 2768-1 ⚠️ verificar, Agostinho, Rodrigues e Lirani Tolerâncias, Ajustes, Desvios e Análise de Dimensões]
status: rascunho
---

**Resumo:** nem toda cota precisa de tolerância própria. As medidas sem tolerância indicada seguem uma tolerância geral, declarada uma vez na legenda ou numa nota, por exemplo "ISO 2768-m". Isso deixa o desenho limpo e concentra a atenção nas cotas que realmente importam.

## O que é

**Tolerâncias gerais** são valores de tolerância que valem automaticamente para **todas as cotas sem tolerância individual**. Elas correspondem à precisão "normal" da oficina: o que se obtém sem cuidado especial.

### ISO 2768-1 (dimensões lineares e angulares)

A norma define quatro classes: **f** (fina), **m** (média), **c** (grosseira) e **v** (muito grosseira).

**Dimensões lineares (mm):**

| Faixa (mm) | f | m | c | v |
|---|---|---|---|---|
| 0,5 a 3 | ±0,05 | ±0,1 | ±0,2 | — |
| > 3 a 6 | ±0,05 | ±0,1 | ±0,3 | ±0,5 |
| > 6 a 30 | ±0,1 | ±0,2 | ±0,5 | ±1 |
| > 30 a 120 | ±0,15 | ±0,3 | ±0,8 | ±1,5 |
| > 120 a 400 | ±0,2 | ±0,5 | ±1,2 | ±2,5 |
| > 400 a 1000 | ±0,3 | ±0,8 | ±2 | ±4 |
| > 1000 a 2000 | ±0,5 | ±1,2 | ±3 | ±6 |
| > 2000 a 4000 | — | ±2 | ±4 | ±8 |

**Raios externos e chanfros:**

| Faixa (mm) | f e m | c e v |
|---|---|---|
| 0,5 a 3 | ±0,2 | ±0,4 |
| > 3 a 6 | ±0,5 | ±1 |
| > 6 | ±1 | ±2 |

**Ângulos** (pelo comprimento do lado menor):

| Lado menor (mm) | f e m | c | v |
|---|---|---|---|
| até 10 | ±1° | ±1°30' | ±3° |
| > 10 a 50 | ±0°30' | ±1° | ±2° |
| > 50 a 120 | ±0°20' | ±0°30' | ±1° |
| > 120 a 400 | ±0°10' | ±0°15' | ±0°30' |
| > 400 | ±0°5' | ±0°10' | ±0°20' |

⚠️ verificar todos os valores na ISO 2768-1.

### ISO 2768-2 (tolerâncias geométricas gerais)

Define classes **H**, **K** e **L** para retitude, planeza, perpendicularidade, simetria e batimento sem indicação individual. A indicação combinada fica, por exemplo, **"ISO 2768-mK"**: classe m para dimensões e K para geometria.

**Atenção:** a ISO 2768-2 foi **cancelada** e substituída pela **ISO 22081:2021**, que trata das especificações geométricas gerais de outro modo. Muitos desenhos e empresas ainda usam "ISO 2768-mK". ⚠️ verificar o padrão adotado. Ver [[03-gdt/index|GD&T]].

### Outros casos

- **Peças soldadas:** usam normas próprias de tolerâncias gerais para construções soldadas (por exemplo, ISO 13920, classes A a D para dimensões e E a H para geometria). Ver [[07-processos-fabricacao/index|Processos de fabricação]].
- **Peças fundidas e forjadas:** têm normas específicas de tolerâncias (por exemplo, ISO 8062 para fundidos). ⚠️ verificar.

## Por que importa no projeto

- **Desenho limpo:** a maioria das cotas de uma peça não é funcional. Sem tolerância geral, ou cada cota teria uma tolerância escrita, ou ficaria indefinida.
- **Contrato claro:** uma cota sem tolerância e sem nota geral é uma cota sem critério de aceitação. Qualquer peça "serve" ou nenhuma serve.
- **Custo:** a classe m corresponde à precisão normal de uma oficina de usinagem; f exige cuidado extra; c e v servem para caldeiraria e corte térmico.

## Como aplicar (passo a passo / regras práticas)

1. **Declare a tolerância geral** na legenda ou numa nota: "TOLERÂNCIAS GERAIS: ISO 2768-m" (ou "-mK"). Ver [[Legenda]].
2. **Escolha a classe pelo processo:**
   - usinagem de precisão → f
   - usinagem geral → **m** (a mais comum)
   - caldeiraria, corte e solda → c (ou a norma de soldados)
   - peças brutas → v
3. **Dê tolerância individual só às cotas funcionais** (ajustes, posicionamentos críticos).
4. **Confira se a tolerância geral não é mais apertada que o necessário** em peças grandes de caldeiraria.

## Norma relacionada

- **ISO 2768-1:1989**: tolerâncias gerais para dimensões lineares e angulares.
- **ISO 2768-2:1989**: tolerâncias geométricas gerais (substituída pela ISO 22081:2021).
- **ISO 22081:2021**: especificações geométricas e dimensionais gerais.
- **ISO 13920**: tolerâncias gerais para construções soldadas.

## Exemplo prático

**Situação:** uma **chapa de base** de aço, cortada a plasma e depois usinada só nos furos dos chumbadores e na face de apoio do motor, com dimensões externas de 1200 × 600 mm.

- Se a nota geral fosse "ISO 2768-m", o contorno de 1200 mm teria ±0,8 mm, difícil de garantir no corte a plasma e desnecessário para a função.
- **Solução:** nota geral "ISO 2768-c" para a peça (1200 ± 2 mm, 600 ± 2 mm), e tolerâncias individuais só para a posição dos furos dos chumbadores e para a planeza da face de apoio.

> [!question] Exercício
>
> Numa peça com nota "ISO 2768-m", qual a tolerância de uma cota de 85 mm, de um raio de 4 mm e de um ângulo de 30° com lado menor de 40 mm?
>
> > [!success]- Resolução
> >
> > - 85 mm (faixa > 30 a 120): **±0,3 mm**.
> > - Raio de 4 mm (faixa > 3 a 6): **±0,5 mm**.
> > - Ângulo com lado menor de 40 mm (faixa > 10 a 50): **±0°30'**.

## Erros comuns

- **Desenho sem nenhuma indicação de tolerância geral.**
- **Usar classe f em peças de caldeiraria**, impossível de atingir sem usinagem.
- **Esquecer que a ISO 2768-2 foi substituída** e citar só "-mK" em projetos novos sem conferir o padrão da empresa.
- **Aplicar tolerância geral a uma cota funcional**, como o diâmetro de um assento de rolamento.

## Ver também

- [[Conceitos de tolerância]]
- [[Indicação de tolerâncias]]
- [[Legenda]]
- [[02-tolerancias-ajustes/index|Índice do módulo 02]]
