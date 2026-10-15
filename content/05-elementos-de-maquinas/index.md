---
title: 05 · Elementos de máquinas
tags: [indice, elementos]
---

**Resumo:** Os componentes que transmitem força e movimento: eixos, mancais, engrenagens, chavetas, parafusos, molas e acoplamentos.

## Por que este módulo importa
É o núcleo do dia a dia de projeto de moenda: eixos dos rolos, mancais, acoplamentos e redutores da transmissão. Dimensionar e padronizar esses itens é onde mais se ganha em confiabilidade.

## Tópicos
Ordem sugerida de estudo: de cima para baixo.

- [x] [[Dimensionamento estático de eixos|Eixos: dimensionamento estático]]
- [x] [[Fadiga de eixos|Eixos: dimensionamento à fadiga]]
- [x] [[Concentradores de tensão]]
- [x] [[Chavetas]]
- [x] [[Eixos estriados]]
- [x] [[Seleção de rolamentos|Rolamentos: tipos e seleção]]
- [x] [[Vida de rolamentos|Rolamentos: vida nominal]]
- [x] [[Montagem de rolamentos|Rolamentos: montagem e fixação]]
- [x] [[Mancais de deslizamento|Mancais de deslizamento (buchas)]]
- [x] [[Geometria de engrenagens|Engrenagens cilíndricas: geometria]]
- [x] [[Dimensionamento de engrenagens|Engrenagens: dimensionamento]]
- [x] [[Redutores]]
- [x] [[Acoplamentos|Acoplamentos rígidos e elásticos]]
- [x] [[Parafusos|Parafusos: classes de resistência]]
- [x] [[Molas helicoidais]]
- [x] [[Correias e correntes]]
- [x] [[Fixação axial|Elementos de fixação axial]]

## Normas principais
Lista de partida, para conferir no documento original. Nenhum trecho de norma é reproduzido aqui.

- ISO 281 — rolamentos: capacidade de carga dinâmica e vida
- ISO 6336 (série) — capacidade de carga de engrenagens cilíndricas
- ISO 898-1 — propriedades mecânicas de parafusos
- DIN 743 — cálculo de resistência de eixos
- DIN 6885 — chavetas paralelas ⚠️ verificar norma equivalente ABNT/ISO em uso na empresa

## Módulos relacionados
- [[02-tolerancias-ajustes/index|02 · Tolerâncias e ajustes]]
- [[06-materiais/index|06 · Materiais]]
- [[08-unioes-vedacoes/index|08 · Uniões e vedações]]

## Revisão rápida

Tente responder antes de abrir a resposta.

> [!question] 1. Qual o torque num eixo que transmite 55 kW a 150 rpm?
>
> > [!success]- Resposta
> >
> > $T = 9550 \times 55/150 \approx 3502$ N·m. Ver [[Dimensionamento estático de eixos]].

> [!question] 2. Por que um eixo girante sob flexão precisa ser bem mais grosso do que indica o cálculo estático?
>
> > [!success]- Resposta
> >
> > Porque a flexão rotativa **alterna** a tensão a cada volta, causando **fadiga**. O limite de fadiga corrigido (com fatores de superfície, tamanho, confiabilidade e concentradores) é muito menor que o escoamento. Ver [[Fadiga de eixos]].

> [!question] 3. Cite três formas de reduzir a concentração de tensão num ressalto de eixo onde encosta um rolamento.
>
> > [!success]- Resposta
> >
> > Aumentar o **raio de concordância**; usar **canal de alívio** (raio maior rebaixado no ressalto); usar **anel espaçador** chanfrado; reforçar a superfície por **roletamento** ou **shot peening**. Ver [[Concentradores de tensão]].

> [!question] 4. Qual critério normalmente determina o comprimento de uma chaveta paralela, e qual a fórmula?
>
> > [!success]- Resposta
> >
> > A **pressão de contato (esmagamento)** nas faces laterais: $p = \dfrac{2T}{d\,(h - t_1)\,L} \le p_{\text{adm}}$. Ver [[Chavetas]].

> [!question] 5. Que tipo de rolamento escolher para um eixo longo, com carga radial alta, rotação baixa e estrutura sujeita a desalinhamento?
>
> > [!success]- Resposta
> >
> > **Autocompensador de rolos**, em arranjo **fixo-livre**, de preferência com bucha de fixação. Ver [[Seleção de rolamentos]].

> [!question] 6. Um rolamento de rolos tem C/P = 4 e gira a 100 rpm. Qual a vida L10 em horas?
>
> > [!success]- Resposta
> >
> > $L_{10} = 4^{10/3} \approx 101{,}6$ milhões de rotações. $L_{10h} = 101{,}6\times10^6/(60 \times 100) \approx 16\,900$ h. Ver [[Vida de rolamentos]].

> [!question] 7. Calcule p, v e pv de uma bucha de Ø80 × 80 mm com carga de 20 kN a 120 rpm.
>
> > [!success]- Resposta
> >
> > $p = 20\,000/(80 \times 80) \approx 3{,}1$ MPa; $v = \pi \times 80 \times 120/60\,000 \approx 0{,}50$ m/s; $pv \approx 1{,}57$ MPa·m/s. Ver [[Mancais de deslizamento]].

> [!question] 8. Um par de engrenagens tem m = 5, z1 = 18, z2 = 72. Calcule d1, d2, a distância entre centros e a relação.
>
> > [!success]- Resposta
> >
> > $d_1 = 90$ mm; $d_2 = 360$ mm; $a = 225$ mm; $i = 4$. Ver [[Geometria de engrenagens]].

> [!question] 9. O que significa a classe 10.9 de um parafuso?
>
> > [!success]- Resposta
> >
> > Resistência à tração nominal de **1000 MPa** (na tabela, 1040) e escoamento de **90 %** dela (≈ 900–940 MPa). Usa porca classe 10. Ver [[Parafusos]].

> [!question] 10. Por que um redutor de coroa e sem-fim pode ser limitado pela capacidade térmica antes da capacidade mecânica?
>
> > [!success]- Resposta
> >
> > Porque seu **rendimento é baixo** (50–90 %), e a potência perdida vira **calor** no óleo. Se a carcaça não dissipar esse calor, o óleo superaquece mesmo com as engrenagens dentro da capacidade mecânica. Ver [[Redutores]].

