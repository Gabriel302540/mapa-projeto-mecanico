---
title: Padrão de detalhamento
tags: [cad, padronizacao]
fontes: [ABNT NBR 16752, NBR 16861, NBR 10126 e NBR 10067 (normas de desenho), ISO 7200, ISO 128 (série), Pahl, Beitz, Feldhusen e Grote Projeto na Engenharia (cap. de documentação)]
status: rascunho
---

**Resumo:** um padrão de detalhamento é o conjunto de regras e recursos que fazem todos os desenhos da equipe saírem iguais: template com folhas e legendas, layers, estilos, blocos, notas gerais padrão e uma lista de verificação antes da liberação. Ele junta as normas de desenho técnico com as decisões próprias da equipe.

## O que é

### Componentes de um padrão

| Componente | Conteúdo |
|---|---|
| **Template (.dwt)** | Layers, estilos de texto e cota, tipos de linha, layouts com formatos A0–A4, configurações de plotagem |
| **Bibliotecas de blocos** | Legenda, quadro de revisões, símbolos (rugosidade, solda, diedro, referências), balões, componentes padronizados |
| **Notas gerais padrão** | Tolerâncias gerais, acabamento geral, cantos vivos, proteção superficial, normas de referência |
| **Regras de vistas e cotagem** | Diedro, escalas preferenciais, como cotar elementos repetitivos, uso de GD&T |
| **Regras de numeração e revisão** | Codificação de desenhos, revisões, situação (em elaboração, liberado) |
| **Lista de verificação** | Itens conferidos antes da liberação |

### Notas gerais — exemplo

1. Desenho conforme ABNT NBR 16752 / NBR 10126; 1º diedro.
2. Cotas em milímetros.
3. Tolerâncias gerais: ISO 2768-m (usinados) / ISO 13920-BF (soldados). ⚠️ verificar classes adotadas.
4. Rugosidade geral Ra 6,3, exceto onde indicado.
5. Quebrar cantos vivos 0,5 × 45°.
6. Raios não cotados R2.
7. Superfícies não usinadas: jatear e pintar conforme especificação.

### Lista de verificação antes da liberação

- [ ] Legenda completa (número, título, material, tratamento, escala, diedro, revisão, responsáveis)
- [ ] Vistas suficientes e necessárias; cortes indicados
- [ ] Todas as cotas necessárias para fabricar, sem duplicidade e sem cadeias fechadas
- [ ] Tolerâncias e ajustes nas cotas funcionais; tolerância geral declarada
- [ ] GD&T coerente com a montagem (referências)
- [ ] Rugosidades nas superfícies funcionais; indicação geral
- [ ] Soldas indicadas com simbologia
- [ ] Notas gerais aplicáveis
- [ ] Coerência com o conjunto e a lista de materiais
- [ ] Revisão e quadro de revisões atualizados

## Por que importa no projeto

- **Qualidade uniforme**, independentemente de quem desenhou.
- **Menos erros** na fabricação (a oficina sabe onde procurar cada informação).
- **Menos tempo** de detalhamento (recursos prontos).
- **Integração de novas pessoas** na equipe.

## Como aplicar (passo a passo / regras práticas)

1. **Documente o padrão** (um guia curto, com exemplos).
2. **Coloque tudo no template e nas bibliotecas**, para que o padrão seja o caminho mais fácil.
3. **Use a lista de verificação** em toda liberação, e a revisão por outra pessoa.
4. **Revise o padrão** periodicamente com base nos erros encontrados na oficina.

## Norma relacionada

- **ABNT NBR 16752, NBR 16861, NBR 10126, NBR 10067** e **ISO 128**: a base normativa que o padrão aplica.
- **ISO 7200**: campos da legenda.

## Exemplo prático

**Situação:** a oficina reclamou de três problemas recorrentes: desenhos sem tolerância geral, rugosidade indicada de formas diferentes e legendas com campos vazios.

**Medidas:**
1. Nota de tolerância geral incluída como **bloco padrão** no template (não precisa lembrar de escrever).
2. Bloco de símbolo de rugosidade com atributos, em uma única forma.
3. Atributos obrigatórios na legenda, conferidos pela extração de dados antes da liberação (campos vazios aparecem na tabela).
4. Lista de verificação anexada ao fluxo de aprovação.

> [!question] Exercício
>
> Monte três itens de lista de verificação específicos para desenhos de peças soldadas.
>
> > [!success]- Resolução
> >
> > Exemplos: (1) todas as soldas indicadas com **símbolo, dimensão e lado** corretos (sistema AWS ou ISO declarado); (2) **tolerâncias gerais de construção soldada** (ISO 13920) declaradas; (3) **sequência** solda → alívio de tensões → usinagem indicada quando houver usinagem posterior; (4) **materiais** das chapas com norma e espessura; (5) **chanfros** cotados ou referenciados à EPS.

## Erros comuns

- **Padrão só no papel**, sem template e bibliotecas que o apliquem.
- **Exceções demais** permitidas.
- **Lista de verificação ignorada** na pressa.
- **Padrão desatualizado** em relação às normas (ex.: margens antigas da NBR 10068).

## Ver também

- [[Organização de layers]]
- [[Blocos e atributos]]
- [[Controle de desenhos]]
- [[10-cad/index|Índice do módulo 10]]
