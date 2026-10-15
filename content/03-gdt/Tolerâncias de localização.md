---
title: Tolerâncias de localização
tags: [gdt, localizacao]
fontes: [ISO 1101:2017, ISO 5458 (tolerâncias de posição de padrões), ISO 2692:2021, ASME Y14.5-2018, Krulikowski Fundamentals of Geometric Dimensioning and Tolerancing (cap. de posição)]
status: rascunho
---

**Resumo:** tolerâncias de localização controlam onde um elemento está em relação a referências: posição (a mais usada, principalmente para furos), coaxialidade/concentricidade e simetria. A posição usa cotas teoricamente exatas e uma zona normalmente cilíndrica, o que elimina o acúmulo de tolerâncias e aprova mais peças funcionais que as cotas com ±.

## O que é

| Símbolo | Característica | Zona típica | Uso |
|---|---|---|---|
| ⌖ | **Posição** | Cilindro Ø t centrado na posição teórica (para eixos de furos e pinos) | Padrões de furos, pinos, rasgos |
| ◎ | **Coaxialidade** (eixos) / **concentricidade** (pontos, numa seção) | Cilindro (ou círculo) Ø t coaxial à referência | Eixos escalonados, buchas |
| ⌯ | **Simetria** | Entre dois planos paralelos, simétricos em relação ao plano de referência | Rasgos de chaveta, ranhuras centradas |

### Posição: zona cilíndrica × zona quadrada

Com cotas ± em X e Y, a zona é um **quadrado**. Com posição Ø t, é um **círculo** (cilindro ao longo do furo).

Se o quadrado tem lado $2a$ (tolerância ±a), o círculo que passa pelos cantos tem diâmetro:

$$
\varnothing t = 2\sqrt{a^2 + a^2} = 2\sqrt{2}\,a \approx 2{,}83\,a
$$

Para ±0,1 mm, esse círculo tem Ø0,283 mm. O raciocínio funcional é o seguinte: se o parafuso passa quando o furo está deslocado 0,141 mm na diagonal (canto do quadrado), ele também passa com o mesmo deslocamento em qualquer outra direção, porque o que importa é a **distância radial** do furo à posição ideal. A zona circular aceita todos esses casos, e tem cerca de **57 % mais área** que o quadrado de 0,2 × 0,2 mm:

$$
\frac{\pi (0{,}283/2)^2}{0{,}2^2} = \frac{0{,}0629}{0{,}04} \approx 1{,}57
$$

### Conversão de medições para posição

Se um furo foi medido deslocado $\Delta x$ e $\Delta y$ da posição teórica, o diâmetro da zona que ele ocupa é:

$$
\varnothing_{\text{real}} = 2\sqrt{\Delta x^2 + \Delta y^2}
$$

O furo está aprovado se $\varnothing_{\text{real}} \le t$ (mais o bônus, se houver Ⓜ; ver [[Requisito de máximo material]]).

### Fórmulas de montagem de parafusos

Com Ⓜ e as duas peças com a mesma tolerância de posição:

- **Fixador flutuante** (parafuso passa com folga nas duas peças, preso por porca):
$$ t = H - F $$
- **Fixador fixo** (parafuso rosqueado numa das peças; folga só na outra):
$$ t_1 + t_2 = H - F $$

onde $H$ é o diâmetro mínimo do furo passante (máximo material do furo) e $F$ é o diâmetro máximo do fixador (máximo material do parafuso). No caso fixo, a tolerância é dividida entre as duas peças e, se a peça roscada tiver espessura grande em relação à folga, deve-se usar **zona projetada** Ⓟ.

## Por que importa no projeto

- **Montabilidade garantida** de flanges, tampas e bases com vários parafusos.
- **Sem acúmulo:** cada furo é localizado diretamente da referência por cotas em caixa.
- **Coaxialidade** em eixos escalonados garante que os diâmetros girem "juntos". Na prática, para peças que giram, o **batimento** costuma ser preferido, porque é mais fácil de medir (ver [[Batimento]]).
- **Simetria** de rasgos de chaveta evita que a chaveta force o cubo para um lado.

## Como aplicar (passo a passo / regras práticas)

1. **Defina as referências** (face de apoio A, diâmetro de centralização B, elemento de orientação angular C).
2. **Cote a posição teórica** de cada furo em caixa (círculo de furação, ângulos, coordenadas).
3. **Calcule a tolerância** pela fórmula do fixador (flutuante ou fixo).
4. **Use Ⓜ** em furos de passagem de parafusos: aumenta a tolerância quando o furo sai maior, sem prejudicar a montagem.
5. **Use Ⓟ** em furos roscados e furos de pinos em peças espessas.

## Norma relacionada

- **ISO 1101:2017**: definição das zonas de posição, coaxialidade e simetria.
- **ISO 5458**: tolerâncias de posição em padrões de elementos.
- **ISO 2692:2021**: requisitos de máximo e mínimo material.
- **ASME Y14.5-2018**: na edição de 2018, concentricidade e simetria foram eliminadas, e recomenda-se posição, perfil ou batimento em seu lugar.

## Exemplo prático

**Situação:** duas flanges de tubo são unidas por **8 parafusos M16** com porca (fixador flutuante). Os furos são Ø18 com tolerância +0,3/0 (Ø18,0 a 18,3).

- $H$ = 18,0 mm (furo no mínimo)
- $F$ = 16,0 mm (parafuso no máximo; o diâmetro maior nominal da rosca)
- $t = H - F = 18{,}0 - 16{,}0 = 2{,}0$ mm

Quadro dos furos:

<span class="fcf"><span>⌖</span><span>Ø2 Ⓜ</span><span>A</span><span>B</span></span>

com "8× Ø18 +0,3/0" e o círculo de furação em caixa. Uma tolerância tão grande (Ø2) mostra que os furos podem ser feitos até por corte térmico de boa qualidade, se a peça permitir. Se fosse usada uma porca sextavada em furo escareado ou houvesse restrições de espaço, o valor seria menor.

> [!question] Exercício 1
>
> Um furo deveria estar em (50, 30) e foi medido em (50,06; 29,93). A tolerância de posição é Ø0,15 sem modificador. O furo está aprovado?
>
> > [!success]- Resolução
> >
> > $\Delta x = 0{,}06$; $\Delta y = -0{,}07$.
> > $\varnothing_{\text{real}} = 2\sqrt{0{,}06^2 + 0{,}07^2} = 2\sqrt{0{,}0036 + 0{,}0049} = 2\sqrt{0{,}0085} \approx 0{,}184$ mm.
> > Como $0{,}184 > 0{,}15$, o furo está **reprovado**.
> >
> > Compare: com cotas de ±0,075 em X e em Y (um quadrado de 0,15 × 0,15), o mesmo furo seria **aprovado**, porque 0,06 e 0,07 estão ambos abaixo de 0,075. O quadrado aceita desvios maiores nas diagonais (até $0{,}075\sqrt{2} \approx 0{,}106$ do centro) do que nos eixos (0,075). A zona circular trata todas as direções igualmente, que é o que importa para um parafuso passar.

> [!question] Exercício 2
>
> Uma tampa com furos passantes Ø13 (mínimo) é presa numa carcaça com furos roscados M12, por parafusos (fixador fixo). Qual a tolerância de posição total disponível, e como dividi-la?
>
> > [!success]- Resolução
> >
> > $t_1 + t_2 = H - F = 13 - 12 = 1{,}0$ mm.
> > Uma divisão comum é dar mais para a peça que é mais difícil de fabricar com precisão. Por exemplo, **Ø0,4 Ⓜ** para os furos passantes da tampa e **Ø0,6 Ⓟ** para os furos roscados da carcaça (zona projetada na altura da tampa). Qualquer divisão que some 1,0 garante a montagem.

## Erros comuns

- **Cotas de posição com ±** ao mesmo tempo em que há tolerância de posição.
- **Esquecer o Ø** no valor da posição de furos (a zona vira entre planos).
- **Usar o fixador flutuante para um caso fixo**, dando o dobro da tolerância permitida.
- **Coaxialidade em peças que giram**, quando o batimento seria mais simples de medir.

## Ver também

- [[Requisito de máximo material]]
- [[Referências geométricas]]
- [[Quadro de tolerância]]
- [[Cotagem]]
- [[03-gdt/index|Índice do módulo 03]]
