---
title: Organização de layers
tags: [cad, autocad]
fontes: [ISO 13567-1 e 13567-2 (organização e nomenclatura de layers em CAD), Autodesk AutoCAD — documentação oficial (gerenciador de propriedades de layers), ABNT NBR 16861:2020 (tipos e larguras de linha)]
status: rascunho
---

**Resumo:** layers (camadas) organizam os objetos de um desenho de CAD por tipo — contorno, linhas ocultas, linhas de centro, cotas, textos, hachuras. Cada layer carrega a cor, o tipo e a espessura de linha correspondentes à norma, de modo que o desenho sai certo na impressão sem ajustar objeto por objeto. Um padrão de layers da equipe é a base de desenhos consistentes.

## O que é

### Propriedades de um layer

| Propriedade | Função |
|---|---|
| **Nome** | Identifica o conteúdo (de preferência pelo padrão da equipe) |
| **Cor** | Diferencia na tela; em plotagem por tabela de cores (CTB), também define a espessura impressa |
| **Tipo de linha** | Contínua, tracejada, traço e ponto... |
| **Espessura (lineweight)** | Espessura impressa, quando a plotagem usa as espessuras do layer |
| **Plotar / não plotar** | Layers auxiliares (construção, viewports) não saem na impressão |
| **Ligado / congelado / travado** | Visibilidade e proteção contra edição |

### Exemplo de padrão para desenho mecânico

| Layer | Conteúdo | Tipo de linha | Espessura (mm) |
|---|---|---|---|
| `CONTORNO` | Arestas visíveis | Contínua | 0,50 |
| `OCULTA` | Arestas ocultas | Tracejada | 0,25 |
| `CENTRO` | Linhas de centro e simetria | Traço e ponto | 0,25 |
| `CORTE` | Planos de corte | Traço e ponto | 0,25 (extremidades largas desenhadas à parte) |
| `HACHURA` | Hachuras | Contínua | 0,18 |
| `COTA` | Cotas e linhas de chamada | Contínua | 0,25 |
| `TEXTO` | Notas e textos | Contínua | 0,35 |
| `VIZINHA` | Peças adjacentes, posições extremas | Traço e dois pontos | 0,25 |
| `FOLHA` | Quadro e legenda | Contínua | 0,70 |
| `CONSTRUCAO` | Linhas auxiliares | Contínua | — (não plotar) |
| `VIEWPORT` | Contorno das janelas de layout | Contínua | — (não plotar) |

As espessuras seguem o par 0,5/0,25 mm (ver [[Tipos de linha]]). ⚠️ adaptar ao padrão da equipe.

A **ISO 13567** propõe uma estrutura de nomes por campos (agente responsável, elemento, apresentação, status...), mais usada em arquitetura e construção; em desenho mecânico, um padrão simples e consistente costuma bastar.

### Layer "0" e DEFPOINTS

- **Layer 0:** objetos dentro de **blocos** desenhados no layer 0 assumem o layer em que o bloco é inserido. Use-o para criar blocos, não para desenhar.
- **DEFPOINTS:** criado automaticamente pelas cotas; nunca é plotado. Não desenhe nele.

## Por que importa no projeto

- **Desenhos legíveis:** contraste correto entre linhas largas e estreitas sai automaticamente.
- **Edição rápida:** desligar cotas e hachuras para trabalhar na geometria; congelar layers de outras disciplinas.
- **Padrão da equipe:** qualquer pessoa abre o desenho de outra e entende a organização.
- **Interoperabilidade:** arquivos enviados a fornecedores e clientes chegam organizados.

## Como aplicar (passo a passo / regras práticas)

1. **Crie os layers no template** (.dwt) da equipe, não desenho a desenho.
2. **Propriedades "ByLayer":** cor, tipo e espessura dos objetos devem vir do layer, nunca definidas objeto por objeto.
3. **Use o layer certo antes de desenhar** (ou mude depois com o "pincel" de propriedades).
4. **Layers auxiliares como "não plotar".**
5. **Limpe** layers vazios antes de enviar (comando PURGE).

## Norma relacionada

- **ISO 13567-1/-2**: organização e nomenclatura de layers.
- **ABNT NBR 16861**: tipos e larguras de linha que os layers devem reproduzir.

## Exemplo prático

**Situação:** um desenho recebido de fornecedor tem tudo no layer 0, com cores e espessuras definidas objeto por objeto. A impressão sai com todas as linhas iguais.

**Correção:**
1. Inserir o template da equipe (ou importar os layers com o DesignCenter).
2. Selecionar objetos por tipo (filtro rápido: tipo de linha tracejada → layer `OCULTA`; cotas → `COTA`; hachuras → `HACHURA`).
3. Ajustar as propriedades dos objetos para "ByLayer" (comando SETBYLAYER).
4. Conferir na pré-visualização de plotagem.

> [!question] Exercício
>
> Por que se recomenda desenhar os objetos de um bloco no layer 0?
>
> > [!success]- Resolução
> >
> > Porque objetos no layer 0 dentro de um bloco **herdam o layer em que o bloco é inserido**. Assim, o mesmo bloco (por exemplo, um parafuso) pode ser inserido no layer `CONTORNO` ou `VIZINHA` e assume a aparência correta em cada caso. Se os objetos internos estivessem num layer específico, manteriam sempre aquele layer.

## Erros comuns

- **Tudo no layer 0.**
- **Cores e espessuras definidas por objeto** em vez de ByLayer.
- **Desenhar no DEFPOINTS** (não sai na impressão).
- **Layers diferentes para a mesma coisa** em cada desenho da equipe.

## Ver também

- [[Tipos de linha]]
- [[Blocos e atributos]]
- [[Plotagem e escalas]]
- [[10-cad/index|Índice do módulo 10]]
