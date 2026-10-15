---
title: "Eixos: dimensionamento à fadiga"
tags: [elementos, eixos, fadiga]
fontes: [Budynas e Nisbett Elementos de Máquinas de Shigley (cap. 6 — falha por fadiga; cap. 7 — eixos), Norton Projeto de Máquinas (cap. de fadiga e de eixos), DIN 743-1 a 743-3, Collins Failure of Materials in Mechanical Design]
status: rascunho
---

**Resumo:** num eixo que gira sob flexão, cada ponto da superfície passa de tração para compressão a cada volta. Essa tensão alternada, mesmo bem abaixo do escoamento, provoca trincas que crescem até a ruptura. O dimensionamento à fadiga corrige o limite de fadiga do material para as condições reais (acabamento, tamanho, confiabilidade, concentradores) e combina tensões alternadas e médias por um critério como o de Goodman.

## O que é

### Tensões alternada e média

Num eixo girando com momento fletor de direção fixa e torque constante:

- A **flexão é totalmente alternada**: $M_a = M$, $M_m = 0$.
- A **torção é constante**: $T_m = T$, $T_a = 0$ (se o torque não oscila).

Se o torque oscila (acionamentos com choques), aparece $T_a$; se há forças girando com o eixo (desbalanceamento), aparece $M_m$.

### Limite de fadiga corrigido (Marin)

$$
S_e = k_a\,k_b\,k_c\,k_d\,k_e\,k_f\,S_e'
$$

| Fator | Significado | Valores típicos |
|---|---|---|
| $S_e'$ | Limite de fadiga do corpo de prova polido | Aços: $\approx 0{,}5\,S_{ut}$ (até $S_{ut}$ = 1400 MPa); 700 MPa acima |
| $k_a$ | Superfície | $a\,S_{ut}^{\,b}$; usinado: $a$ = 4,51, $b$ = −0,265. Ver [[Rugosidade pela função]] |
| $k_b$ | Tamanho (flexão e torção, eixo girando) | $1{,}24\,d^{-0{,}107}$ para 2,79 ≤ d ≤ 51 mm; $1{,}51\,d^{-0{,}157}$ para 51 < d ≤ 254 mm |
| $k_c$ | Tipo de carga | Flexão 1; axial 0,85; torção pura 0,59 (no critério de von Mises usa-se 1 e combina-se pela fórmula) |
| $k_d$ | Temperatura | 1 até cerca de 250 °C |
| $k_e$ | Confiabilidade | 50 % → 1; 90 % → 0,897; 95 % → 0,868; 99 % → 0,814; 99,9 % → 0,753 |
| $k_f$ | Efeitos diversos (corrosão, revestimentos, tensões residuais) | 1, salvo dados |

⚠️ verificar coeficientes na edição do livro adotada.

### Concentradores

Ressaltos, rasgos e canais elevam a tensão local por um fator de fadiga $K_f$ (flexão) e $K_{fs}$ (torção). Ver [[Concentradores de tensão]].

### Critério DE-Goodman (Shigley)

Combinando von Mises com a linha de Goodman:

$$
\frac{1}{n} = \frac{16}{\pi d^3}\left\{\frac{1}{S_e}\left[4(K_f M_a)^2 + 3(K_{fs} T_a)^2\right]^{1/2} + \frac{1}{S_{ut}}\left[4(K_f M_m)^2 + 3(K_{fs} T_m)^2\right]^{1/2}\right\}
$$

Para o caso usual (flexão alternada, torque constante):

$$
d = \left[\frac{16\,n}{\pi}\left(\frac{2K_f M_a}{S_e} + \frac{\sqrt{3}\,K_{fs} T_m}{S_{ut}}\right)\right]^{1/3}
$$

Como $k_b$ depende de $d$, o cálculo é **iterativo**: estima-se $k_b$ (por exemplo 0,8), calcula-se $d$, recalcula-se $k_b$ e repete-se.

Além disso, verifica-se o **escoamento na primeira volta** (tensão máxima de von Mises com $M_a + M_m$ e $T_a + T_m$, comparada com $S_y$).

## Por que importa no projeto

- **A fadiga é a causa da grande maioria das quebras de eixos** em serviço. A fratura típica mostra marcas de praia (crescimento lento da trinca) e uma pequena zona de ruptura final.
- **Detalhes de projeto valem mais que o material:** um raio de concordância maior ou um rasgo de chaveta bem posicionado aumentam mais a vida do que trocar o aço.
- **Peças de reposição redesenhadas** sem considerar a fadiga repetem a falha.

## Como aplicar (passo a passo / regras práticas)

1. Faça os diagramas de momento e torque (ver [[Dimensionamento estático de eixos]]).
2. Liste as **seções críticas**: momento alto + concentrador.
3. Para cada uma: escolha $K_f$, $K_{fs}$; calcule $S_e$ com estimativa de $k_b$.
4. Calcule $d$ pelo DE-Goodman com $n$ entre 1,5 e 2,5 (conforme a incerteza das cargas).
5. Recalcule $k_b$ com o $d$ obtido e repita até convergir.
6. Verifique o escoamento na primeira volta.
7. Arredonde para um diâmetro comercial e confira o coeficiente de segurança final.

## Norma relacionada

- **DIN 743** (partes 1 a 4): método alemão completo para eixos, com coeficientes próprios para concentradores, tamanho e superfície.
- O método de Marin e os critérios de Goodman, Gerber e ASME-elíptico vêm da **literatura** (Shigley, Norton).

## Exemplo prático

**Situação:** o mesmo eixo da nota [[Dimensionamento estático de eixos]]: **SAE 1045** ($S_{ut} \approx 630$ MPa ⚠️), usinado, **75 kW a 300 rpm** ($T$ = 2387,5 N·m), momento de **3000 N·m** no ressalto do mancal, com raio de concordância generoso. Confiabilidade 95 %, $n$ = 2.

1. $S_e' = 0{,}5 \times 630 = 315$ MPa
2. $k_a = 4{,}51 \times 630^{-0{,}265} \approx 0{,}82$
3. $k_b$ (para d ≈ 90): $1{,}51 \times 90^{-0{,}157} \approx 0{,}745$
4. $k_e = 0{,}868$
5. $S_e = 0{,}82 \times 0{,}745 \times 0{,}868 \times 315 \approx 167$ MPa
6. Concentradores (ressalto bem arredondado, estimativa inicial): $K_f \approx 1{,}6$; $K_{fs} \approx 1{,}4$
7. Diâmetro:
$$
d = \left[\frac{16 \times 2}{\pi}\left(\frac{2 \times 1{,}6 \times 3\times10^6}{167} + \frac{\sqrt{3} \times 1{,}4 \times 2{,}39\times10^6}{630}\right)\right]^{1/3} \approx 88\ \text{mm}
$$
8. Diâmetro comercial: **Ø90**, com coeficiente de segurança resultante ≈ 2,1.

Compare: o critério estático pedia 52 mm. **A fadiga exigiu um eixo cerca de 70 % mais grosso.**

> [!question] Exercício
>
> No exemplo acima, o que aconteceria com o diâmetro necessário se o ressalto tivesse canto vivo ($K_f \approx 2{,}5$, $K_{fs} \approx 2{,}0$)? Estime.
>
> > [!success]- Resolução
> >
> > O termo dominante é o da flexão: $2 K_f M_a / S_e$. Com $K_f$ = 2,5 em vez de 1,6, ele cresce 56 %; o termo da torção cresce 43 %.
> > - Termo de flexão: $2 \times 2{,}5 \times 3\times10^6 / 167 \approx 89\,820$
> > - Termo de torção: $\sqrt{3} \times 2{,}0 \times 2{,}39\times10^6 / 630 \approx 13\,140$
> > - $d = [10{,}19 \times 102\,960]^{1/3} \approx 102$ mm
> >
> > Só por causa do canto vivo, o eixo precisaria passar de Ø90 para cerca de **Ø105**. Um raio bem feito economiza material e peso.

## Erros comuns

- **Usar $S_y$ ou $S_{ut}$ diretamente** como tensão admissível em eixos girantes.
- **Esquecer os fatores de Marin**, principalmente superfície e tamanho.
- **Ignorar o concentrador** do rasgo de chaveta ou do canal de anel elástico.
- **Raio de concordância não especificado** no desenho (a oficina faz canto vivo).
- **Soldar** em eixos sob fadiga (por exemplo, para recuperar um assento), criando concentradores e zonas termicamente afetadas.

## Ver também

- [[Dimensionamento estático de eixos]]
- [[Concentradores de tensão]]
- [[Rugosidade pela função]]
- [[06-materiais/index|Materiais]]
- [[05-elementos-de-maquinas/index|Índice do módulo 05]]
