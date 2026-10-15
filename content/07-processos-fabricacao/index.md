---
title: 07 · Processos de fabricação
tags: [indice, fabricacao]
---

**Resumo:** Como a peça é feita: usinagem, soldagem, caldeiraria, corte e dobra, e o que isso muda no desenho.

## Por que este módulo importa
Projetar sem pensar na fabricação gera peças caras ou impossíveis. Saber o que a oficina e a caldeiraria conseguem fazer evita retrabalho e define tolerâncias realistas.

## Tópicos
Ordem sugerida de estudo: de cima para baixo.

- [x] [[Torneamento]]
- [x] [[Fresamento]]
- [x] [[Furação e mandrilamento]]
- [x] [[Tolerâncias por processo|Tolerâncias alcançáveis por processo]]
- [x] [[Processos de soldagem]]
- [x] [[Simbologia de soldagem]]
- [x] [[Juntas e chanfros]]
- [x] [[Caldeiraria|Caldeiraria: traçagem e planificação]]
- [x] [[Dobra de chapas]]
- [x] [[Corte térmico|Corte térmico (oxicorte, plasma, laser)]]
- [x] [[Projeto para fabricação]]

## Normas principais
Lista de partida, para conferir no documento original. Nenhum trecho de norma é reproduzido aqui.

- AWS A2.4 — símbolos de soldagem e ensaios não destrutivos
- ISO 2553 — representação simbólica de soldas
- AWS D1.1 — soldagem de estruturas de aço

## Módulos relacionados
- [[06-materiais/index|06 · Materiais]]
- [[08-unioes-vedacoes/index|08 · Uniões e vedações]]
- [[04-acabamento-superficial/index|04 · Acabamento superficial]]

## Revisão rápida

Tente responder antes de abrir a resposta.

> [!question] 1. Qual a rotação para tornear um Ø80 com velocidade de corte de 200 m/min?
>
> > [!success]- Resposta
> >
> > $n = 1000 \times 200/(\pi \times 80) \approx 796$ rpm. Ver [[Torneamento]].

> [!question] 2. Por que os diâmetros de um eixo que precisam girar concêntricos devem ser usinados entre pontas ou na mesma fixação?
>
> > [!success]- Resposta
> >
> > Porque cada nova fixação introduz um erro de centragem. Usinando todos os diâmetros com a **mesma referência** (os furos de centro), a concentricidade (batimento) entre eles fica garantida. Ver [[Torneamento]].

> [!question] 3. Qual a sequência de operações para obter um furo Ø16 H7?
>
> > [!success]- Resposta
> >
> > Furo de centro → broca (≈ Ø15,7) → **alargador Ø16 H7** (ou mandrilamento). Furação sozinha dá só IT11–IT13. Ver [[Furação e mandrilamento]].

> [!question] 4. Por que especificar IT6 com Ra 3,2 é incoerente?
>
> > [!success]- Resposta
> >
> > Porque IT6 exige **torneamento fino ou retificação**, e Ra 3,2 corresponde a torneamento comum, cuja rugosidade (Rz) pode consumir quase toda a tolerância. Grau IT e Ra devem ser compatíveis. Ver [[Tolerâncias por processo]].

> [!question] 5. Qual processo de soldagem é mais indicado para manutenção em campo, com vento e em várias posições? Por quê?
>
> > [!success]- Resposta
> >
> > **Eletrodo revestido (SMAW)** ou **arame tubular autoprotegido**: a proteção vem da escória e dos gases do próprio consumível, que o vento não dispersa como o gás do MIG/MAG; o equipamento é simples e portátil. Ver [[Processos de soldagem]].

> [!question] 6. No sistema AWS, o que significa um símbolo de solda desenhado abaixo da linha de referência? E no ISO 2553?
>
> > [!success]- Resposta
> >
> > **AWS:** abaixo da linha = **lado da seta**. **ISO 2553 (sistema A):** símbolo na **linha contínua** = lado da seta; na **linha tracejada** = outro lado. Ver [[Simbologia de soldagem]].

> [!question] 7. Qual a garganta de um filete com perna de 10 mm? E por que o chanfro em X é preferível ao V em chapas grossas?
>
> > [!success]- Resposta
> >
> > $a = 0{,}707 \times 10 \approx 7{,}1$ mm. O chanfro em **X** deposita **cerca de metade** do metal do V e **equilibra a distorção** (solda dos dois lados). Ver [[Juntas e chanfros]].

> [!question] 8. Qual o comprimento de chapa para uma virola de Ø1200 externo em chapa de 16 mm?
>
> > [!success]- Resposta
> >
> > $L = \pi\,(1200 - 16) = \pi \times 1184 \approx 3719{,}6$ mm (pelo diâmetro médio). Ver [[Caldeiraria]].

> [!question] 9. Calcule o comprimento da zona dobrada (BA) para uma dobra de 90° com raio interno de 10 mm, chapa de 8 mm e K = 0,4.
>
> > [!success]- Resposta
> >
> > $BA = \dfrac{\pi}{180} \times 90 \times (10 + 0{,}4 \times 8) = \dfrac{\pi}{2} \times 13{,}2 \approx 20{,}7$ mm. Ver [[Dobra de chapas]].

> [!question] 10. Por que um furo de Ø18 numa chapa de 25 mm não deve ser feito a plasma, e qual a alternativa?
>
> > [!success]- Resposta
> >
> > Porque o diâmetro é **menor que a espessura**: o plasma deixa o furo cônico e irregular. Alternativas: **furar** (furadeira ou fresadora) após o corte, ou usar **laser** de alta potência se disponível. Ver [[Corte térmico]].

