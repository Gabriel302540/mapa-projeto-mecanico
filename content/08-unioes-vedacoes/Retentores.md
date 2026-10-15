---
title: Retentores
tags: [vedacoes]
fontes: [ISO 6194-1 (retentores radiais — dimensões e tolerâncias), DIN 3760 e DIN 3761, catálogos técnicos de fabricantes de retentores (seções de projeto do eixo e do alojamento), Müller e Nau Fluid Sealing Technology]
status: rascunho
---

**Resumo:** retentores (vedações radiais de lábio) vedam eixos girantes em mancais, redutores e motores, mantendo o lubrificante dentro e a sujeira fora. Um lábio de elastômero, pressionado por uma mola, trabalha sobre o eixo com um filme de óleo microscópico. Sua vida depende muito mais do eixo — acabamento, dureza, batimento — e da montagem do que do próprio retentor.

## O que é

### Partes

- **Corpo** (metálico revestido de borracha ou exposto), que é montado com interferência no alojamento.
- **Lábio principal** de vedação, com **mola** helicoidal que mantém a pressão radial.
- **Lábio auxiliar** (guarda-pó), opcional, para ambientes sujos.

### Materiais do elastômero

| Material | Temperatura aproximada | Observações |
|---|---|---|
| **NBR** (nitrílica) | −40 a +100 °C | O mais comum; óleos minerais e graxas |
| **ACM** (poliacrílica) | até ≈ +150 °C | Óleos de transmissão; não tolera água |
| **FKM** (fluorelastômero) | até ≈ +200 °C | Temperaturas altas, óleos sintéticos, produtos químicos |
| **PTFE** | ampla | Velocidades e temperaturas altas, química agressiva; lábio sem mola em alguns modelos |

⚠️ verificar faixas no catálogo do fabricante.

### Requisitos do eixo (valores de referência)

| Requisito | Valor típico |
|---|---|
| Tolerância do diâmetro | h11 |
| Rugosidade | Ra 0,2 – 0,8 µm |
| Acabamento | **Retificado de mergulho** (sem marcas helicoidais) |
| Dureza | ≥ 45–55 HRC (maior para ambientes sujos e velocidades altas) |
| Chanfro de entrada | 15° a 30°, para não cortar o lábio |
| Batimento e excentricidade | Limitados conforme a rotação (catálogo) |

**Alojamento:** tolerância H8, Ra 1,6–3,2, chanfro de entrada.

⚠️ verificar todos os valores no catálogo do retentor escolhido. Ver [[Rugosidade pela função]].

### Velocidade periférica

$$
v = \frac{\pi\,d\,n}{60\,000}\ [\text{m/s}]
$$

Cada material e perfil tem uma velocidade máxima. A pressão admissível de retentores comuns é **baixa** (da ordem de 0,05 MPa); para pressões maiores, usam-se perfis especiais.

## Por que importa no projeto

- **Vazamentos de óleo** em redutores e mancais são, em grande parte, problemas de retentor — e quase sempre começam no eixo (riscado, gasto, com marcas helicoidais) ou na montagem (lábio virado, cortado).
- **Contaminação:** poeira, água e produto entrando nos mancais destroem rolamentos. Retentores com guarda-pó, labirintos externos e graxa como barreira protegem.
- **Projeto do eixo** precisa reservar a pista com acabamento e dureza próprios.

## Como aplicar (passo a passo / regras práticas)

1. **Escolha o retentor** pelo diâmetro, rotação, temperatura, lubrificante e ambiente.
2. **Projete a pista no eixo** com h11, Ra 0,2–0,8, retificação de mergulho, dureza adequada e chanfro.
3. **Projete o alojamento** com H8, chanfro e encosto (ou montagem rente à face).
4. **Lábio voltado para o fluido** a ser retido; guarda-pó voltado para fora.
5. **Preveja a troca:** espaço para extração; em eixos já gastos, use **luva de desgaste** ou desloque o retentor alguns milímetros (calço) para trabalhar numa pista nova.
6. **Monte com ferramenta** adequada (bucha de montagem), lubrificando o lábio.

## Norma relacionada

- **ISO 6194-1**: retentores radiais — dimensões e tolerâncias.
- **DIN 3760 / DIN 3761**: retentores (dimensões e requisitos). ⚠️ verificar.

## Exemplo prático

**Situação:** retentor de NBR num eixo de **Ø60** girando a **1500 rpm**.

- $v = \dfrac{\pi \times 60 \times 1500}{60\,000} \approx 4{,}7$ m/s — dentro da faixa usual de retentores de NBR (conferir no catálogo).
- Eixo: Ø60 h11 (59,810 a 60,000), Ra 0,4, retificado de mergulho, região temperada por indução ≥ 50 HRC, chanfro de 20°.
- Alojamento: H8, chanfro de entrada.

> [!question] Exercício
>
> Um redutor vaza óleo pelo retentor do eixo de saída logo após a troca do retentor. O eixo tem um sulco circunferencial na antiga pista. Qual a causa provável e duas soluções?
>
> > [!success]- Resolução
> >
> > **Causa:** o lábio novo está trabalhando sobre o **sulco gasto** pelo retentor anterior; a superfície não veda.
> > **Soluções:** (1) **luva de desgaste** fina prensada sobre a pista; (2) **deslocar o retentor** axialmente com um anel espaçador para uma região nova do eixo; (3) recuperar a pista (metalização ou cromo duro e retificação) ou substituir o eixo.

## Erros comuns

- **Eixo torneado** com marcas helicoidais na pista.
- **Montar sem chanfro** ou sem bucha, cortando o lábio na rosca ou no rasgo de chaveta.
- **Lábio invertido.**
- **Retentor comum em aplicação com pressão.**
- **Trocar o retentor sem corrigir a pista gasta.**

## Ver também

- [[O-rings]]
- [[Selos mecânicos]]
- [[Rugosidade pela função]]
- [[Montagem de rolamentos]]
- [[08-unioes-vedacoes/index|Índice do módulo 08]]
