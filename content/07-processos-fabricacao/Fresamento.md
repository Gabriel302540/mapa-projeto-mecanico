---
title: Fresamento
tags: [fabricacao, usinagem]
fontes: [Diniz, Marcondes e Coppini Tecnologia da Usinagem dos Materiais (cap. de fresamento), Ferraresi Fundamentos da Usinagem dos Metais, Kalpakjian e Schmid Manufacturing Engineering and Technology (cap. de fresamento), catálogos técnicos de ferramentas de fresamento]
status: rascunho
---

**Resumo:** no fresamento, a ferramenta (fresa) gira com vários gumes e a peça avança contra ela, gerando superfícies planas, rasgos, cavidades, perfis e, com máquinas CNC, formas complexas. É o processo típico para faces de apoio, rasgos de chaveta, alojamentos e peças prismáticas.

## O que é

### Tipos e operações

| Tipo | Como é | Uso |
|---|---|---|
| **Fresamento frontal (de topo)** | O eixo da fresa é perpendicular à superfície; corta com a face | Faces planas grandes (bases, flanges) |
| **Fresamento periférico (tangencial)** | O eixo da fresa é paralelo à superfície; corta com a periferia | Rasgos, degraus, perfis |
| **Fresa de topo (*end mill*)** | Corta com a ponta e a lateral | Rasgos de chaveta, bolsões, contornos |
| **Fresa de disco** | Disco com dentes na periferia | Rasgos de chaveta "em trenó", canais |

**Concordante × discordante:** no **concordante**, a fresa gira no mesmo sentido do avanço (o cavaco começa grosso): melhor acabamento e vida da ferramenta, exige máquina sem folga (CNC). No **discordante**, sentido contrário: preferido em máquinas convencionais com folga no fuso.

### Parâmetros

| Parâmetro | Relação |
|---|---|
| Rotação | $n = \dfrac{1000\,v_c}{\pi\,D}$ |
| Avanço por dente | $f_z$ (mm/dente) |
| Velocidade de avanço | $v_f = f_z\,z\,n$ (mm/min) |
| Taxa de remoção | $Q = \dfrac{a_p\,a_e\,v_f}{1000}$ (cm³/min) |

onde $z$ é o número de dentes, $a_p$ a profundidade axial e $a_e$ a largura radial de corte.

### Mandriladoras e centros de usinagem

**Mandriladoras horizontais** e **centros de usinagem** combinam fresamento, furação e mandrilamento numa mesma fixação. São essenciais para carcaças de redutores e mancais, onde os furos dos rolamentos precisam ser paralelos e alinhados (ver [[Tolerâncias de orientação]]).

## Por que importa no projeto

- **Faces de apoio de bases e carcaças** são fresadas; o projeto define a área a usinar (com sobremetal) e a planeza.
- **Raios internos** de bolsões e rasgos dependem do raio da fresa: um canto interno vivo é impossível de fresar.
- **Peças prismáticas grandes** exigem máquinas com curso suficiente; o projetista deve conhecer a capacidade da oficina.

## Como aplicar (passo a passo / regras práticas)

1. **Cantos internos com raio** compatível com fresas comuns (R3, R5, R6, R8, R10...), e profundidade de bolsões limitada a cerca de 3–4 vezes o diâmetro da fresa.
2. **Faces a usinar elevadas** (ressaltos de usinagem) em peças soldadas e fundidas, para não usinar a peça inteira.
3. **Agrupe as usinagens** que precisam de alinhamento na mesma fixação.
4. **Rasgos de chaveta:** indique o tipo de fresa se o fim do rasgo importar (fresa de topo → fim reto; fresa de disco → saída curva). Ver [[Concentradores de tensão]].

## Norma relacionada

- **Catálogos de ferramentas**: dados de corte.
- **ISO 1832**: designação de insertos.

## Exemplo prático

**Situação:** fresar a face de apoio de uma base de aço A36 com cabeçote de **Ø80**, **6 insertos**, $v_c$ = 200 m/min, $f_z$ = 0,15 mm/dente.

- $n = \dfrac{1000 \times 200}{\pi \times 80} \approx 796$ rpm
- $v_f = 0{,}15 \times 6 \times 796 \approx 716$ mm/min
- Com $a_p$ = 2 mm e $a_e$ = 60 mm: $Q = 2 \times 60 \times 716/1000 \approx 86$ cm³/min

> [!question] Exercício
>
> Por que um bolsão retangular fresado não pode ter os cantos internos vivos? Como o projeto deve tratar isso?
>
> > [!success]- Resolução
> >
> > Porque a fresa é **cilíndrica**: o menor raio que ela deixa no canto interno é o seu próprio raio. Cantos vivos só por eletroerosão ou outros processos caros. O projeto deve **indicar um raio** nos cantos internos compatível com fresas padrão (por exemplo, R6 para uma fresa de Ø12) ou, se a peça encaixada exigir canto vivo, prever **alívios** (furos ou rebaixos nos cantos).

## Erros comuns

- **Cantos internos vivos** em bolsões.
- **Faces de apoio sem sobremetal** em peças soldadas.
- **Furos de alinhamento usinados em fixações diferentes.**
- **Profundidades excessivas** para fresas de pequeno diâmetro.

## Ver também

- [[Torneamento]]
- [[Furação e mandrilamento]]
- [[Projeto para fabricação]]
- [[07-processos-fabricacao/index|Índice do módulo 07]]
