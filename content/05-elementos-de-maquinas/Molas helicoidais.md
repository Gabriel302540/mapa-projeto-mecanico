---
title: Molas helicoidais
tags: [elementos, molas]
fontes: [Budynas e Nisbett Elementos de Máquinas de Shigley (cap. 10 — molas mecânicas), EN 13906-1 (molas helicoidais de compressão — cálculo) ⚠️ verificar, DIN 2095 (tolerâncias de molas de compressão), Norton Projeto de Máquinas (cap. de molas)]
status: rascunho
---

**Resumo:** molas helicoidais de compressão armazenam energia e aplicam força proporcional à deformação. O fio trabalha principalmente em torção. O projeto relaciona diâmetro do fio, diâmetro médio da espira e número de espiras com a rigidez e a tensão, que precisa ficar abaixo do limite do material — inclusive na fadiga, quando a mola trabalha ciclicamente.

## O que é

### Grandezas

| Símbolo | Grandeza |
|---|---|
| $d$ | Diâmetro do fio |
| $D$ | Diâmetro médio da espira |
| $C = D/d$ | Índice da mola (recomendado entre 4 e 12) |
| $N_a$ | Número de espiras ativas |
| $N_t$ | Número total de espiras (inclui as das pontas) |
| $G$ | Módulo de elasticidade transversal (aço ≈ 79,3 GPa) |

### Rigidez (constante elástica)

$$
k = \frac{F}{y} = \frac{d^4\,G}{8\,D^3\,N_a}
$$

Repare na sensibilidade: o fio entra na **quarta potência** e o diâmetro médio na **terceira**.

### Tensão no fio

$$
\tau = K_W\,\frac{8\,F\,D}{\pi\,d^3}
$$

com o **fator de Wahl**, que corrige a curvatura e o cisalhamento direto:

$$
K_W = \frac{4C - 1}{4C - 4} + \frac{0{,}615}{C}
$$

(Para carga estática, pode-se usar o fator de Bergsträsser ou $K_s = 1 + 0{,}5/C$, que só considera o cisalhamento direto, já que o efeito da curvatura se alivia por escoamento local.)

### Materiais e resistência

A resistência à tração do arame diminui com o diâmetro (arame fino é mais resistente):

$$
S_{ut} = \frac{A}{d^{\,m}}
$$

| Material | Uso | $A$ (MPa·mm$^m$) | $m$ |
|---|---|---|---|
| Arame de aço para molas (música) — ASTM A228 | Uso geral, alta resistência | 2211 | 0,145 |
| Arame temperado em óleo — ASTM A229 | Uso geral | 1855 | 0,187 |
| Cromo-vanádio — ASTM A232 | Choques, temperaturas moderadas | 2005 | 0,168 |
| Cromo-silício — ASTM A401 | Choques, fadiga | 1974 | 0,108 |

Fonte: tabela de Shigley. Limite de escoamento à torção para molas de compressão: $S_{sy} \approx 0{,}45\,S_{ut}$ (aços sem pré-assentamento). ⚠️ verificar na edição do livro adotada.

### Pontas e flambagem

- **Pontas esquadradas e retificadas**: melhor apoio, a mais comum em máquinas. Para esse tipo, $N_t = N_a + 2$.
- **Flambagem:** molas longas e esbeltas (comprimento livre muito maior que o diâmetro) podem flambar; usa-se guia (haste ou tubo) ou verifica-se pelo critério de estabilidade.

## Por que importa no projeto

- **Válvulas, embreagens, tensores de correias e correntes, amortecedores, dispositivos de segurança**.
- **Molas sob ciclos** (válvulas, peneiras vibratórias) falham por fadiga se a tensão alternada não for controlada.
- **Reposição:** uma mola "parecida" com fio levemente mais fino tem rigidez bem menor (quarta potência).

## Como aplicar (passo a passo / regras práticas)

1. **Requisitos:** forças e deflexões de trabalho, espaço disponível (diâmetro externo, comprimento), ciclos.
2. **Escolha um índice $C$** entre 6 e 10 e um material.
3. **Calcule $d$** pela tensão admissível; depois $D = C\,d$.
4. **Calcule $N_a$** pela rigidez necessária.
5. **Verifique:** tensão na altura sólida (mola totalmente comprimida) abaixo de $S_{sy}$; flambagem; fadiga, se houver ciclos.
6. **Especifique no desenho:** $d$, $D$ (ou diâmetro externo), comprimento livre, $N_t$, $N_a$, tipo de pontas, sentido da hélice, material, tratamento, e a tabela força × comprimento.

## Norma relacionada

- **EN 13906-1**: cálculo de molas helicoidais de compressão. ⚠️ verificar.
- **DIN 2095**: tolerâncias de molas de compressão de arame redondo.
- **ASTM A228, A229, A232, A401**: arames para molas.

## Exemplo prático

**Situação:** mola de compressão de arame temperado em óleo (A229), **d = 5 mm**, **D = 40 mm**, **8 espiras ativas**, carga de trabalho **500 N**.

- $C = 40/5 = 8$
- $K_W = \dfrac{4 \times 8 - 1}{4 \times 8 - 4} + \dfrac{0{,}615}{8} = \dfrac{31}{28} + 0{,}077 \approx 1{,}184$
- $\tau = 1{,}184 \times \dfrac{8 \times 500 \times 40}{\pi \times 5^3} \approx 482$ MPa
- $k = \dfrac{5^4 \times 79\,300}{8 \times 40^3 \times 8} \approx 12{,}1$ N/mm → deflexão de $500/12{,}1 \approx 41$ mm
- $S_{ut} = 1855/5^{0{,}187} \approx 1373$ MPa; $S_{sy} \approx 0{,}45 \times 1373 \approx 618$ MPa
- Coeficiente de segurança ao escoamento na carga de trabalho: $618/482 \approx 1{,}28$ (precisa ser verificado também na altura sólida).

> [!question] Exercício
>
> Na mola acima, o fio é trocado por um de 4,5 mm (mesmo D e Na). Qual a nova rigidez?
>
> > [!success]- Resolução
> >
> > A rigidez é proporcional a $d^4$: $k_{\text{novo}} = 12{,}1 \times (4{,}5/5)^4 = 12{,}1 \times 0{,}656 \approx 7{,}9$ N/mm. Uma redução de **35 %** por uma diferença de só 0,5 mm no fio.

## Erros comuns

- **Índice C muito baixo** (difícil de enrolar, tensões altas) ou muito alto (mola instável, enroscando).
- **Esquecer a verificação na altura sólida.**
- **Ignorar a flambagem** em molas longas.
- **Especificar só "mola de Ø40"** sem fio, espiras e comprimento livre.

## Ver também

- [[Correias e correntes]] (tensores)
- [[06-materiais/index|Materiais]]
- [[05-elementos-de-maquinas/index|Índice do módulo 05]]
