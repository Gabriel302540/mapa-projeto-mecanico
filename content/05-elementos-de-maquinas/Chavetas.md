---
title: Chavetas
tags: [elementos, eixo-cubo]
fontes: [DIN 6885-1 (chavetas paralelas), ISO/R 773 (histórica) ⚠️ verificar, DIN 6887 (chavetas inclinadas com cabeça), DIN 6888 (chavetas Woodruff), Budynas e Nisbett Elementos de Máquinas de Shigley (cap. 7), Niemann Elementos de Máquinas (cap. de uniões eixo-cubo)]
status: rascunho
---

**Resumo:** chaveta é a peça prismática que transmite torque entre um eixo e um cubo (engrenagem, polia, acoplamento), encaixada em rasgos dos dois. A chaveta paralela é a mais comum. Ela é dimensionada principalmente pela pressão de contato (esmagamento) nas faces laterais, que define o comprimento necessário.

## O que é

### Tipos

| Tipo | Características | Uso |
|---|---|---|
| **Paralela** (DIN 6885) | Faces paralelas; transmite torque pelas laterais; não fixa axialmente | O mais comum: engrenagens, polias, acoplamentos |
| **Inclinada com cabeça** (DIN 6887) | Face superior com inclinação 1:100; travada por cunha | Fixação axial também; montagem por batida. Uso decrescente por segurança (cabeça girando) |
| **Woodruff (meia-lua)** (DIN 6888) | Forma de segmento circular; o rasgo no eixo é fundo | Eixos pequenos e pontas cônicas |
| **Tangencial** | Pares de cunhas na tangente do eixo | Torques muito altos e alternados |

### Dimensões da chaveta paralela

As dimensões $b \times h$ (largura × altura) e as profundidades dos rasgos ($t_1$ no eixo, $t_2$ no cubo) são tabeladas em função da faixa de diâmetro do eixo. Exemplos (DIN 6885-1):

| Faixa de d (mm) | b × h | $t_1$ | $t_2$ |
|---|---|---|---|
| > 30 a 38 | 10 × 8 | 5,0 | 3,3 |
| > 38 a 44 | 12 × 8 | 5,0 | 3,3 |
| > 44 a 50 | 14 × 9 | 5,5 | 3,8 |
| > 50 a 58 | 16 × 10 | 6,0 | 4,3 |
| > 58 a 65 | 18 × 11 | 7,0 | 4,4 |
| > 65 a 75 | 20 × 12 | 7,5 | 4,9 |
| > 75 a 85 | 22 × 14 | 9,0 | 5,4 |
| > 85 a 95 | 25 × 14 | 9,0 | 5,4 |
| > 95 a 110 | 28 × 16 | 10,0 | 6,4 |

⚠️ verificar todos os valores na DIN 6885-1 ou na norma adotada.

### Tolerâncias

A chaveta é fabricada em **h9** de largura (sistema eixo-base; ver [[Sistema eixo-base]]). O ajuste é escolhido pela tolerância do rasgo:

| Ajuste | Rasgo no eixo | Rasgo no cubo |
|---|---|---|
| Livre (deslizante) | H9 | D10 |
| Normal | N9 | JS9 |
| Forçado | P9 | P9 |

### Dimensionamento

Força tangencial na chaveta, no raio do eixo: $F = 2T/d$.

**Pressão de contato (esmagamento)** — normalmente determinante, no lado do cubo (menor altura de contato):

$$
p = \frac{2T}{d\,(h - t_1)\,L} \le p_{\text{adm}}
$$

**Cisalhamento** da chaveta:

$$
\tau = \frac{2T}{d\,b\,L} \le \tau_{\text{adm}}
$$

Pressões admissíveis dependem do material mais fraco (cubo ou eixo) e do tipo de carga. Valores de referência da literatura: da ordem de **90 a 150 MPa** para cubos de aço sob carga estável, e bem menores para ferro fundido ou cargas com choque. ⚠️ verificar na referência adotada (Niemann, DIN 6892).

**Regras práticas de comprimento:** $L$ até cerca de **1,5 d**. Se precisar mais, considere duas chavetas a 180° (que não dobram a capacidade, pela distribuição desigual; conta-se cerca de 1,5 vezes), eixo estriado ou ajuste com interferência.

## Por que importa no projeto

- **Falhas típicas:** chaveta cisalhada, rasgo "ovalizado" (esmagado) no cubo, trinca no fundo do rasgo do eixo (concentrador). Ver [[Concentradores de tensão]].
- **A chaveta é um fusível barato?** Às vezes ela é projetada para falhar antes do eixo, mas isso só funciona se o rasgo e o eixo resistirem ao pico.
- **Ajuste eixo-cubo:** a chaveta transmite torque, mas é o ajuste (k6, m6) que centraliza a peça e evita o "batimento" que destrói a chaveta por fadiga. Ver [[Ajustes recomendados]].

## Como aplicar (passo a passo / regras práticas)

1. **Selecione b × h e $t_1$, $t_2$** pela faixa de diâmetro do eixo.
2. **Calcule o comprimento** pela pressão admissível; confira o cisalhamento.
3. **Limite $L$ a cerca de 1,5 d** e ao comprimento do cubo.
4. **Escolha o ajuste** do rasgo (normal: N9/JS9).
5. **Cote o rasgo** corretamente: $d - t_1$ no eixo e $d + t_2$ no cubo. Ver [[Cotagem de elementos]].
6. **Ajuste eixo-cubo** incerto ou leve interferência para torques alternados.
7. **Termine o rasgo longe dos raios de concordância.**

## Norma relacionada

- **DIN 6885-1**: chavetas paralelas e rasgos (forma alta).
- **DIN 6892**: cálculo de uniões com chavetas paralelas. ⚠️ verificar.
- **DIN 6887 / DIN 6888**: chavetas inclinadas e Woodruff.
- **ISO/R 773**: antiga recomendação ISO de chavetas paralelas. ⚠️ verificar norma vigente equivalente.

## Exemplo prático

**Situação:** um acoplamento é montado num eixo de **Ø80** que transmite **3000 N·m**, com cubo de aço. Chaveta 22 × 14 ($t_1$ = 9). Pressão admissível adotada: 100 MPa.

- Comprimento pela pressão:
$$
L = \frac{2T}{d\,(h - t_1)\,p_{\text{adm}}} = \frac{2 \times 3\times10^6}{80 \times (14 - 9) \times 100} = 150\ \text{mm}
$$
- Cisalhamento com L = 150: $\tau = \dfrac{2 \times 3\times10^6}{80 \times 22 \times 150} \approx 22{,}7$ MPa — muito baixo; o esmagamento manda.
- $L/d = 150/80 = 1{,}9$: **acima do recomendado**.

**Alternativas:** (a) aumentar o comprimento do cubo e aceitar 1,9 d com cuidado na distribuição de pressão; (b) usar **ajuste com interferência** (H7/s6) somado à chaveta; (c) usar **eixo estriado**; (d) usar elementos de travamento por cone (*shrink disc* ou anéis de fixação). A escolha depende do espaço, da desmontagem e do custo.

> [!question] Exercício
>
> Um eixo de Ø50 transmite 600 N·m com chaveta 14 × 9 ($t_1$ = 5,5) e cubo de 70 mm. Com $p_{\text{adm}}$ = 100 MPa, a chaveta de 63 mm atende?
>
> > [!success]- Resolução
> >
> > $p = \dfrac{2 \times 600\,000}{50 \times (9 - 5{,}5) \times 63} = \dfrac{1\,200\,000}{11\,025} \approx 109$ MPa.
> > **Não atende** (109 > 100). Com L = 70 mm (todo o cubo): $p \approx 98$ MPa → atende, mas no limite. Para margem, aumentar o cubo ou o diâmetro.

## Erros comuns

- **Dimensionar só pelo cisalhamento**, quando o esmagamento é o critério real.
- **Chaveta mais comprida que o cubo.**
- **Ajuste eixo-cubo com folga** sob torque alternado: a chaveta trabalha "batendo" e falha.
- **Rasgo terminando no raio do ressalto.**
- **Substituir chaveta original por barra comum** sem a tolerância h9 e o material correto.

## Ver também

- [[Eixos estriados]]
- [[Concentradores de tensão]]
- [[Cotagem de elementos]]
- [[Acoplamentos]]
- [[05-elementos-de-maquinas/index|Índice do módulo 05]]
