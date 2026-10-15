---
title: Model e layout (paper space)
tags: [cad, autocad]
fontes: [Autodesk AutoCAD — documentação oficial (espaço do modelo, espaço do papel, viewports de layout), ABNT NBR 16752 (folhas de desenho)]
status: rascunho
---

**Resumo:** no AutoCAD, a geometria é desenhada em tamanho real (1:1) no espaço do modelo (Model). A folha de desenho — formato, legenda, notas — é montada no espaço do papel (Layout), onde janelas (viewports) mostram partes do modelo em escalas definidas. Essa separação permite várias escalas na mesma folha sem nunca alterar as medidas reais do modelo.

## O que é

| Espaço | O que contém | Unidade |
|---|---|---|
| **Model (modelo)** | A geometria da peça ou do conjunto, sempre em **1:1** (mm) | mm reais |
| **Layout (papel)** | A folha (formato, quadro, legenda, notas gerais) e as **viewports** | mm de papel |
| **Viewport** | Janela no layout que mostra o modelo numa **escala** definida (1:10, 2:1...) | Escala da vista |

### Regras de ouro

1. **Desenhe sempre em 1:1 no modelo.** As medidas do arquivo são as medidas reais; cotas associativas saem corretas.
2. **A folha (legenda, quadro) fica no layout**, em escala 1:1 de papel.
3. **Cada viewport tem uma escala normalizada** (ver [[Escalas]]) e deve ser **travada** depois de ajustada, para não mudar por acidente com o zoom.
4. **Cotas:** podem ficar no modelo (anotativas) ou no layout (cotando "através" da viewport). Escolha um padrão para a equipe.
5. **Vários layouts num arquivo** podem mostrar folhas diferentes do mesmo modelo (folha 1 conjunto, folha 2 detalhes).

### Escala da viewport

Ao definir a escala 1:10 numa viewport, 100 mm do modelo aparecem como 10 mm no papel. A escala é indicada abaixo da vista ou na legenda. Ver [[Legenda]].

## Por que importa no projeto

- **Medidas reais preservadas:** nada de "desenhar já reduzido" e ter cotas erradas.
- **Várias escalas na mesma folha** (vista geral e detalhes).
- **Reaproveitamento:** a mesma geometria serve para várias folhas e para o arranjo geral.
- **Plotagem previsível:** imprimindo o layout em 1:1 no formato certo, a escala de cada vista sai correta. Ver [[Plotagem e escalas]].

## Como aplicar (passo a passo / regras práticas)

1. **Template** com layouts prontos para A0–A4 (quadro e legenda como blocos no layout).
2. **Desenhe no modelo em 1:1.**
3. **Crie viewports** num layer próprio não plotável.
4. **Ajuste a escala** de cada viewport pela lista de escalas normalizadas e **trave** a viewport.
5. **Congele layers por viewport** quando uma vista não deve mostrar certos elementos.
6. **Indique a escala** de cada vista.

## Norma relacionada

- **ABNT NBR 16752**: folhas e escalas (o layout deve reproduzi-las).

## Exemplo prático

**Situação:** folha A1 com o conjunto de um mancal: vista geral em corte (1:5) e detalhe da vedação labirinto (2:1).

1. Modelo em 1:1 com toda a geometria.
2. Layout "A1" com quadro e legenda (escala 1:5 indicada como principal, "INDICADAS" para as demais).
3. Viewport 1: corte geral em **1:5**, travada.
4. Viewport 2: detalhe da vedação em **2:1**, travada, com o título "DETALHE A — ESCALA 2:1".
5. Cotas anotativas, com as duas escalas atribuídas conforme a viewport.

> [!question] Exercício
>
> Um colega desenhou uma peça de 800 mm já reduzida a 80 mm no modelo, "para caber na folha". Que problemas isso causa?
>
> > [!success]- Resolução
> >
> > (1) **Cotas associativas** mostram 80 em vez de 800 (seria preciso sobrescrever todas, perdendo a associatividade); (2) a geometria **não pode ser reaproveitada** em montagens ou arranjos com outras peças em 1:1; (3) medições, áreas e massas extraídas do arquivo saem **erradas**; (4) qualquer pessoa que use o arquivo depois pode cometer erros graves. O correto é desenhar em 1:1 e aplicar a escala na viewport.

## Erros comuns

- **Desenhar em escala no modelo.**
- **Viewport destravada** que muda de escala com o zoom.
- **Escala da viewport fora da série** normalizada.
- **Legenda desenhada no modelo** e escalada para cada desenho.

## Ver também

- [[Plotagem e escalas]]
- [[Escalas]]
- [[Estilos de cota e texto]]
- [[10-cad/index|Índice do módulo 10]]
