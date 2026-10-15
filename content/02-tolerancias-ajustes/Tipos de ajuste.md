---
title: "Tipos de ajuste: folga, incerto e interferência"
tags: [tolerancias, ajustes]
fontes: [ISO 286-1:2010, Budynas e Nisbett Elementos de Máquinas de Shigley (cap. de tolerâncias e ajustes e cap. de eixos), Norton Projeto de Máquinas (cap. de eixos — ajustes de interferência), Agostinho, Rodrigues e Lirani Tolerâncias, Ajustes, Desvios e Análise de Dimensões]
status: rascunho
---

**Resumo:** um ajuste é a relação entre um furo e um eixo montados. Se o furo é sempre maior que o eixo, há folga; se é sempre menor, há interferência; se as faixas se sobrepõem, o ajuste é incerto e pode resultar em uma ou outra coisa. Calcular as folgas e interferências máximas e mínimas é o que mostra se o ajuste atende a função.

## O que é

### Definições

- **Folga ($F$):** diferença positiva entre o diâmetro do furo e o do eixo, quando o furo é maior.
- **Interferência ($I$):** diferença entre o eixo e o furo, quando o eixo é maior. Para montar, é preciso forçar (prensa) ou dilatar o furo (aquecimento) ou contrair o eixo (resfriamento).

### Fórmulas

$$
F_{\max} = D_{\max} - d_{\min} = ES - ei
$$
$$
F_{\min} = D_{\min} - d_{\max} = EI - es
$$

Se $F_{\min}$ der **negativo**, isso significa interferência: $I_{\max} = -F_{\min} = es - EI$. Da mesma forma, se $F_{\max}$ der negativo, $I_{\min} = -F_{\max} = ei - ES$.

### Os três tipos

| Tipo | Condição | No diagrama | Uso típico |
|---|---|---|---|
| **Com folga** | $F_{\min} \geq 0$ (furo mínimo ≥ eixo máximo) | Faixa do furo **toda acima** da do eixo | Peças que giram ou deslizam uma sobre a outra |
| **Incerto (de transição)** | $F_{\max} > 0$ e $F_{\min} < 0$ | Faixas **se sobrepõem** | Peças que precisam de centralização precisa e devem ser desmontáveis |
| **Com interferência** | $F_{\max} \leq 0$ (furo máximo ≤ eixo mínimo) | Faixa do furo **toda abaixo** da do eixo | Peças que transmitem força ou torque sem outro elemento, ou que não podem afrouxar |

**Tolerância do ajuste:** é a variação total possível da folga (ou interferência), igual à soma das tolerâncias do furo e do eixo:

$$
T_{\text{ajuste}} = T_{\text{furo}} + T_{\text{eixo}} = F_{\max} - F_{\min}
$$

Isso mostra que **apertar uma das tolerâncias reduz a variação do ajuste**, e é por isso que ajustes de precisão exigem graus IT baixos nas duas peças.

### Montagem de ajustes com interferência

- **Prensagem a frio:** para interferências pequenas e peças pequenas. Exige chanfro de entrada e lubrificação.
- **Montagem térmica:** aquece-se o cubo (ou resfria-se o eixo) até haver folga. A diferença de temperatura necessária é:

$$
\Delta T = \frac{I_{\max} + F_{\text{montagem}}}{\alpha \cdot d}
$$

onde $\alpha$ é o coeficiente de dilatação térmica (aço: cerca de $11{,}5 \times 10^{-6}$ /°C) e $F_{\text{montagem}}$ é uma folga extra para a peça entrar sem travar (regra prática: cerca de 0,001 × d). ⚠️ verificar os limites de temperatura do material e de componentes como retentores e rolamentos (rolamentos, normalmente, não devem passar de cerca de 120 °C).

## Por que importa no projeto

- **Folga demais** num mancal gera batimento e desgaste; **folga de menos** gera aquecimento e travamento.
- **Ajuste incerto** é ideal para centralizar com precisão uma peça que precisa ser desmontada em manutenção, mas exige um elemento (chaveta, parafuso, porca) para transmitir torque ou impedir o deslocamento.
- **Interferência** transmite torque sem chaveta e não afrouxa com vibração, mas dificulta a desmontagem e gera tensões no cubo que precisam ser verificadas (ver [[08-unioes-vedacoes/index|Uniões por interferência]]).

## Como aplicar (passo a passo / regras práticas)

1. **Defina a função:** gira? desliza? posiciona? transmite torque?
2. **Escolha um ajuste preferencial** (ver [[Ajustes recomendados]]).
3. **Calcule** $F_{\max}$ e $F_{\min}$ (ou $I_{\max}$, $I_{\min}$).
4. **Verifique a função nos extremos:**
   - folga mínima ainda suficiente para o filme de óleo e a dilatação térmica?
   - interferência mínima ainda suficiente para transmitir o torque?
   - interferência máxima não gera tensão excessiva no cubo nem dificulta a montagem?
5. **Ajuste o grau ou a letra** se algum extremo não atender.

## Norma relacionada

- **ISO 286-1:2010**: definição de ajustes com folga, incerto e com interferência, e ajustes preferenciais.
- **ABNT NBR 6158:1995**: equivalente brasileira. ⚠️ verificar edição vigente.

## Exemplo prático

**Situação:** o cubo de um acoplamento de aço deve ser montado a quente numa ponta de eixo **Ø80 H7/s6**, sem chaveta auxiliar.

**1. Limites** (faixa "> 65 a 80"; IT7 = 30 µm; IT6 = 19 µm; s: $ei = +59$ µm; ⚠️ verificar na ISO 286-2):

- Furo H7: 80,000 a 80,030 mm
- Eixo s6: $ei = +59$, $es = +78$ µm → 80,059 a 80,078 mm

**2. Interferências:**

- $I_{\max} = es - EI = 78 - 0 = 78$ µm
- $I_{\min} = ei - ES = 59 - 30 = 29$ µm

É um ajuste com interferência garantida: mesmo no pior caso há 29 µm de aperto.

**3. Temperatura de montagem** (folga de montagem ≈ 0,001 × 80 = 80 µm):

$$
\Delta T = \frac{78 + 80}{11{,}5 \times 10^{-6} \times 80\,000\ \text{µm}} \approx \frac{158}{0{,}92} \approx 172\ °\text{C}
$$

Com o ambiente a 25 °C, o cubo deve ser aquecido a cerca de **200 °C** (em forno ou aquecedor por indução), temperatura aceitável para um cubo de aço sem vedações montadas.

> [!question] Exercício 1
>
> Classifique o ajuste Ø50 H7/n6 e calcule seus extremos.
>
> > [!success]- Resolução
> >
> > Faixa "> 30 a 50": IT7 = 25; IT6 = 16; n: $ei = +17$ µm.
> > - Furo: 50,000 a 50,025; eixo n6: 50,017 a 50,033.
> > - $F_{\max} = 25 - 17 = +8$ µm (folga)
> > - $F_{\min} = 0 - 33 = -33$ µm → interferência máxima de 33 µm
> >
> > Como pode haver folga (8 µm) ou interferência (33 µm), é um **ajuste incerto**, com tendência forte à interferência.

> [!question] Exercício 2
>
> Num ajuste Ø40 H8/f7, qual é a tolerância do ajuste? Confira pela soma das tolerâncias.
>
> > [!success]- Resolução
> >
> > Faixa "> 30 a 50": IT8 = 39; IT7 = 25; f: $es = -25$ µm, $ei = -50$ µm.
> > - $F_{\max} = 39 - (-50) = 89$ µm; $F_{\min} = 0 - (-25) = 25$ µm.
> > - Tolerância do ajuste $= 89 - 25 = 64$ µm $= 39 + 25$ ✔

## Erros comuns

- **Calcular só a folga média** e ignorar os extremos.
- **Esquecer a dilatação térmica em operação:** um eixo de aço numa bucha de bronze aquecida muda a folga real.
- **Ajuste incerto sem elemento de travamento**, esperando que ele transmita torque.
- **Montar ajuste com interferência a frio** em peças grandes, danificando as superfícies (escoriação).

## Ver também

- [[Sistema furo-base]]
- [[Ajustes recomendados]]
- [[Conceitos de tolerância]]
- [[02-tolerancias-ajustes/index|Índice do módulo 02]]
