---
title: "Engrenagens: dimensionamento"
tags: [elementos, engrenagens]
fontes: [ISO 6336 (partes 1, 2, 3 e 5), AGMA 2001-D04 / AGMA 2101 (equivalente americano), Budynas e Nisbett Elementos de Máquinas de Shigley (cap. 13 e 14), Niemann Elementos de Máquinas (vol. de engrenagens)]
status: rascunho
---

**Resumo:** um dente de engrenagem pode falhar de duas formas principais: quebra no pé por flexão (fadiga) e desgaste da superfície do flanco por pressão de contato (pitting). O dimensionamento verifica as duas tensões — de flexão no pé e de contato (Hertz) no flanco — corrigidas por fatores de aplicação, dinâmicos e de distribuição de carga, e compara com os limites do material.

## O que é

### Modos de falha

| Modo | Aparência | Causa principal |
|---|---|---|
| **Quebra do dente** | Dente arrancado, trinca no pé | Flexão excessiva, sobrecarga ou fadiga |
| **Pitting** | Pequenas crateras no flanco, perto do diâmetro primitivo | Fadiga de contato (tensão de Hertz) |
| **Desgaste abrasivo** | Flancos riscados e afinados | Contaminação do lubrificante |
| **Escoriação (*scuffing*)** | Marcas de solda e arrancamento, em faixas radiais | Quebra do filme de óleo (velocidade e carga altas, óleo inadequado) |

### Equação de Lewis (estimativa inicial de flexão)

O dente é tratado como uma viga em balanço:

$$
\sigma = \frac{K_v\,F_t}{b\,m\,Y}
$$

- $Y$: fator de forma de Lewis (depende de $z$; para $\alpha$ = 20°: z = 17 → 0,303; 20 → 0,322; 25 → 0,337; 30 → 0,359; 40 → 0,389; 50 → 0,409).
- $K_v$: fator dinâmico, por exemplo $K_v = (6{,}1 + v)/6{,}1$ para dentes fresados (Barth), com $v$ em m/s.
- $b$: largura da face, tipicamente $8m$ a $16m$.

É útil para uma primeira estimativa do módulo.

### ISO 6336 (método completo — visão geral)

**Tensão no pé do dente:**

$$
\sigma_F = \frac{F_t}{b\,m_n}\,Y_F\,Y_S\,Y_\beta\,(\ldots)\;K_A\,K_V\,K_{F\beta}\,K_{F\alpha} \le \sigma_{FP}
$$

**Tensão de contato no flanco:**

$$
\sigma_H = Z_H\,Z_E\,Z_\varepsilon\,Z_\beta\sqrt{\frac{F_t}{d_1\,b}\,\frac{u + 1}{u}}\;\sqrt{K_A\,K_V\,K_{H\beta}\,K_{H\alpha}} \le \sigma_{HP}
$$

| Fator | Significado |
|---|---|
| $K_A$ | Aplicação: choques do motor e da máquina acionada (1,0 a 2,0+) |
| $K_V$ | Dinâmico: depende da velocidade e da qualidade da engrenagem |
| $K_{H\beta}$, $K_{F\beta}$ | Distribuição de carga ao longo da face (desalinhamento, deflexão) |
| $K_{H\alpha}$, $K_{F\alpha}$ | Distribuição entre pares de dentes |
| $Z_E$ | Elasticidade: aço com aço ≈ 189,8 $\sqrt{\text{MPa}}$ |
| $Z_H$ | Geometria do contato: ≈ 2,49 para $\alpha$ = 20°, dentes retos, sem correção |
| $u$ | Relação de engrenamento $z_2/z_1$ |

As tensões admissíveis vêm dos limites do material ($\sigma_{F\lim}$, $\sigma_{H\lim}$), corrigidos por vida, tamanho, rugosidade e coeficiente de segurança. A tensão de contato admissível cresce muito com a dureza: aços cementados e temperados suportam cerca do dobro dos aços beneficiados. ⚠️ verificar valores na ISO 6336-5.

## Por que importa no projeto

- **O contato (pitting) costuma limitar** engrenagens de aço beneficiado; a flexão costuma limitar engrenagens cementadas (flanco muito duro).
- **Material e tratamento** mudam a capacidade mais que a geometria. Ver [[06-materiais/index|Materiais]].
- **Alinhamento** (fator $K_{H\beta}$) é crítico em engrenagens largas e em acionamentos com estrutura flexível.

## Como aplicar (passo a passo / regras práticas)

1. **Torque, rotação e relação** (com fator de aplicação $K_A$ pelo tipo de máquina).
2. **Estimativa do módulo** pela equação de Lewis.
3. **Verificação pela ISO 6336** (ou AGMA), normalmente com software, para flexão e contato.
4. **Escolha material e tratamento** compatíveis com as tensões.
5. **Defina a qualidade** (ISO 1328) e a lubrificação (viscosidade conforme velocidade e carga).
6. **Confira os eixos e rolamentos** com as forças do engrenamento.

## Norma relacionada

- **ISO 6336-1, -2, -3, -5**: cálculo da capacidade de carga de engrenagens cilíndricas (princípios, contato, flexão, materiais).
- **AGMA 2001 / AGMA 2101**: método americano equivalente.
- **ISO 1328-1**: classes de qualidade.

## Exemplo prático

**Situação:** pinhão de aço, **15 kW a 1450 rpm**, $m$ = 4, $z_1$ = 20 ($d_1$ = 80 mm), largura $b$ = 40 mm, dentes fresados.

**Lewis:**

- $v = \pi \times 0{,}080 \times 1450/60 \approx 6{,}07$ m/s
- $T = 9550 \times 15/1450 \approx 98{,}8$ N·m → $F_t = 2 \times 98\,800/80 \approx 2470$ N
- $K_v = (6{,}1 + 6{,}07)/6{,}1 \approx 2{,}0$
- $\sigma = \dfrac{2{,}0 \times 2470}{40 \times 4 \times 0{,}322} \approx 96$ MPa

**Contato (estimativa simplificada, coroa com $u$ = 3):** com $Z_H$ = 2,49, $Z_E$ = 189,8, $Z_\varepsilon \approx 0{,}9$ e $K_A K_V K_{H\beta} K_{H\alpha} \approx 1{,}25 \times 1{,}2 \times 1{,}3 \times 1{,}0 \approx 1{,}95$ (valores ilustrativos):

$$
\sigma_H \approx 2{,}49 \times 189{,}8 \times 0{,}9 \times \sqrt{\frac{2470}{80 \times 40} \times \frac{4}{3}} \times \sqrt{1{,}95} \approx 600\ \text{MPa}
$$

Uma tensão de contato de ~600 MPa é compatível com aço beneficiado de boa dureza; com aço cementado, haveria grande folga. ⚠️ verificar limites na ISO 6336-5.

> [!question] Exercício
>
> Pela equação de Lewis, o que acontece com a tensão de flexão se o módulo passar de 4 para 5 mm, mantendo o número de dentes e a largura?
>
> > [!success]- Resolução
> >
> > O diâmetro aumenta de 80 para 100 mm, então, para o mesmo torque, $F_t$ cai para $2470 \times 80/100 \approx 1976$ N. O denominador $b\,m\,Y$ cresce na proporção 5/4. Ignorando a variação de $K_v$ (a velocidade aumenta um pouco), a tensão cai para cerca de $96 \times (0{,}8) \times (4/5) \approx 61$ MPa, ou seja, uma redução de cerca de 36 %. A tensão de flexão cai aproximadamente com o **quadrado do módulo** quando o torque é fixo.

## Erros comuns

- **Dimensionar só por flexão**, esquecendo o contato.
- **Ignorar o fator de aplicação** em máquinas com choque (britadores, moinhos, transportadores pesados).
- **Engrenagens largas com eixos flexíveis**, gerando contato numa só ponta da face.
- **Lubrificante errado**, levando a escoriação ou pitting precoce.

## Ver também

- [[Geometria de engrenagens]]
- [[Redutores]]
- [[06-materiais/index|Materiais]]
- [[05-elementos-de-maquinas/index|Índice do módulo 05]]
