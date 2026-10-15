---
title: Dobra de chapas
tags: [fabricacao, caldeiraria, conformacao]
fontes: [Kalpakjian e Schmid Manufacturing Engineering and Technology (cap. de conformação de chapas), Schuler Metal Forming Handbook (cap. de dobramento), catálogos técnicos de fabricantes de prensas dobradeiras e de chapas de alta resistência]
status: rascunho
---

**Resumo:** dobrar uma chapa numa prensa dobradeira cria abas e perfis a partir de chapas planas. O projeto precisa respeitar o raio mínimo de dobra do material, calcular o desenvolvimento pelo fator K e considerar o retorno elástico. A força da prensa depende do comprimento, da espessura, da resistência do material e da abertura da matriz.

## O que é

### Raio mínimo de dobra

Dobrar com raio pequeno demais trinca o lado externo. O raio interno mínimo depende do material, da espessura e da direção de laminação:

- Aços estruturais comuns (A36): raio interno da ordem de **1 a 2 vezes a espessura**.
- Aços de alta resistência e antidesgaste: **3 a 5 vezes** ou mais.
- Dobras **perpendiculares** à direção de laminação aceitam raios menores que dobras paralelas.

⚠️ verificar na especificação do fabricante da chapa.

### Desenvolvimento (fator K)

Na dobra, a linha neutra se desloca para o lado interno. O **fator K** é a posição da linha neutra como fração da espessura, medida a partir do lado interno ($0 < K \le 0{,}5$). Valores típicos: ≈ 0,33 para raios pequenos ($r \approx t$) até ≈ 0,5 para raios grandes.

**Comprimento da zona dobrada (*bend allowance*):**

$$
BA = \frac{\pi}{180}\,\theta\,(r + K\,t)
$$

com $\theta$ o ângulo de dobra (graus), $r$ o raio interno e $t$ a espessura.

**Comprimento total da chapa plana:** soma dos trechos retos (medidos até o início da curvatura) mais o BA de cada dobra.

### Retorno elástico (*springback*)

Ao retirar a carga, a chapa "volta" um pouco, abrindo o ângulo. A dobradeira compensa dobrando um pouco além. O retorno é maior em materiais de alta resistência e raios grandes.

### Força de dobra (dobra no ar, matriz em V)

Fórmula empírica comum:

$$
F \approx \frac{1{,}33\,L\,t^2\,R_m}{V}
$$

com $L$ o comprimento da dobra, $t$ a espessura, $R_m$ a resistência à tração e $V$ a abertura da matriz (tipicamente **6 a 10 vezes a espessura**; ≈ 8t é comum). ⚠️ verificar a fórmula e os fatores na tabela do fabricante da prensa.

## Por que importa no projeto

- **Peças dobradas substituem soldas**, reduzindo distorção e custo.
- **Capacidade da prensa** limita comprimento e espessura: uma chapa grossa e longa pode exceder a força disponível.
- **Furos e recortes perto da dobra** se deformam; precisam de distância mínima.

## Como aplicar (passo a passo / regras práticas)

1. **Raio interno ≥ mínimo** do material; use raios padrão das ferramentas da oficina.
2. **Aba mínima:** a aba precisa apoiar na matriz; regra prática ≈ metade da abertura V + algumas espessuras. ⚠️ verificar com a oficina.
3. **Furos a pelo menos ≈ 2 t + r da linha de dobra.**
4. **Alívios de canto** (pequenos recortes) onde duas dobras se encontram.
5. **Cote as abas pelo lado externo ou interno** de forma consistente e indique o raio interno.
6. **Verifique a força** da prensa para dobras longas e chapas grossas.

## Norma relacionada

- **Especificações das chapas** (ASTM A36, EN 10025 etc.) e **fichas técnicas** dos fabricantes de aços de alta resistência (raios mínimos).
- Não há uma norma única de dobra; os dados vêm dos fabricantes de chapas e de prensas.

## Exemplo prático

**Situação 1 — desenvolvimento:** cantoneira de chapa de **6,3 mm**, abas retas de **100** e **60 mm** (medidas até o início da curva), dobra de **90°**, raio interno **8 mm**, K = 0,4.

$$
BA = \frac{\pi}{180} \times 90 \times (8 + 0{,}4 \times 6{,}3) \approx 16{,}5\ \text{mm}
$$

Comprimento da chapa plana: $100 + 60 + 16{,}5 = 176{,}5$ mm.

**Situação 2 — força:** dobrar **2000 mm** de chapa de **6,3 mm** de aço com $R_m$ = 450 MPa, matriz de 50 mm.

$$
F \approx \frac{1{,}33 \times 2000 \times 6{,}3^2 \times 450}{50} \approx 950\ \text{kN} \approx 97\ \text{tf}
$$

Uma prensa de 100 tf estaria no limite; seria prudente usar uma de 135 tf ou mais.

> [!question] Exercício
>
> O que acontece com a força de dobra se a espessura da chapa dobrar e a matriz for trocada por uma com o dobro da abertura?
>
> > [!success]- Resolução
> >
> > A força é proporcional a $t^2/V$. Com $t \times 2$ e $V \times 2$: $F \times \dfrac{4}{2} =$ **o dobro** da força.

## Erros comuns

- **Raio interno menor que o mínimo** (trincas no lado externo).
- **Furos próximos demais da dobra.**
- **Desenvolvimento calculado pela linha média** em dobras de raio pequeno (sem fator K).
- **Ignorar o retorno elástico** em aços de alta resistência.

## Ver também

- [[Caldeiraria]]
- [[Corte térmico]]
- [[Projeto para fabricação]]
- [[07-processos-fabricacao/index|Índice do módulo 07]]
