---
title: Sistema furo-base
tags: [tolerancias, ajustes]
fontes: [ISO 286-1:2010, ABNT NBR 6158:1995, Budynas e Nisbett Elementos de Máquinas de Shigley (cap. de tolerâncias e ajustes), Agostinho, Rodrigues e Lirani Tolerâncias, Ajustes, Desvios e Análise de Dimensões]
status: rascunho
---

**Resumo:** no sistema furo-base, todos os furos têm a mesma posição de tolerância (H, com desvio inferior zero), e o tipo de ajuste é obtido variando a letra do eixo. É o sistema mais usado na mecânica, porque é muito mais fácil e barato variar o diâmetro de um eixo do que o de um furo.

## O que é

Num ajuste, duas peças com a **mesma dimensão nominal** se encaixam: um furo e um eixo. O ajuste resultante (folga, incerto ou interferência) depende da posição relativa das duas faixas de tolerância. Para não ter combinações infinitas, padroniza-se uma das peças:

- **Furo-base:** o **furo é sempre H** ($EI = 0$). Folga, incerto ou interferência são obtidos pela letra do **eixo**.
- **Eixo-base:** o **eixo é sempre h** ($es = 0$). O ajuste é obtido pela letra do **furo**. Ver [[Sistema eixo-base]].

No furo-base, a sequência de ajustes, do mais folgado ao mais apertado, é simplesmente percorrer as letras do eixo:

$$
\underbrace{\text{a, b, c, d, e, f, g}}_{\text{folga}} \;\; \underbrace{\text{h}}_{\text{folga mín. zero}} \;\; \underbrace{\text{js, j, k, m, n}}_{\text{incerto (em geral)}} \;\; \underbrace{\text{p, r, s, t, u...}}_{\text{interferência (em geral)}}
$$

A fronteira exata entre incerto e interferência depende dos graus IT. Por exemplo, H7/n6 é incerto, e H7/p6 é interferência leve em boa parte das faixas. Sempre confira calculando. Ver [[Tipos de ajuste]].

## Por que importa no projeto

- **Ferramentas:** furos de precisão são acabados com alargadores, mandriladoras e brochas de diâmetro fixo e são verificados com calibradores tampão. Padronizando o furo em H7, a fábrica precisa de **um alargador e um calibrador por diâmetro**, em vez de um para cada tipo de ajuste.
- **Eixos são fáceis de variar:** no torno ou na retífica, mudar o diâmetro em alguns micrômetros é só ajustar a máquina, e a medição é feita com micrômetro.
- **Compatibilidade com catálogos:** a maioria das recomendações de ajuste (inclusive de rolamentos para o eixo) parte do furo-base.

## Como aplicar (passo a passo / regras práticas)

1. **Fixe o furo em H**, normalmente **H7** (ou H8 em ajustes menos precisos, H11 em ajustes grosseiros).
2. **Escolha a letra do eixo** pelo ajuste desejado:
   - folga de giro ou deslizamento → f, g
   - posicionamento com folga mínima zero → h
   - posicionamento preciso, desmontável → js, k
   - fixação com montagem por prensa leve → m, n
   - fixação permanente por interferência → p, r, s
3. **Escolha o grau do eixo** um grau abaixo do furo (H7 → eixo 6).
4. **Calcule folgas e interferências máximas e mínimas** para conferir se o ajuste atende a função.

## Norma relacionada

- **ISO 286-1:2010**: define os sistemas furo-base e eixo-base e recomenda ajustes preferenciais.
- **ABNT NBR 6158:1995**: equivalente brasileira. ⚠️ verificar edição vigente.

## Exemplo prático

**Situação:** num redutor, três peças montam em eixos de Ø50 com furos usinados em **H7** (50,000 a 50,025 mm):

| Peça | Função | Eixo | Limites do eixo (mm) | Resultado |
|---|---|---|---|---|
| Bucha de bronze sobre eixo girando | Girar com folga | g6 | 49,975 a 49,991 | Folga de 9 a 50 µm |
| Cubo de engrenagem com chaveta | Posicionar, desmontável | k6 | 50,002 a 50,018 | Incerto: folga até 23 µm ou interferência até 18 µm |
| Bucha espaçadora fixa | Fixar sem chaveta | s6 | 50,043 a 50,059 | Interferência de 18 a 59 µm |

Os três furos são feitos com **o mesmo alargador e conferidos com o mesmo calibrador H7**. Só o eixo muda.

> [!question] Exercício
>
> Para um ajuste Ø30 H7/g6, calcule a folga máxima e a mínima.
>
> > [!success]- Resolução
> >
> > Faixa "> 18 a 30": IT7 = 21 µm; IT6 = 13 µm; g: $es = -7$ µm.
> > - Furo H7: 30,000 a 30,021 mm.
> > - Eixo g6: $es = -7$, $ei = -7 - 13 = -20$ µm → 29,980 a 29,993 mm.
> > - **Folga máxima** = furo máx − eixo mín = $30{,}021 - 29{,}980 = 0{,}041$ mm = 41 µm.
> > - **Folga mínima** = furo mín − eixo máx = $30{,}000 - 29{,}993 = 0{,}007$ mm = 7 µm.

## Erros comuns

- **Misturar sistemas** sem motivo no mesmo projeto (alguns furos em H, outros em K, M, N...), o que multiplica ferramentas e calibradores.
- **Achar que H7 é "um diâmetro"**: H7 é uma faixa de 0 a +IT7.
- **Usar furo-base para eixos lisos longos** com várias peças montadas (aí o eixo-base pode ser melhor; ver [[Sistema eixo-base]]).

## Ver também

- [[Sistema eixo-base]]
- [[Tipos de ajuste]]
- [[Ajustes recomendados]]
- [[02-tolerancias-ajustes/index|Índice do módulo 02]]
