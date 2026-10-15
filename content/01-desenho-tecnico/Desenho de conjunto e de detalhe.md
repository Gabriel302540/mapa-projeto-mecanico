---
title: Desenho de conjunto e de detalhe
tags: [desenho-tecnico, conjunto]
fontes: [ABNT NBR 13272 (elaboração de listas de itens) ⚠️ verificar, ISO 7573 (listas de peças), ISO 6433 (referências de itens), French e Vierck Desenho Técnico e Tecnologia Gráfica (cap. de desenhos de trabalho), Provenza Projetista de Máquinas (cap. de desenho de conjunto)]
status: rascunho
---

**Resumo:** um projeto mecânico é documentado em níveis: o desenho de conjunto mostra como as peças se montam e lista todas elas; os desenhos de detalhe definem cada peça fabricada, com todas as informações para produzi-la e inspecioná-la. Peças compradas (parafusos, rolamentos, retentores) não ganham desenho de detalhe: são especificadas na lista de peças.

## O que é

### Hierarquia dos desenhos

| Nível | O que mostra | Informação típica |
|---|---|---|
| **Arranjo geral (layout)** | O equipamento inteiro e sua relação com o entorno (bases, outros equipamentos, acessos) | Dimensões gerais, cotas de interface, pesos, pontos de fixação |
| **Conjunto (montagem)** | Como as peças se montam | Vistas e cortes do conjunto, balões numerados, **lista de peças**, cotas de montagem e ajustes |
| **Subconjunto** | Uma parte do conjunto que é montada separadamente (um mancal completo, uma tampa com retentor) | Igual ao conjunto, em escala menor |
| **Detalhe (fabricação)** | Uma única peça | **Todas** as cotas, tolerâncias, acabamentos, material, tratamento e notas |

### Elementos do desenho de conjunto

- **Balões (referências de itens):** círculos com o número do item, ligados à peça por uma linha de chamada que termina num ponto dentro da peça (ou numa seta no contorno). Os balões ficam alinhados em linhas ou colunas.
- **Lista de peças:** tabela com item, quantidade, denominação, material ou norma, código e observações. Normalmente fica **acima da legenda** e é numerada **de baixo para cima**.
- **Cotas de conjunto:** só as que importam para a montagem e a instalação (distâncias entre eixos, alturas de centro, dimensões máximas, furos de fixação) e os **ajustes** entre peças (por exemplo, Ø80 H7/k6 no assento do rolamento).
- **Cortes** que mostram o encaixe das peças, com hachuras diferentes para peças vizinhas. Ver [[Hachuras]].

### Elementos do desenho de detalhe

- Vistas e cortes **suficientes e necessários** para definir a peça.
- **Todas as cotas**, com tolerâncias dimensionais e geométricas onde forem necessárias.
- **Acabamento superficial** das superfícies funcionais.
- **Material, tratamento térmico e dureza**, na legenda.
- **Notas gerais:** tolerâncias gerais, cantos vivos, proteção superficial.
- **Referência ao conjunto** (número do desenho de conjunto e número do item).

### Peças padronizadas (compradas)

Parafusos, porcas, arruelas, rolamentos, retentores, anéis elásticos, chavetas normalizadas e acoplamentos de catálogo **não recebem desenho de detalhe**. Na lista de peças, eles são especificados pela norma e pela designação completa: "Parafuso sextavado ISO 4017 M16 × 60 - 8.8 - zincado", "Rolamento 22220 E", "Retentor 80 × 100 × 10".

## Por que importa no projeto

- **Separação de responsabilidades:** a oficina usa o detalhe para fabricar; a montagem usa o conjunto para montar; o almoxarifado usa a lista para comprar.
- **Rastreabilidade:** cada item da lista aponta para um desenho de detalhe ou para uma especificação de compra.
- **Padronização:** quanto mais itens forem peças de catálogo e menos forem peças especiais, mais barato e rápido é manter o equipamento. Ver [[09-metodologia-de-projeto/index|Metodologia de projeto]].

## Como aplicar (passo a passo / regras práticas)

1. **Monte a árvore do produto:** conjunto → subconjuntos → peças. Cada nó recebe um número de desenho.
2. **No conjunto:** escolha vistas e cortes que mostrem **todas** as peças pelo menos uma vez; numere com balões em ordem lógica (de dentro para fora, ou na ordem de montagem).
3. **Lista de peças:** um item por peça diferente; peças iguais têm o mesmo item com a quantidade total.
4. **Cote no conjunto só o que é de montagem** (ajustes, folgas, distâncias de instalação). As cotas de fabricação ficam nos detalhes.
5. **No detalhe:** confira se todas as cotas necessárias para fabricar estão lá, sem depender de nenhum outro desenho.
6. **Peças compradas:** especifique pela norma e designação; não desenhe.
7. **Revisões:** se uma peça mudar, revise o detalhe e verifique se o conjunto e a lista também precisam mudar. Ver [[Legenda]].

## Norma relacionada

- **ISO 7573**: listas de peças. ⚠️ verificar a norma ABNT equivalente vigente (a NBR 13272, de elaboração de lista de itens, é citada em materiais didáticos).
- **ISO 6433**: referências de itens (balões).
- **ISO 4017, ISO 4014, ISO 281** etc.: normas das peças padronizadas citadas na lista.

## Exemplo prático

**Situação:** documentar o **mancal de um eixo de transmissão** com rolamento autocompensador de rolos montado em bucha de fixação, caixa bipartida e vedação por labirinto.

| Item | Qtd | Denominação | Especificação | Tipo |
|---|---|---|---|---|
| 1 | 1 | Caixa de mancal bipartida | Desenho de detalhe DES-001 | Fabricada (ou de catálogo) |
| 2 | 1 | Rolamento autocompensador de rolos | 22220 EK | Comprada |
| 3 | 1 | Bucha de fixação | H 320 | Comprada |
| 4 | 2 | Anel de vedação labirinto | Desenho DES-002 | Fabricada |
| 5 | 4 | Parafuso sextavado | ISO 4017 M20 × 80 - 8.8 | Comprada |
| 6 | 4 | Arruela lisa | ISO 7089 - 20 - 200 HV | Comprada |

No conjunto: corte longitudinal mostrando eixo, bucha, rolamento e vedações; cota de altura de centro; cotas dos furos de fixação; ajuste do alojamento (por exemplo, Ø180 H7). Os itens 1 e 4 ganham desenhos de detalhe; os outros só aparecem na lista. As designações são ilustrativas; ⚠️ verificar no catálogo do fabricante.

> [!question] Exercício
>
> Num desenho de conjunto, a montagem tem 6 parafusos M12 × 40 iguais, 2 tampas iguais e 1 eixo. Quantos itens a lista de peças deve ter e quais quantidades?
>
> > [!success]- Resolução
> >
> > **Três itens:** eixo (qtd 1), tampa (qtd 2) e parafuso M12 × 40 com a especificação completa (qtd 6). Peças iguais compartilham o mesmo número de item; a quantidade total vai na coluna "Qtd". Cada peça diferente, mesmo que pequena, é um item.

## Erros comuns

- **Desenho de detalhe que depende do conjunto** para ter alguma cota ("ver conjunto").
- **Peças compradas desenhadas e cotadas** como se fossem fabricadas.
- **Especificação incompleta** de parafusos (sem classe de resistência) e rolamentos (sem sufixos de folga ou vedação).
- **Balões cruzando linhas** ou espalhados sem alinhamento.
- **Lista de peças numerada de cima para baixo**, que não cresce sem redesenhar.

## Ver também

- [[Legenda]]
- [[Cortes e seções]]
- [[Perspectivas]] (vista explodida)
- [[09-metodologia-de-projeto/index|Metodologia de projeto]]
- [[01-desenho-tecnico/index|Índice do módulo 01]]
