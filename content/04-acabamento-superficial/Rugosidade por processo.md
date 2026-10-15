---
title: Rugosidade obtida por processo de fabricação
tags: [acabamento, processos]
fontes: [ISO 21920-1:2021 (anexo informativo de valores típicos) ⚠️ verificar, Kalpakjian e Schmid Manufacturing Engineering and Technology (cap. de acabamento superficial), Machinery's Handbook (tabela de rugosidade por processo), Diniz, Marcondes e Coppini Tecnologia da Usinagem dos Materiais (cap. de acabamento)]
status: rascunho
---

**Resumo:** cada processo de fabricação tem uma faixa típica de rugosidade. Escolher um Ra no desenho é, na prática, escolher o processo final e, portanto, o custo. Esta nota traz a tabela de referência e a fórmula que liga o avanço e o raio da ferramenta à rugosidade no torneamento.

## O que é

### Faixas típicas de Ra por processo (µm)

| Processo | Faixa comum | Faixa possível com cuidado especial |
|---|---|---|
| Oxicorte | 12,5 – 50 | 6,3 |
| Corte a plasma | 6,3 – 25 | 3,2 |
| Corte a laser (chapas finas e médias) | 1,6 – 6,3 | 0,8 |
| Serra | 6,3 – 25 | 3,2 |
| Fundição em areia | 12,5 – 50 | 6,3 |
| Forjamento a quente | 3,2 – 12,5 | 1,6 |
| Laminação a quente | 12,5 – 25 | 6,3 |
| Torneamento de desbaste | 6,3 – 25 | — |
| Torneamento de acabamento | 0,8 – 3,2 | 0,4 |
| Fresamento | 1,6 – 6,3 | 0,8 |
| Furação | 3,2 – 12,5 | 1,6 |
| Alargamento | 0,8 – 3,2 | 0,4 |
| Mandrilamento | 0,8 – 3,2 | 0,4 |
| Brochamento | 0,8 – 3,2 | 0,4 |
| Retificação | 0,2 – 1,6 | 0,05 |
| Brunimento | 0,05 – 0,4 | 0,025 |
| Lapidação | 0,025 – 0,2 | 0,012 |
| Polimento | 0,05 – 0,4 | 0,025 |

Valores aproximados, compilados de tabelas de manuais de fabricação; dependem da máquina, ferramenta, material e parâmetros de corte. ⚠️ verificar com a capacidade real da oficina.

### Rugosidade teórica no torneamento

No torneamento com ferramenta de raio de ponta $r$ e avanço $f$ por volta, as marcas deixadas são arcos de círculo repetidos. A geometria dá:

$$
R_t \approx \frac{f^2}{8\,r} \qquad\qquad Ra \approx \frac{f^2}{32\,r} \approx 0{,}032\,\frac{f^2}{r}
$$

(com $f$ e $r$ em mm, o resultado sai em mm). É a rugosidade **mínima teórica**: vibração, desgaste da ferramenta, aresta postiça e o material aumentam o valor real.

**Consequências práticas:**

- A rugosidade cresce com o **quadrado do avanço**: dobrar o avanço quadruplica o Ra.
- Um **raio de ponta maior** melhora o acabamento, mas aumenta a força de corte radial e a tendência à vibração.

## Por que importa no projeto

- **Custo cresce rápido** abaixo de Ra 1,6 (retificação) e muito rápido abaixo de Ra 0,4 (brunimento, lapidação).
- **Peças grandes** (eixos longos, rolos, carcaças) nem sempre cabem numa retificadora disponível; especificar Ra 0,4 num eixo de 4 m pode obrigar a terceirizar o serviço.
- **Processo e tolerância andam juntos:** Ra 3,2 e IT7 dificilmente convivem; Ra 0,8 é coerente com IT6. Ver [[Graus IT]].

## Como aplicar (passo a passo / regras práticas)

1. **Parta da função** e determine o Ra máximo admissível. Ver [[Rugosidade pela função]].
2. **Escolha o processo mais barato** cuja faixa comum atenda a esse Ra.
3. **Evite especificar no limite** da faixa "com cuidado especial" sem consultar a oficina.
4. **Para torneamento**, use a fórmula para escolher avanço e raio de ponta.

## Norma relacionada

- **ISO 21920-1:2021**: indicação no desenho (o processo pode ser escrito junto ao símbolo).
- As faixas por processo vêm de **manuais e literatura técnica**, não de norma obrigatória.

## Exemplo prático

**Situação:** um assento de rolamento deve ter **Ra 1,6** e vai ser feito em torneamento de acabamento com inserto de raio 0,8 mm. Qual o avanço máximo?

$$
f = \sqrt{\frac{Ra \cdot r}{0{,}032}} = \sqrt{\frac{0{,}0016 \times 0{,}8}{0{,}032}} = \sqrt{0{,}04} = 0{,}2\ \text{mm/volta}
$$

Como o valor real costuma ser maior que o teórico, o torneiro usaria algo como **0,10 a 0,15 mm/volta**, com margem. Se a especificação fosse Ra 0,4, o avanço teórico cairia para 0,1 mm/volta, e na prática seria melhor **retificar**.

> [!question] Exercício
>
> Torneando com raio de ponta de 1,2 mm e avanço de 0,25 mm/volta, qual a rugosidade teórica Rt e Ra?
>
> > [!success]- Resolução
> >
> > $R_t = \dfrac{0{,}25^2}{8 \times 1{,}2} = \dfrac{0{,}0625}{9{,}6} \approx 0{,}0065$ mm ≈ **6,5 µm**.
> > $Ra \approx 0{,}032 \times \dfrac{0{,}0625}{1{,}2} \approx 0{,}0017$ mm ≈ **1,7 µm**.
> > Na prática, o Ra medido seria um pouco maior; atende Ra 3,2 com folga, mas não garante Ra 1,6.

## Erros comuns

- **Especificar Ra por hábito** (Ra 0,8 em tudo), sem olhar o custo do processo.
- **Achar que a fórmula dá o valor real** (ela dá o mínimo teórico).
- **Pedir retificação** em superfícies que um bom torneamento atenderia.
- **Ignorar o tamanho da peça** na escolha do processo.

## Ver também

- [[Rugosidade pela função]]
- [[Parâmetros de rugosidade]]
- [[07-processos-fabricacao/index|Processos de fabricação]]
- [[04-acabamento-superficial/index|Índice do módulo 04]]
