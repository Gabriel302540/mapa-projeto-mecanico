---
title: "Parafusos: classes de resistência"
tags: [elementos, fixadores]
fontes: [ISO 898-1:2013 (parafusos de aço — propriedades mecânicas), ISO 898-2 (porcas), ISO 724 e ISO 261 (roscas métricas), VDI 2230-1, Budynas e Nisbett Elementos de Máquinas de Shigley (cap. 8)]
status: rascunho
---

**Resumo:** parafusos de aço são classificados por dois números, como 8.8 ou 10.9, que indicam a resistência à tração e a relação entre escoamento e ruptura. Junto com a área resistente da rosca, eles definem a carga de prova e a pré-carga que o parafuso pode receber. A porca deve ter classe compatível.

## O que é

### Significado da classe (ISO 898-1)

Na classe **X.Y**:

- **X × 100** = resistência à tração nominal $R_m$ (MPa).
- **X × Y × 10** = limite de escoamento nominal $R_{p0,2}$ (MPa).

| Classe | $R_m$ nominal (MPa) | $R_{p0,2}$ nominal (MPa) | Tensão de prova $S_p$ (MPa) | Material típico |
|---|---|---|---|---|
| 4.6 | 400 | 240 | 225 | Aço baixo carbono |
| 5.8 | 500 | 400 | 380 | Aço baixo carbono |
| **8.8** (d ≤ 16) | 800 | 640 | 580 | Aço médio carbono temperado e revenido |
| **8.8** (d > 16) | 830 | 660 | 600 | Idem |
| **10.9** | 1040 | 940 | 830 | Aço ligado temperado e revenido |
| **12.9** | 1220 | 1100 | 970 | Aço ligado temperado e revenido |

⚠️ verificar valores na ISO 898-1 (os nominais de 8.8 acima de M16 e as tensões de prova).

**Porcas:** classe 8 para parafusos 8.8, classe 10 para 10.9, classe 12 para 12.9. Porca de classe menor pode "espanar" a rosca antes de o parafuso atingir a carga.

### Área resistente à tração

A seção resistente de uma rosca é calculada com a média dos diâmetros primitivo e menor:

$$
A_s = \frac{\pi}{4}\left(\frac{d_2 + d_3}{2}\right)^2
$$

| Rosca (passo grosso) | Passo (mm) | $A_s$ (mm²) |
|---|---|---|
| M8 | 1,25 | 36,6 |
| M10 | 1,5 | 58,0 |
| M12 | 1,75 | 84,3 |
| M16 | 2 | 157 |
| M20 | 2,5 | 245 |
| M24 | 3 | 353 |
| M30 | 3,5 | 561 |
| M36 | 4 | 817 |

### Carga de prova e pré-carga

- **Carga de prova:** $F_p = A_s\,S_p$. É a maior carga que o parafuso suporta sem deformação permanente mensurável.
- **Pré-carga recomendada** (Shigley): $F_i \approx 0{,}75\,F_p$ para uniões reutilizáveis; $0{,}9\,F_p$ para permanentes.
- **Torque de aperto (estimativa):**

$$
T = K\,F_i\,d
$$

com $K$ (fator de torque) ≈ 0,2 para aço sem lubrificação e ≈ 0,15 lubrificado ou zincado. É uma estimativa grosseira: a dispersão do atrito faz a pré-carga real variar ±25 % ou mais com chave de torque. Ver [[08-unioes-vedacoes/index|Uniões parafusadas]] para o cálculo completo (VDI 2230).

### Marcação

Parafusos 8.8 e acima têm a classe gravada na cabeça, junto com a marca do fabricante.

## Por que importa no projeto

- **Substituir 8.8 por 4.6** "porque é o que tinha no almoxarifado" pode reduzir a pré-carga a menos da metade e fazer a união afrouxar ou romper.
- **12.9 zincado eletroliticamente** tem risco de **fragilização por hidrogênio**: ruptura retardada, sem aviso. Prefira revestimentos lamelares de zinco ou cuidados de desidrogenação.
- **Parafusos de alta resistência não devem ser soldados nem aquecidos.**

## Como aplicar (passo a passo / regras práticas)

1. **Classe usual em máquinas: 8.8**; 10.9 quando o espaço é pequeno ou a carga é alta.
2. **Porca de classe correspondente** (8 ou 10).
3. **Calcule a pré-carga** e o torque com o fator $K$ coerente com a lubrificação real.
4. **Especifique no desenho** a norma, a rosca, o comprimento, a classe e o revestimento: "ISO 4017 M20 × 80 – 8.8 – zincado".
5. **Defina o método de aperto** (torque, ângulo, tensionador hidráulico) para uniões críticas.

## Norma relacionada

- **ISO 898-1:2013**: propriedades mecânicas de parafusos de aço carbono e ligados.
- **ISO 898-2**: porcas.
- **ISO 4014 / ISO 4017**: parafusos sextavados (parcialmente roscado / totalmente roscado).
- **ISO 4762**: parafusos de cabeça cilíndrica com sextavado interno (Allen).
- **VDI 2230-1**: cálculo sistemático de uniões parafusadas.

## Exemplo prático

**Situação:** fixação da tampa de um mancal pesado com parafusos **M20 classe 8.8**, montados a seco.

- $F_p = 245 \times 600 = 147$ kN
- $F_i = 0{,}75 \times 147 \approx 110$ kN
- $T = 0{,}2 \times 110\,000 \times 0{,}020 \approx 441$ N·m

Se os parafusos forem lubrificados (K ≈ 0,15) e o mesmo torque de 441 N·m for aplicado, a pré-carga sobe para cerca de 147 kN, **igual à carga de prova**: o parafuso pode escoar. **O torque especificado tem de corresponder à condição de lubrificação real.**

> [!question] Exercício
>
> Qual a carga de prova e o torque estimado para pré-carga de 75 % de um parafuso M16 classe 10.9, lubrificado (K = 0,15)?
>
> > [!success]- Resolução
> >
> > - $F_p = 157 \times 830 \approx 130$ kN
> > - $F_i = 0{,}75 \times 130 \approx 97{,}7$ kN
> > - $T = 0{,}15 \times 97\,700 \times 0{,}016 \approx 234$ N·m

## Erros comuns

- **Misturar classes** na mesma união.
- **Torque de tabela "a seco" com parafuso lubrificado.**
- **Porca de classe inferior.**
- **Reutilizar parafusos** que trabalharam próximos do escoamento (alongados).
- **12.9 com zincagem eletrolítica sem tratamento contra hidrogênio.**

## Ver também

- [[Representação de roscas]]
- [[Cotagem de elementos]]
- [[08-unioes-vedacoes/index|Uniões e vedações]]
- [[05-elementos-de-maquinas/index|Índice do módulo 05]]
