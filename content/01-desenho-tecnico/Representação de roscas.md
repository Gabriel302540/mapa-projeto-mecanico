---
title: Representação de roscas
tags: [desenho-tecnico, roscas]
fontes: [ISO 6410-1, ABNT NBR 8993 (cancelada 2015, histórica), ISO 261 e ISO 965-1 (roscas métricas), French e Vierck Desenho Técnico e Tecnologia Gráfica (cap. de roscas e fixadores), Telecurso 2000 Leitura e Interpretação de Desenho Técnico Mecânico]
status: rascunho
---

**Resumo:** roscas não são desenhadas com todos os filetes. Usa-se uma representação convencional simples: linha larga na crista, linha estreita no fundo, e, na vista de topo, um arco de cerca de 3/4 de círculo para o fundo. O tipo exato de rosca é informado pela designação escrita (M20 × 1,5 - 6g).

## O que é

### Vocabulário

- **Crista:** a "ponta" do filete. Na rosca externa (parafuso), está no diâmetro maior; na interna (porca, furo roscado), no diâmetro menor.
- **Fundo (raiz):** o "vale" entre filetes. Na rosca externa, está no diâmetro menor; na interna, no diâmetro maior.
- **Diâmetro nominal ($d$):** o diâmetro maior, que dá nome à rosca (M20 → 20 mm).
- **Passo ($P$):** distância entre dois filetes consecutivos.
- **Rosca útil:** trecho com filetes completos.

### Representação convencional

| Elemento | Vista longitudinal | Vista de topo (circular) |
|---|---|---|
| **Crista** | Linha contínua **larga** | Círculo completo em contínua larga |
| **Fundo** | Linha contínua **estreita** | Arco em contínua estreita de **cerca de 3/4 de circunferência** |
| **Fim da rosca útil** | Linha contínua larga transversal | — |
| **Chanfro de entrada** | Desenhado normalmente na vista longitudinal | Não é desenhado na vista de topo |

**Rosca externa:** a linha larga fica por fora (diâmetro nominal) e a estreita por dentro.
**Rosca interna (furo roscado):** a linha larga fica por dentro (diâmetro do furo de broca) e a estreita por fora (diâmetro nominal).

**Em corte**, a hachura vai **até a linha larga** (a crista), atravessando a linha estreita. Isso vale para roscas externas e internas.

**Roscas ocultas** (vistas sem corte) são desenhadas com tracejadas para crista e fundo.

### Furo roscado cego

- O furo de broca é mais profundo que a rosca útil, para dar espaço à saída do macho.
- A ponta do furo é desenhada como um **cone de 120°** (aproximação do ângulo de 118° da broca).

### Conjunto parafusado

Quando um parafuso está aparafusado num furo roscado, **a rosca externa (do parafuso) prevalece** e cobre a interna no trecho em que estão engrenadas. O parafuso **não é hachurado** no corte longitudinal (ver [[Cortes e seções]]).

### Designação (o que é escrito)

| Designação | Significado |
|---|---|
| M20 | Métrica, Ø20, passo grosso (2,5 mm) |
| M20 × 1,5 | Métrica, Ø20, passo fino de 1,5 mm |
| M20 × 1,5 - 6g | Rosca externa, classe de tolerância 6g |
| M20 - 6H | Rosca interna, classe 6H |
| M20 - LH | Rosca esquerda |
| G 1/2 | Rosca de tubo cilíndrica (Whitworth para tubos, ISO 228) |
| R 1/2 / Rp 1/2 | Rosca de tubo cônica / interna cilíndrica para vedação na rosca (ISO 7-1) |
| 1/2" NPT | Rosca de tubo cônica americana |
| Tr 40 × 7 | Rosca trapezoidal, Ø40, passo 7 (fusos de movimento) |

## Por que importa no projeto

- **Desenhar todos os filetes** seria lento e não acrescentaria nada: o tipo de rosca já está definido pela designação.
- **Trocar crista e fundo** (larga e estreita) faz o leitor confundir rosca interna com externa.
- **Roscas de tubo** (G, R, NPT) parecem iguais no desenho, mas não são intercambiáveis. A designação correta evita vazamentos em linhas de óleo, água e vapor.

## Como aplicar (passo a passo / regras práticas)

1. Desenhe o diâmetro da **crista** em linha larga e o do **fundo** em linha estreita. Na rosca métrica, o fundo da rosca externa fica em aproximadamente $d - 1{,}2P$ (aproximação suficiente para o desenho).
2. Na vista de topo, desenhe o **arco de 3/4** do fundo, com a abertura em qualquer quadrante (normalmente o superior direito).
3. Marque o **fim da rosca útil** com linha larga transversal.
4. Em corte, leve a hachura até a crista.
5. Escreva a **designação completa** com linha de chamada e cote o comprimento de rosca útil.
6. Em furos cegos, cote o furo de broca (diâmetro e profundidade). Ver [[Cotagem de elementos]].

## Norma relacionada

- **ISO 6410-1**: representação convencional de roscas e peças roscadas. Revisada e confirmada em 2024. A parte 3 (representação simplificada) consta como retirada. ⚠️ verificar.
- **ABNT NBR 8993**: equivalente brasileira, **cancelada sem substituição em 2015**; as regras continuam sendo as da ISO 6410.
- **ISO 261** (rosca métrica: plano geral) e **ISO 965-1** (tolerâncias de roscas métricas).
- **ISO 228-1** (roscas de tubo para uniões sem vedação na rosca, "G") e **ISO 7-1** (roscas de tubo com vedação na rosca, "R/Rp").

## Exemplo prático

**Situação:** o furo de dreno de óleo no fundo da carcaça de um redutor, com bujão roscado.

- Rosca de tubo **G 1/2** (cilíndrica), com vedação por arruela de cobre ou anel, e não pela rosca.
- No corte da carcaça: linha estreita no diâmetro externo da rosca, linha larga no diâmetro do furo, hachura até a linha larga, fim da rosca marcado em linha larga.
- Designação: **"G 1/2"** com linha de chamada; profundidade de rosca útil cotada.
- Se o projeto usasse **R 1/2** (cônica), a vedação seria feita na própria rosca, com fita ou vedante. Trocar uma pela outra na compra do bujão causa vazamento.

> [!question] Exercício
>
> Numa vista longitudinal sem corte de um eixo com a ponta roscada M24, qual linha representa o diâmetro de 24 mm, e qual representa o diâmetro de fundo? E se fosse um furo roscado M24 numa peça cortada?
>
> > [!success]- Resolução
> >
> > - **Eixo (rosca externa):** Ø24 (crista) em **linha contínua larga**; fundo (≈ $24 - 1{,}2 \times 3 = 20{,}4$ mm, passo grosso de 3 mm) em **linha contínua estreita**.
> > - **Furo roscado (rosca interna) em corte:** o diâmetro do furo de broca (crista da rosca interna, ≈ 21 mm) em **linha larga**; o Ø24 (fundo da rosca interna) em **linha estreita**; a hachura vai até a linha larga.

## Erros comuns

- **Inverter larga e estreita** entre rosca interna e externa.
- **Hachura parando na linha estreita** em vez de ir até a crista.
- **Desenhar o círculo completo do fundo** na vista de topo (o arco é de 3/4).
- **Designação incompleta** (só "M20" quando o passo é fino).
- **Confundir G, R e NPT** em roscas de tubo.

## Ver também

- [[Cotagem de elementos]]
- [[Cortes e seções]]
- [[Tipos de linha]]
- [[08-unioes-vedacoes/index|Uniões e vedações]]
- [[01-desenho-tecnico/index|Índice do módulo 01]]
