---
title: Etapas do projeto
tags: [metodologia, processo]
fontes: [Pahl, Beitz, Feldhusen e Grote Projeto na Engenharia (caps. 1 a 6), VDI 2221-1:2019, Back, Ogliari, Dias e Silva Projeto Integrado de Produtos (caps. de processo de projeto), Ullman The Mechanical Design Process]
status: rascunho
---

**Resumo:** projetar não é desenhar: é um processo que vai do entendimento do problema até a documentação para fabricar, montar e manter. As metodologias clássicas (Pahl e Beitz, VDI 2221) dividem esse processo em fases — esclarecer a tarefa, conceber, configurar e detalhar —, com decisões cada vez mais concretas e caras de mudar.

## O que é

### Fases do processo de projeto (Pahl e Beitz / VDI 2221)

| Fase | Pergunta central | Resultado |
|---|---|---|
| **1. Planejamento e esclarecimento da tarefa** | O que exatamente precisa ser resolvido? | **Lista de requisitos** (especificação). Ver [[Levantamento de requisitos]] |
| **2. Projeto conceitual** | Que princípios de solução podem atender? | **Concepções** alternativas e a escolhida. Ver [[Matriz de decisão]] |
| **3. Projeto preliminar (configuração)** | Qual a forma, o arranjo e o dimensionamento? | Leiaute, cálculos principais, escolha de componentes, materiais |
| **4. Projeto detalhado** | Como fabricar e montar cada peça? | Desenhos de detalhe e conjunto, listas de materiais, memorial, instruções. Ver [[Desenho de conjunto e de detalhe]] |

### Fases típicas em projetos industriais

Em empresas, o mesmo processo aparece com outros nomes:

1. **Estudo de viabilidade / conceitual:** alternativas, estimativa de custo e prazo.
2. **Projeto básico:** arranjo, principais dimensões, cálculos, especificações dos equipamentos comprados.
3. **Projeto executivo (detalhado):** desenhos de fabricação e montagem, listas de materiais, memoriais.
4. **Fabricação e montagem**, com acompanhamento e respostas a dúvidas da obra.
5. **Comissionamento:** testes, ajustes e partida.
6. **"Como construído" (*as built*):** atualização dos desenhos com o que realmente foi feito.

### Iterações e custo das mudanças

O processo **não é linear**: descobertas no detalhamento levam a rever o conceito. Mas o **custo de uma mudança cresce muito** a cada fase: alterar uma ideia no papel custa pouco; alterar uma peça já fabricada, muito; alterar um equipamento já montado e parado na produção, muito mais.

## Por que importa no projeto

- **Pular o esclarecimento da tarefa** é a causa mais comum de projetos que resolvem o problema errado.
- **Fixar a primeira ideia** sem gerar alternativas leva a soluções piores.
- **Em manutenção e melhoria de equipamentos existentes**, a fase de esclarecimento inclui investigar a falha (ver [[Análise de modos de falha]]).

## Como aplicar (passo a passo / regras práticas)

1. Escreva a **lista de requisitos** e valide com quem pediu.
2. Gere **pelo menos duas ou três alternativas** de solução antes de escolher.
3. Escolha com critérios explícitos (matriz de decisão).
4. Faça o **leiaute** com as dimensões principais e os cálculos que definem o tamanho.
5. **Revise o conceito e o leiaute** com fabricação, montagem, manutenção e segurança antes de detalhar. Ver [[Projeto para fabricação]] e [[Segurança de máquinas]].
6. **Detalhe**, com [[Memorial de cálculo]] e [[Lista de materiais]].
7. **Libere** pelo processo de controle de desenhos. Ver [[Controle de desenhos]].

## Norma relacionada

- **VDI 2221-1:2019**: metodologia de desenvolvimento de produtos técnicos.
- Não há norma ABNT específica do processo; as referências são **livros de metodologia** (Pahl e Beitz, Back et al., Ullman).

## Exemplo prático

**Situação:** a equipe recebe o pedido "aumentar a vida das facas de um picador, que hoje duram 3 dias".

| Fase | O que fazer |
|---|---|
| Esclarecimento | Medir o desgaste, identificar o mecanismo (abrasão por terra? impacto?), definir meta (ex.: 10 dias), restrições (troca em até 2 h, custo máximo por faca, compatível com o porta-facas atual) |
| Conceitual | Alternativas: (a) revestimento duro diferente; (b) faca com pastilhas substituíveis; (c) mudar o material base; (d) reduzir a entrada de terra no processo anterior |
| Preliminar | Escolher (a) + (d) pela matriz; definir liga, espessura, padrão de cordões; estudar a fixação |
| Detalhado | Desenho da faca, procedimento de soldagem, instrução de troca |
| Teste | Instalar parte das facas novas, medir desgaste, comparar |

> [!question] Exercício
>
> Por que é mais barato descobrir uma falha de concepção na fase conceitual do que no comissionamento?
>
> > [!success]- Resolução
> >
> > Na fase conceitual, mudar significa **refazer esboços e cálculos**. No comissionamento, a mesma mudança pode exigir **refabricar peças, desmontar o equipamento, parar a produção** e refazer a documentação. O custo cresce a cada fase porque cada decisão gera trabalho (desenhos, compras, fabricação) que depende dela.

## Erros comuns

- **Começar pelo desenho detalhado** sem conceito definido.
- **Uma única alternativa** considerada.
- **Não envolver** fabricação, montagem e manutenção antes do detalhamento.
- **Não atualizar o "como construído".**

## Ver também

- [[Levantamento de requisitos]]
- [[Matriz de decisão]]
- [[Memorial de cálculo]]
- [[09-metodologia-de-projeto/index|Índice do módulo 09]]
