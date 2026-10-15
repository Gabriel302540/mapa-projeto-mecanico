---
title: Lista de materiais
tags: [metodologia, documentacao]
fontes: [ISO 7573 (listas de peças) ⚠️ verificar, ISO 10209 (vocabulário de documentação técnica de produto), Pahl, Beitz, Feldhusen e Grote Projeto na Engenharia (cap. de estrutura do produto e listas de peças), APICS Dictionary (definições de BOM)]
status: rascunho
---

**Resumo:** a lista de materiais (BOM, *bill of materials*) relaciona todos os itens necessários para fabricar e montar um conjunto: peças fabricadas, peças compradas, materiais brutos e consumíveis, com quantidades e especificações. É a ponte entre o projeto, as compras, o almoxarifado e a fabricação.

## O que é

### Estrutura

- **Lista de peças do desenho:** a tabela no desenho de conjunto (ver [[Desenho de conjunto e de detalhe]]).
- **BOM estruturada (multinível):** árvore com níveis — produto → conjuntos → subconjuntos → peças → matérias-primas. Cada nível aponta para o seu desenho.
- **BOM de engenharia × BOM de fabricação:** a de engenharia segue a lógica do projeto; a de fabricação reorganiza conforme a sequência de produção e inclui materiais de processo (eletrodos, tintas, gabaritos).

### Campos típicos

| Campo | Exemplo |
|---|---|
| Item | 5 |
| Quantidade | 4 |
| Unidade | pç, kg, m, m² |
| Denominação | Parafuso sextavado |
| Especificação / norma | ISO 4017 M20 × 80 – 8.8 – zincado |
| Material | — (comprado) / ASTM A36 |
| Dimensões brutas | Chapa # 12,5 × 300 × 450 |
| Número do desenho | DES-0125 (se fabricado) |
| Código interno | Código do almoxarifado |
| Massa unitária e total | 0,3 kg / 1,2 kg |
| Observações | Sobressalente crítico; fornecedor preferencial |

### Material bruto

Para peças fabricadas, a lista indica a **dimensão bruta** de compra (barra Ø100 × 420 mm; chapa # 12,5 × 300 × 450), já com **sobremetal** para usinagem e perdas de corte. Isso permite comprar e reservar material antes da fabricação.

## Por que importa no projeto

- **Compras e prazos:** itens de prazo longo (redutores, rolamentos grandes, fundidos) são identificados cedo.
- **Custo e peso:** a soma das massas permite estimar custo de material, frete e içamento.
- **Manutenção:** a BOM do equipamento instalado é a base da lista de sobressalentes.
- **Erros de lista** (quantidade errada, especificação incompleta) param a montagem tanto quanto um erro de desenho.

## Como aplicar (passo a passo / regras práticas)

1. **Monte a árvore do produto** antes de detalhar.
2. **Cada peça diferente = um item**; peças iguais compartilham o item com a quantidade total.
3. **Especificação completa** para itens comprados (norma, dimensão, classe, acabamento, sufixos).
4. **Dimensões brutas** e material para itens fabricados.
5. **Extraia a BOM do CAD 3D** quando possível, para reduzir erros de digitação, mas **confira** (itens de catálogo mal configurados geram linhas erradas).
6. **Revise junto com os desenhos** (mesma revisão).

## Norma relacionada

- **ISO 7573**: listas de peças em documentação técnica. ⚠️ verificar se ainda vigente ou substituída.
- **Padrões internos** de codificação de materiais da empresa.

## Exemplo prático

**Situação:** BOM resumida de um **mancal de transportador** (subconjunto).

| Item | Qtd | Un | Denominação | Especificação | Desenho / código |
|---|---|---|---|---|---|
| 1 | 1 | pç | Caixa de mancal bipartida | Ferro fundido nodular, conforme desenho | DES-0201 |
| 2 | 1 | pç | Rolamento autocompensador de rolos | Furo cônico, folga C3 | Código de catálogo ⚠️ |
| 3 | 1 | pç | Bucha de fixação | Conforme rolamento | Código de catálogo |
| 4 | 2 | pç | Vedação labirinto | SAE 1020, conforme desenho; bruto: barra Ø200 × 40 | DES-0202 |
| 5 | 4 | pç | Parafuso sextavado | ISO 4017 M20 × 80 – 8.8 – zincado | — |
| 6 | 4 | pç | Porca sextavada | ISO 4032 M20 – 8 – zincada | — |
| 7 | 0,2 | kg | Graxa | Graxa para rolamentos conforme especificação de lubrificação | — |

> [!question] Exercício
>
> Por que a lista de materiais deve indicar a dimensão bruta das peças fabricadas, e não só a dimensão final?
>
> > [!success]- Resolução
> >
> > Porque compras e almoxarifado precisam saber **o que comprar ou separar**: a barra ou a chapa com **sobremetal** para usinagem, perdas de corte e eventuais corpos de prova. A dimensão final não diz qual bitola comercial usar nem quanto material reservar.

## Erros comuns

- **Especificação incompleta** de componentes comprados.
- **Quantidades erradas** (esquecer que há 2 mancais por eixo, 2 eixos por equipamento...).
- **BOM e desenho em revisões diferentes.**
- **Esquecer consumíveis** necessários à montagem (graxa, vedantes, calços).

## Ver também

- [[Desenho de conjunto e de detalhe]]
- [[Padronização de componentes]]
- [[Controle de desenhos]]
- [[09-metodologia-de-projeto/index|Índice do módulo 09]]
