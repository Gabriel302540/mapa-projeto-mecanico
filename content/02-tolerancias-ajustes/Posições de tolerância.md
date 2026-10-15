---
title: Posições de tolerância (letras)
tags: [tolerancias, iso-286]
fontes: [ISO 286-1:2010, ISO 286-2:2010, ABNT NBR 6158:1995, Budynas e Nisbett Elementos de Máquinas de Shigley (cap. de tolerâncias e ajustes)]
status: rascunho
---

**Resumo:** a letra da classe de tolerância (H, g, k, p...) define **onde** a faixa de tolerância fica em relação à dimensão nominal: acima, abaixo ou atravessando a linha zero. Junto com o grau IT (o número), forma a classe completa, como H7 ou g6. Maiúsculas valem para furos; minúsculas, para eixos.

## O que é

A **posição** da faixa é dada pelo **desvio fundamental**: o desvio (superior ou inferior) **mais próximo da linha zero**. A ISO 286 usa letras:

- **Furos:** A, B, C, CD, D, E, EF, F, FG, G, **H**, JS, J, K, M, N, P, R, S, T, U, V, X, Y, Z, ZA, ZB, ZC
- **Eixos:** a, b, c, cd, d, e, ef, f, fg, g, **h**, js, j, k, m, n, p, r, s, t, u, v, x, y, z, za, zb, zc

### Como as letras se posicionam (eixos)

| Letras | Posição em relação à linha zero | Desvio fundamental |
|---|---|---|
| a até g | **Abaixo** (eixo menor que o nominal) | $es$ negativo; quanto mais perto de "a", mais abaixo |
| **h** | **Encostado por baixo** | $es = 0$ |
| js | **Simétrico** | $es = +IT/2$, $ei = -IT/2$ |
| j, k, m, n | **Atravessando ou logo acima** | $ei$ pequeno (k: ≈ 0 a +5 µm) |
| p até zc | **Acima** (eixo maior que o nominal) | $ei$ positivo, crescendo até zc |

Para **furos**, é o espelho: A a G ficam **acima** da linha zero (furo maior que o nominal), **H** começa na linha zero ($EI = 0$), e K a ZC ficam progressivamente **abaixo**.

### A letra mais importante: H (e h)

- Furo **H**: $EI = 0$. O furo nunca é menor que o nominal; a tolerância fica toda "para cima".
- Eixo **h**: $es = 0$. O eixo nunca é maior que o nominal; a tolerância fica toda "para baixo".

São a base dos sistemas [[Sistema furo-base|furo-base]] e [[Sistema eixo-base|eixo-base]].

### Desvios fundamentais de eixos (µm)

Para as letras mais usadas. Para a–h o valor é $es$; para k–s é $ei$.

| Faixa (mm) | d | e | f | g | h | k* | m | n | p | s |
|---|---|---|---|---|---|---|---|---|---|---|
| > 10 a 18 | −50 | −32 | −16 | −6 | 0 | +1 | +7 | +12 | +18 | +28 |
| > 18 a 30 | −65 | −40 | −20 | −7 | 0 | +2 | +8 | +15 | +22 | +35 |
| > 30 a 50 | −80 | −50 | −25 | −9 | 0 | +2 | +9 | +17 | +26 | +43 |
| > 50 a 65 | −100 | −60 | −30 | −10 | 0 | +2 | +11 | +20 | +32 | +53 |
| > 65 a 80 | −100 | −60 | −30 | −10 | 0 | +2 | +11 | +20 | +32 | +59 |
| > 80 a 100 | −120 | −72 | −36 | −12 | 0 | +3 | +13 | +23 | +37 | +71 |
| > 100 a 120 | −120 | −72 | −36 | −12 | 0 | +3 | +13 | +23 | +37 | +79 |
| > 120 a 180 | −145 | −85 | −43 | −14 | 0 | +3 | +15 | +27 | +43 | ver norma |
| > 180 a 250 | −170 | −100 | −50 | −15 | 0 | +4 | +17 | +31 | +50 | ver norma |

\* Valor de k para graus IT4 a IT7. ⚠️ verificar todos os valores na ISO 286-2 antes de usar.

**Como calcular o outro desvio:** o desvio que falta é o fundamental mais ou menos a tolerância IT do grau escolhido (ver [[Graus IT]]):

- Letras a–h (eixo): $ei = es - IT$
- Letras k–zc (eixo): $es = ei + IT$
- Furo H: $ES = EI + IT = IT$

Para furos de K a ZC, a regra de cálculo tem correções (um termo $\Delta$) e é mais seguro **ler direto a tabela da ISO 286-2**.

## Por que importa no projeto

- **A letra define o tipo de ajuste.** Furo H com eixo g → sempre folga; com eixo k → ajuste incerto; com eixo s → sempre interferência. Ver [[Tipos de ajuste]].
- **Linguagem universal:** "Ø50 H7" é entendido por qualquer fabricante, em qualquer país, e há calibradores tampão e anel prontos para as classes usuais.
- **Catálogos de componentes** (rolamentos, buchas, acoplamentos) indicam diretamente as classes de eixo e alojamento recomendadas.

## Como aplicar (passo a passo / regras práticas)

1. Decida o tipo de ajuste pela função (folga, incerto, interferência).
2. Escolha o sistema (normalmente furo-base: furo H).
3. Escolha a letra do eixo que dá o ajuste desejado (g, h, k, m, n, p, s...).
4. Escolha os graus (furo IT7, eixo IT6 é o par mais comum).
5. Calcule os desvios: leia o desvio fundamental na tabela, some ou subtraia a tolerância IT.
6. Escreva no desenho a classe e, se for útil para a oficina, os desvios entre parênteses: **Ø50 g6** $\left(^{-0{,}009}_{-0{,}025}\right)$. Ver [[Indicação de tolerâncias]].

## Norma relacionada

- **ISO 286-1:2010**: define o sistema de letras e a lógica dos desvios fundamentais.
- **ISO 286-2:2010**: tabelas de desvios para as classes de furos e eixos.
- **ABNT NBR 6158:1995**: equivalente brasileira. ⚠️ verificar edição vigente.

## Exemplo prático

**Situação:** calcular os limites de um eixo **Ø60 m6**, que recebe uma engrenagem com chaveta.

- Faixa "> 50 a 65": $ei(m) = +11$ µm; IT6 (faixa 50 a 80) = 19 µm.
- $es = 11 + 19 = +30$ µm.
- Limites: **60,011 a 60,030 mm**.

> [!question] Exercício 1
>
> Calcule os limites de um eixo Ø25 f7 e de um eixo Ø25 h6.
>
> > [!success]- Resolução
> >
> > Faixa "> 18 a 30": IT7 = 21 µm; IT6 = 13 µm.
> > - **f7:** $es = -20$ µm; $ei = -20 - 21 = -41$ µm → **24,959 a 24,980 mm**.
> > - **h6:** $es = 0$; $ei = -13$ µm → **24,987 a 25,000 mm**.

> [!question] Exercício 2
>
> Um eixo Ø40 tem limites 40,017 e 40,033 mm. Que classe é essa?
>
> > [!success]- Resolução
> >
> > Tolerância: $33 - 17 = 16$ µm → **IT6** (faixa 30 a 50).
> > Desvio inferior: +17 µm → letra **n** (ei = +17 na faixa 30 a 50).
> > Classe: **Ø40 n6**.

## Erros comuns

- **Usar letra maiúscula para eixo** ou minúscula para furo (H7 é furo; h7 é eixo; são coisas diferentes).
- **Somar a tolerância para o lado errado** (em g, o desvio fundamental é o superior; o inferior é mais negativo).
- **Calcular desvios de furos K a ZC** pela regra simples, sem a correção da norma.
- **Usar a faixa de diâmetro errada** para a letra (os desvios de s mudam a cada subfaixa).

## Ver também

- [[Graus IT]]
- [[Sistema furo-base]]
- [[Tipos de ajuste]]
- [[Ajustes recomendados]]
- [[02-tolerancias-ajustes/index|Índice do módulo 02]]
