---
title: "Uniões parafusadas: pré-carga e torque"
tags: [unioes, parafusos]
fontes: [VDI 2230-1:2015, Budynas e Nisbett Elementos de Máquinas de Shigley (cap. 8 — parafusos, fixadores e uniões não permanentes), Bickford An Introduction to the Design and Behavior of Bolted Joints, ISO 898-1:2013]
status: rascunho
---

**Resumo:** numa união parafusada bem projetada, o parafuso é apertado com uma pré-carga alta, que comprime as peças. A carga externa é dividida entre o parafuso (uma fração pequena) e as peças comprimidas (a maior parte). Enquanto as peças não se separam, o parafuso sofre pouca variação de tensão — e por isso resiste à fadiga e não afrouxa. O controle da pré-carga pelo torque é impreciso, e isso deve ser considerado no cálculo.

## O que é

### Rigidez e divisão da carga

O parafuso se comporta como uma mola de rigidez $k_b$ (tracionada) e as peças comprimidas como uma mola de rigidez $k_m$. A **constante da união**:

$$
C = \frac{k_b}{k_b + k_m}
$$

Como as peças são muito mais rígidas que o parafuso, $C$ é normalmente **0,15 a 0,35**.

Com pré-carga $F_i$ e carga externa de tração $P$ por parafuso:

$$
F_b = F_i + C\,P \qquad \text{(força no parafuso)}
$$
$$
F_m = F_i - (1 - C)\,P \qquad \text{(força de compressão nas peças)}
$$

As peças **separam** quando $F_m = 0$, ou seja, com $P_0 = \dfrac{F_i}{1 - C}$. Depois disso, o parafuso passa a carregar toda a carga.

### Fadiga do parafuso

A amplitude de tensão no parafuso vem só da parcela $C\,P$:

$$
\sigma_a = \frac{C\,(P_{\max} - P_{\min})}{2\,A_s}
$$

Por isso uma pré-carga alta (que mantém as peças unidas) é a melhor proteção contra a fadiga. A rosca tem concentração de tensão alta, e os limites de fadiga de parafusos são baixos (algumas dezenas de MPa de amplitude). ⚠️ verificar na VDI 2230 ou Shigley.

### Uniões solicitadas ao cisalhamento (por atrito)

Em uniões de cisalhamento bem projetadas, a carga transversal é transmitida pelo **atrito** entre as peças, gerado pela pré-carga, e não pelo corpo do parafuso:

$$
F_Q \le \frac{n\,\mu\,F_i}{S}
$$

com $n$ parafusos, $\mu$ o coeficiente de atrito entre as superfícies (≈ 0,1–0,2 em aço usinado; maior com superfícies jateadas), e $S$ um coeficiente de segurança contra deslizamento.

### Torque e dispersão

$T = K\,F_i\,d$ (ver [[Parafusos]]). O torque controla mal a pré-carga, porque cerca de **90 % do torque é gasto vencendo o atrito** na rosca e sob a cabeça. A VDI 2230 usa um **fator de aperto** $\alpha_A = F_{\max}/F_{\min}$:

| Método de aperto | $\alpha_A$ típico |
|---|---|
| Chave de impacto | 2,5 – 4 |
| Torquímetro manual | 1,4 – 1,6 |
| Torque + ângulo (aperto até o escoamento) | 1,0 – 1,2 |
| Tensionador hidráulico | ≈ 1,1 – 1,3 (conforme o controle) |

⚠️ verificar valores na VDI 2230-1. O parafuso deve ser dimensionado para que a **menor** pré-carga provável ainda atenda à função, e a **maior** não ultrapasse o escoamento.

### Perdas de pré-carga

- **Assentamento:** achatamento das rugosidades sob a cabeça, porca e entre as peças. Reduz a pré-carga nas primeiras horas.
- **Afrouxamento por vibração transversal:** se as peças deslizam umas sobre as outras, a porca gira sozinha. A defesa principal é a pré-carga suficiente para não haver deslizamento; travas químicas e mecânicas ajudam.
- **Relaxação térmica** em temperaturas altas.

## Por que importa no projeto

- **Tampas de mancais, bases de motores e redutores, flanges de acoplamentos, uniões de estruturas sujeitas a vibração** dependem de pré-carga correta.
- **Parafusos que quebram por fadiga** quase sempre estavam com pré-carga baixa.
- **Juntas que vazam** (flanges com junta) também.

## Como aplicar (passo a passo / regras práticas)

1. **Determine as cargas externas** por parafuso (tração, cisalhamento, momentos).
2. **Escolha diâmetro e classe** (ver [[Parafusos]]) e a pré-carga alvo (≈ 70–75 % da carga de prova).
3. **Considere a dispersão** do método de aperto ($\alpha_A$): com a pré-carga mínima, verifique a não separação e o não deslizamento; com a máxima, verifique o escoamento.
4. **Verifique a fadiga** se houver carga variável.
5. **Especifique o torque e a condição de lubrificação** (e o método) no desenho ou no procedimento de montagem.
6. **Comprimentos de aperto longos** (parafusos longos e finos) aumentam a elasticidade do parafuso e reduzem a perda por assentamento.

## Norma relacionada

- **VDI 2230-1:2015**: cálculo sistemático de uniões parafusadas de alta resistência.
- **ISO 898-1**: propriedades dos parafusos.
- **ISO 16047**: ensaio de torque e pré-carga (determinação do atrito). ⚠️ verificar.

## Exemplo prático

**Situação 1 — tração:** tampa fixada por parafusos **M20 8.8** com pré-carga de **110 kN** cada (ver [[Parafusos]]). Carga externa de **30 kN por parafuso**, $C$ = 0,25.

- $F_b = 110 + 0{,}25 \times 30 = 117{,}5$ kN (o parafuso "sente" só 7,5 kN a mais)
- $F_m = 110 - 0{,}75 \times 30 = 87{,}5$ kN (as peças continuam bem comprimidas)
- Separação só com $P_0 = 110/0{,}75 \approx 147$ kN por parafuso.

**Situação 2 — cisalhamento:** os mesmos 4 parafusos prendem um suporte sujeito a força lateral. Com $\mu$ = 0,2 e $S$ = 1,25:

$$
F_Q \le \frac{4 \times 0{,}2 \times 110}{1{,}25} \approx 70\ \text{kN}
$$

Considerando um aperto com torquímetro ($\alpha_A$ ≈ 1,6), a pré-carga mínima pode ser bem menor que a nominal, e essa capacidade cairia proporcionalmente. A VDI 2230 trata isso de forma sistemática.

> [!question] Exercício
>
> Numa união com $C$ = 0,2, pré-carga de 50 kN e carga externa variando de 0 a 20 kN por parafuso, qual a variação da força no parafuso? E se a pré-carga fosse só 10 kN?
>
> > [!success]- Resolução
> >
> > - **Pré-carga 50 kN:** separação em $P_0 = 50/0{,}8 = 62{,}5$ kN > 20 kN, então não separa. Variação no parafuso: $0{,}2 \times 20 = 4$ kN.
> > - **Pré-carga 10 kN:** separação em $P_0 = 10/0{,}8 = 12{,}5$ kN < 20 kN. Acima de 12,5 kN as peças se separam, e o parafuso passa a carregar toda a carga: varia de 10 kN até 20 kN, ou seja, **10 kN de variação** — 2,5 vezes mais. Com pré-carga baixa, o parafuso sofre muito mais na fadiga.

## Erros comuns

- **Pré-carga baixa** "para não forçar o parafuso".
- **Torque especificado sem dizer se é a seco ou lubrificado.**
- **Contar com o corpo do parafuso no cisalhamento** em uniões que deveriam trabalhar por atrito.
- **Parafusos curtos e grossos** em uniões sujeitas a assentamento.
- **Arruelas de pressão (Grower)** como "trava" em uniões de alta resistência (pouca eficácia comprovada contra afrouxamento por vibração transversal). ⚠️ verificar recomendações da VDI 2230.

## Ver também

- [[Parafusos]]
- [[Juntas planas]]
- [[Pinos e cavilhas]]
- [[08-unioes-vedacoes/index|Índice do módulo 08]]
