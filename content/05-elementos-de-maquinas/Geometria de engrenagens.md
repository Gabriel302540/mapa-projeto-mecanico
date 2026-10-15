---
title: "Engrenagens cilíndricas: geometria"
tags: [elementos, engrenagens]
fontes: [ISO 53 (perfil de referência), ISO 54 (módulos), ISO 21771 (geometria de engrenagens cilíndricas), Budynas e Nisbett Elementos de Máquinas de Shigley (cap. 13), Niemann Elementos de Máquinas (vol. de engrenagens), Maitra Handbook of Gear Design]
status: rascunho
---

**Resumo:** engrenagens cilíndricas transmitem movimento entre eixos paralelos com relação de velocidades constante, graças ao perfil evolvente dos dentes. Toda a geometria parte de dois números: o módulo (tamanho do dente) e o número de dentes. Daí saem diâmetros, distância entre centros, relação de transmissão e forças.

## O que é

### Grandezas básicas (dentes retos, sem correção)

| Grandeza | Símbolo | Fórmula |
|---|---|---|
| Módulo | $m$ | Normalizado (ISO 54): 1; 1,25; 1,5; 2; 2,5; 3; 4; 5; 6; 8; 10; 12; 16; 20... |
| Passo | $p$ | $p = \pi m$ |
| Diâmetro primitivo (de referência) | $d$ | $d = m\,z$ |
| Altura da cabeça (adendo) | $h_a$ | $h_a = m$ |
| Altura do pé (dedendo) | $h_f$ | $h_f = 1{,}25\,m$ |
| Diâmetro externo | $d_a$ | $d_a = d + 2m$ |
| Diâmetro de pé | $d_f$ | $d_f = d - 2{,}5\,m$ |
| Ângulo de pressão | $\alpha$ | 20° (padrão) |
| Diâmetro de base | $d_b$ | $d_b = d\cos\alpha$ |
| Distância entre centros | $a$ | $a = \dfrac{d_1 + d_2}{2} = \dfrac{m(z_1 + z_2)}{2}$ |
| Relação de transmissão | $i$ | $i = \dfrac{z_2}{z_1} = \dfrac{n_1}{n_2}$ |

### Por que o perfil evolvente

O perfil evolvente garante que a **linha de ação** (a direção da força entre os dentes) seja sempre a mesma reta, tangente aos dois círculos de base. Resultado:

- **Relação de velocidades constante**, sem vibração por variação de velocidade.
- **Tolerância a pequenas variações na distância entre centros**: a relação continua constante (só muda a folga entre dentes).

### Número mínimo de dentes e correção de perfil

Com $\alpha$ = 20° e dentes normais, abaixo de cerca de **17 dentes** a ferramenta de corte remove parte do pé do dente (**rebaixamento**, *undercut*), enfraquecendo-o. Soluções:

- Usar mais dentes no pinhão.
- **Correção (deslocamento) de perfil:** afastar a ferramenta do centro por $x\,m$ ($x$ = coeficiente de correção). Também usada para ajustar a distância entre centros e equilibrar a resistência entre pinhão e coroa.

### Grau de recobrimento

Número médio de pares de dentes em contato. Deve ser **maior que 1,2** (na prática 1,4 a 1,8 em dentes retos) para que um par entre em contato antes do anterior sair. Dentes helicoidais somam o recobrimento axial, funcionando mais suavemente.

### Dentes helicoidais

Os dentes são inclinados de um ângulo $\beta$ (8° a 30°). O módulo normal $m_n$ (perpendicular ao dente) é o normalizado:

$$
d = \frac{m_n\,z}{\cos\beta}
$$

Funcionam com menos ruído e maior capacidade, mas geram **força axial**.

### Forças no engrenamento

Com torque $T$ no pinhão de diâmetro $d_1$:

$$
F_t = \frac{2T}{d_1} \qquad F_r = F_t\,\tan\alpha \ \ (\text{retos}) \qquad F_r = \frac{F_t \tan\alpha_n}{\cos\beta},\ \ F_a = F_t\,\tan\beta \ \ (\text{helicoidais})
$$

Essas forças carregam eixos e rolamentos. Ver [[Dimensionamento estático de eixos]].

## Por que importa no projeto

- **Substituir uma engrenagem** exige conhecer módulo (ou passo diametral, em engrenagens de origem americana), número de dentes, ângulo de pressão, ângulo de hélice e correção de perfil. Errar qualquer um faz o par não engrenar.
- **Engrenagens abertas de grandes acionamentos** (coroas e pinhões de baixa rotação) usam módulos grandes (16, 20, 25 mm e mais).
- **As forças radiais e axiais** definem rolamentos e eixos.

## Como aplicar (passo a passo / regras práticas)

1. Defina a relação de transmissão e a distância entre centros disponível.
2. Escolha o módulo (por resistência; ver [[Dimensionamento de engrenagens]]) e os números de dentes (pinhão ≥ 17, de preferência sem divisores comuns com a coroa, para distribuir o desgaste).
3. Calcule diâmetros e distância entre centros; ajuste com correção de perfil se a distância for imposta.
4. Calcule as forças para dimensionar eixos e mancais.
5. No desenho, use a **tabela de dados da engrenagem** (módulo, z, α, β, correção, classe de qualidade, medida sobre dentes ou cota W) em vez de desenhar os dentes. Ver [[Desenho de conjunto e de detalhe]].

## Norma relacionada

- **ISO 53**: perfil de referência (cremalheira básica) para engrenagens cilíndricas.
- **ISO 54**: módulos normalizados.
- **ISO 21771**: geometria de engrenagens cilíndricas evolventes.
- **ISO 1328**: classes de qualidade (tolerâncias) de engrenagens.

## Exemplo prático

**Situação:** par de engrenagens de dentes retos, $m$ = 4 mm, $z_1$ = 20, $z_2$ = 60.

- $d_1 = 4 \times 20 = 80$ mm; $d_2 = 240$ mm
- $d_{a1} = 88$ mm; $d_{f1} = 80 - 10 = 70$ mm
- $a = (80 + 240)/2 = 160$ mm
- $i = 60/20 = 3$
- $d_{b1} = 80 \cos 20° \approx 75{,}2$ mm
- Passo: $p = 4\pi \approx 12{,}57$ mm

Se o pinhão transmite **98,8 N·m** (15 kW a 1450 rpm): $F_t = 2 \times 98\,800/80 \approx 2470$ N; $F_r = 2470 \tan 20° \approx 899$ N.

> [!question] Exercício
>
> Uma engrenagem helicoidal tem $m_n$ = 3, $z$ = 30 e $\beta$ = 20°. Calcule o diâmetro primitivo e, para $F_t$ = 5 kN, a força axial.
>
> > [!success]- Resolução
> >
> > - $d = \dfrac{3 \times 30}{\cos 20°} = \dfrac{90}{0{,}940} \approx 95{,}8$ mm
> > - $F_a = 5000 \times \tan 20° \approx 1820$ N

## Erros comuns

- **Confundir módulo normal e transversal** em engrenagens helicoidais.
- **Misturar módulo e passo diametral** (engrenagens em polegada: $m = 25{,}4/P_d$).
- **Pinhão com menos de 17 dentes sem correção** de perfil.
- **Esquecer a força axial** de helicoidais no cálculo dos rolamentos.
- **Desenhar os dentes** em vez de usar a tabela de dados.

## Ver também

- [[Dimensionamento de engrenagens]]
- [[Redutores]]
- [[Eixos estriados]]
- [[05-elementos-de-maquinas/index|Índice do módulo 05]]
