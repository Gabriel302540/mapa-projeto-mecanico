---
title: "Uniões soldadas: dimensionamento de cordões"
tags: [unioes, soldagem]
fontes: [Budynas e Nisbett Elementos de Máquinas de Shigley (cap. 9 — soldagem, colagem e projeto de uniões permanentes), AWS D1.1 (tensões admissíveis), EN 1993-1-8 e EN 1993-1-9 (ligações e fadiga em estruturas de aço) ⚠️ verificar, Hobbacher IIW Recommendations for Fatigue Design of Welded Joints and Components]
status: rascunho
---

**Resumo:** cordões de filete são dimensionados pela garganta. Para cargas excêntricas (suportes em balanço), trata-se o conjunto de cordões como uma linha, com propriedades de área e inércia "unitárias" multiplicadas pela garganta; somam-se as tensões de cisalhamento direto e as de flexão ou torção. Em cargas cíclicas, a resistência à fadiga da junta soldada — muito menor que a estática — costuma governar.

## O que é

### Método da solda como linha (Shigley)

1. Considere a solda como linhas sem espessura e calcule as propriedades geométricas unitárias: área $A_u$ (comprimento total), momento de inércia unitário $I_u$ ou polar $J_u$.
2. Multiplique pela garganta $a = 0{,}707\,h$ (h = perna): $I = a\,I_u$, $J = a\,J_u$.
3. Calcule as tensões:
   - Cisalhamento primário (direto): $\tau' = \dfrac{F}{a\,A_u}$
   - Flexão: $\sigma = \dfrac{M\,c}{I}$
   - Torção: $\tau'' = \dfrac{T\,r}{J}$
4. Combine vetorialmente no ponto mais solicitado e compare com a tensão admissível do código.

**Propriedades unitárias de duas linhas verticais paralelas** de comprimento $d$ (flexão em torno do eixo horizontal):

$$
A_u = 2d \qquad I_u = \frac{d^3}{6}
$$

### Fadiga de juntas soldadas

As normas de fadiga (EN 1993-1-9, recomendações do IIW) classificam cada detalhe soldado em **categorias**, que dão a faixa de tensão admissível para 2 milhões de ciclos ($\Delta\sigma_C$). Alguns detalhes comuns têm categorias da ordem de **36 a 90 MPa** de **faixa** de tensão — muito abaixo da resistência estática. ⚠️ verificar as categorias de cada detalhe na norma.

**Pontos importantes:**
- A resistência à fadiga da solda **quase não depende do aço** usado (aço de alta resistência não ajuda).
- Depende muito da **geometria do detalhe** (pé do cordão, raiz, mudança de seção).
- **Esmerilhar o pé do cordão**, tratamentos por martelamento e TIG *dressing* melhoram a fadiga.

## Por que importa no projeto

- **Suportes, consoles, bases e estruturas** sob carga excêntrica.
- **Equipamentos vibratórios** (peneiras, alimentadores, transportadores, estruturas de motores) costumam falhar por fadiga nas soldas.
- **Reparos por solda** em peças sob fadiga podem criar detalhes piores que os originais.

## Como aplicar (passo a passo / regras práticas)

1. Defina o esforço (força, excentricidade, momento) no plano da solda.
2. Escolha a geometria dos cordões e calcule $A_u$, $I_u$ ou $J_u$ (tabelas de Shigley).
3. Arbitre a perna $h$ e calcule as tensões no ponto crítico.
4. Compare com a admissível estática do código.
5. **Se houver carga cíclica**, verifique a fadiga pela categoria do detalhe.
6. Evite colocar soldas nas regiões de maior tensão variável; prefira penetração total em juntas críticas.

## Norma relacionada

- **AWS D1.1**: tensões admissíveis e detalhes de juntas (incluindo fadiga em estruturas cíclicas).
- **EN 1993-1-8 / EN 1993-1-9**: ligações e fadiga em estruturas de aço. ⚠️ verificar.
- **Recomendações do IIW**: fadiga de juntas soldadas (referência internacional).

## Exemplo prático

**Situação:** um console em balanço é soldado a uma coluna por **dois filetes verticais de 100 mm**, perna de **6 mm**. Carga vertical de **10 kN** aplicada a **150 mm** da face da solda.

- Garganta: $a = 0{,}707 \times 6 \approx 4{,}24$ mm
- Momento: $M = 10\,000 \times 150 = 1{,}5 \times 10^6$ N·mm
- $I = a\,\dfrac{d^3}{6} = 4{,}24 \times \dfrac{100^3}{6} \approx 707\,000$ mm⁴
- Flexão no topo do cordão: $\sigma = \dfrac{1{,}5\times10^6 \times 50}{707\,000} \approx 106$ MPa
- Cisalhamento direto: $\tau' = \dfrac{10\,000}{4{,}24 \times 200} \approx 11{,}8$ MPa
- Combinada: $\sqrt{106^2 + 11{,}8^2} \approx 107$ MPa

Com admissível de ≈ 144 MPa (AWS, E70, filete, tensões admissíveis ⚠️), **atende em carga estática**. Se a carga fosse cíclica (por exemplo, um equipamento vibrando), a faixa de tensão de ~107 MPa provavelmente **excederia** a categoria de fadiga do detalhe, e seria necessário aumentar os cordões ou mudar o detalhe.

> [!question] Exercício
>
> No exemplo, qual seria a tensão de flexão se o comprimento dos cordões passasse de 100 para 150 mm (mesma perna)?
>
> > [!success]- Resolução
> >
> > $I = 4{,}24 \times 150^3/6 \approx 2\,385\,000$ mm⁴; $c$ = 75 mm.
> > $\sigma = 1{,}5\times10^6 \times 75/2\,385\,000 \approx 47$ MPa.
> > Aumentar o comprimento é muito eficaz: a tensão de flexão cai com o **quadrado** do comprimento (de 106 para 47 MPa, fator $(100/150)^2 \approx 0{,}44$).

## Erros comuns

- **Ignorar a excentricidade** (calcular só o cisalhamento direto).
- **Verificar só a resistência estática** em estruturas vibratórias.
- **Usar aço de alta resistência** esperando melhorar a fadiga da solda.
- **Soldas em regiões de concentração** de tensão (cantos, mudanças de seção).

## Ver também

- [[Juntas e chanfros]]
- [[Processos de soldagem]]
- [[Uniões parafusadas]]
- [[08-unioes-vedacoes/index|Índice do módulo 08]]
