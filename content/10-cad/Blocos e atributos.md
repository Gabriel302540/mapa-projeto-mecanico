---
title: Blocos e atributos
tags: [cad, autocad]
fontes: [Autodesk AutoCAD — documentação oficial (blocos, atributos, blocos dinâmicos), ISO 7200:2004 (campos de legenda), ISO 6433 (referências de itens)]
status: rascunho
---

**Resumo:** blocos são grupos de objetos salvos como uma unidade reutilizável — legenda, símbolos, parafusos, rolamentos, balões. Atributos são campos de texto dentro do bloco (número do desenho, revisão, material) que podem ser preenchidos e extraídos automaticamente. Blocos dinâmicos ajustam tamanho ou forma sem criar um bloco novo para cada variação.

## O que é

### Blocos

- **Definição** (comando BLOCK): guarda a geometria uma vez no arquivo.
- **Referência** (comando INSERT): cada inserção aponta para a definição. Alterar a definição atualiza todas as inserções.
- **Biblioteca:** blocos padronizados da equipe guardados em arquivos ou paletas de ferramentas.

### Atributos

- Definidos com ATTDEF (etiqueta, prompt, valor padrão), dentro do bloco.
- Preenchidos na inserção ou editados depois (EATTEDIT; gerenciador BATTMAN para alterar a definição).
- **Extração de dados** (DATAEXTRACTION): gera tabelas a partir dos atributos — por exemplo, a lista de desenhos de um projeto ou uma lista de materiais a partir de blocos de componentes.

### Blocos dinâmicos

Têm parâmetros e ações (estica, gira, escolhe entre variações de uma lista). Um único bloco "Parafuso sextavado" pode servir para vários comprimentos e diâmetros.

### Usos típicos em desenho mecânico

| Bloco | Atributos |
|---|---|
| **Legenda** | Título, número, revisão, escala, material, tolerâncias gerais, desenhista, verificador, data |
| **Quadro de revisões** | Revisão, descrição, data, responsável |
| **Balão de item** | Número do item |
| **Símbolos** | Rugosidade, soldagem, referência (datum), diedro |
| **Componentes padronizados** | Parafusos, porcas, rolamentos, retentores (com código e especificação) |

## Por que importa no projeto

- **Padronização visual** de legendas e símbolos.
- **Rapidez:** símbolos e componentes prontos.
- **Dados consistentes:** atributos permitem gerar listas de desenhos e de materiais sem digitar duas vezes.
- **Atualização em massa:** mudar o logotipo ou um campo da legenda em todos os desenhos alterando a definição do bloco.

## Como aplicar (passo a passo / regras práticas)

1. **Desenhe os blocos no layer 0** (ver [[Organização de layers]]), em escala 1:1 e com ponto de inserção lógico.
2. **Legenda com atributos** para todos os campos da [[Legenda]].
3. **Bibliotecas centralizadas** (pasta de rede ou paletas), com controle de versão.
4. **Não explodir** blocos de legenda e símbolos (perde-se a padronização e os atributos).
5. **Limpe definições não usadas** (PURGE) antes de enviar o arquivo.

## Norma relacionada

- **ISO 7200**: campos da legenda (base para os atributos).
- **ISO 6433**: referências de itens (balões).

## Exemplo prático

**Situação:** um projeto tem 60 desenhos, e o cliente pediu a lista de desenhos com número, título e revisão.

- Como as legendas são blocos com atributos, usa-se a **extração de dados** sobre a pasta do projeto, selecionando o bloco da legenda e os atributos NÚMERO, TÍTULO e REVISÃO.
- O resultado é uma tabela (no próprio desenho ou em planilha), gerada em minutos e sem erros de digitação.

> [!question] Exercício
>
> Qual a vantagem de alterar a definição de um bloco em vez de editar cada inserção?
>
> > [!success]- Resolução
> >
> > Todas as **inserções do bloco são atualizadas de uma vez**, porque elas apenas referenciam a mesma definição. Editar inserção por inserção é lento e sujeito a esquecimentos (algumas ficam diferentes).

## Erros comuns

- **Explodir blocos de legenda** e editar como texto solto.
- **Blocos com nomes genéricos** ("Bloco1") ou duplicados com nomes diferentes.
- **Blocos desenhados em escala** diferente de 1:1.
- **Atributos digitados como texto comum** (não extraíveis).

## Ver também

- [[Organização de layers]]
- [[Legenda]]
- [[Padrão de detalhamento]]
- [[10-cad/index|Índice do módulo 10]]
