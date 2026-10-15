---
title: Plotagem e escalas
tags: [cad, autocad]
fontes: [Autodesk AutoCAD — documentação oficial (plotagem, tabelas de estilo de plotagem CTB/STB, escala de tipos de linha), ISO 19005-1 (PDF/A para arquivamento) ⚠️ verificar, ABNT NBR 16752 (folhas e escalas)]
status: rascunho
---

**Resumo:** plotar é transformar o layout em papel ou PDF com as espessuras, os tipos de linha e as escalas corretos. O layout é impresso em 1:1 no formato da folha; as escalas das vistas já estão nas viewports. As espessuras vêm dos layers ou de uma tabela de estilos de plotagem, e a escala dos tipos de linha precisa estar ajustada para tracejados e traço-ponto saírem visíveis.

## O que é

### Configuração de plotagem do layout

| Item | Configuração |
|---|---|
| Impressora / plotter | Física ou "DWG to PDF" (ou equivalente) |
| Formato | Igual ao do quadro (A0 a A4) |
| Área | Layout ou janela pelos cantos do formato |
| **Escala de plotagem** | **1:1** (as escalas das vistas estão nas viewports) |
| Tabela de estilo | CTB (por cor) ou STB (por estilo nomeado), ou espessuras do layer |
| Espessuras de linha | Plotar com espessuras ativado |

### Tabelas de estilo de plotagem

- **CTB (dependente de cor):** a **cor** do objeto (ou do layer) define a espessura e a cor impressa. Ex.: cor 7 → 0,5 mm preto; cor 1 → 0,25 mm preto. Comum em escritórios antigos.
- **STB (estilos nomeados):** cada layer tem um estilo de plotagem com nome.
- **Espessuras do layer** (sem tabela que as sobrescreva): mais direto, combina com o padrão de layers da norma.

O importante é **um padrão único na equipe**, guardado com o template.

### Escala de tipos de linha

Tracejados e traço-ponto são definidos por padrões de comprimento. Se a escala estiver errada, a linha sai contínua (padrão grande demais) ou como um borrão (pequeno demais).

- **LTSCALE:** escala global.
- **PSLTSCALE = 1:** no layout, os padrões são escalados pela escala de cada viewport, saindo iguais no papel em todas as vistas.
- **MSLTSCALE = 1:** no modelo, usa a escala anotativa.

### PDF para circulação e arquivamento

- **PDF** é o formato usual para enviar desenhos para fabricação e aprovação (não editável).
- **PDF/A** é uma variante própria para **arquivamento de longo prazo** (fontes embutidas, sem dependências externas). ⚠️ verificar a exigência da empresa.

## Por que importa no projeto

- **A escala da vista impressa deve ser a escala escrita.** Uma impressão "ajustada à página" invalida a escala. Ver [[Formatos de folha]].
- **Contraste de linhas** correto depende da configuração de plotagem.
- **Cópias reduzidas** (A1 impresso em A3) exigem textos de altura suficiente. Ver [[Caligrafia técnica]].

## Como aplicar (passo a passo / regras práticas)

1. **Salve a configuração de plotagem** no template (*page setup*), para cada formato.
2. **Plote o layout em 1:1** no formato da folha.
3. **Ative PSLTSCALE** e ajuste LTSCALE (normalmente 1 em desenhos em mm com layout em mm). ⚠️ conferir com os tipos de linha usados (ISO ou acad).
4. **Pré-visualize** antes de plotar.
5. **Em cópias reduzidas,** carimbe "cópia reduzida — não medir".
6. **Gere PDF** com o nome do arquivo seguindo o padrão (número e revisão). Ver [[Nomenclatura de arquivos]].

## Norma relacionada

- **ABNT NBR 16752**: folhas e escalas.
- **ISO 19005**: PDF/A. ⚠️ verificar.

## Exemplo prático

**Situação:** um desenho A2 impresso sai com todas as linhas de centro **contínuas** na vista em 1:10 e corretas no detalhe em 2:1.

- **Causa:** PSLTSCALE desligado; o padrão traço-ponto está sendo dimensionado pela escala do modelo, e na viewport de 1:10 ele fica 10 vezes menor que o necessário — os traços se "fundem".
- **Correção:** PSLTSCALE = 1, regenerar as viewports (REGENALL) e conferir na pré-visualização.

> [!question] Exercício
>
> Por que o layout deve ser plotado em escala 1:1, mesmo que as vistas estejam em 1:5 e 1:10?
>
> > [!success]- Resolução
> >
> > Porque o **layout já está em tamanho de papel** (a folha A1 no layout tem 841 × 594 mm), e as escalas das vistas já foram aplicadas nas **viewports**. Plotar o layout em outra escala reduziria ou ampliaria tudo de novo, e as vistas deixariam de estar nas escalas indicadas.

## Erros comuns

- **Plotar "ajustado à página"** sem avisar.
- **Tabela de estilo diferente** da usada pela equipe (espessuras erradas).
- **PSLTSCALE desligado** com viewports de escalas diferentes.
- **PDF sem fontes embutidas** para arquivamento.

## Ver também

- [[Model e layout]]
- [[Organização de layers]]
- [[Escalas]]
- [[10-cad/index|Índice do módulo 10]]
