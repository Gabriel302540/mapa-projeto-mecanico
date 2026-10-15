---
title: Levantamento de requisitos
tags: [metodologia, requisitos]
fontes: [Pahl, Beitz, Feldhusen e Grote Projeto na Engenharia (cap. de esclarecimento da tarefa — lista de requisitos), Back, Ogliari, Dias e Silva Projeto Integrado de Produtos (cap. de especificações de projeto), Ullman The Mechanical Design Process (cap. de entendimento do problema)]
status: rascunho
---

**Resumo:** a lista de requisitos traduz o pedido ("preciso de um transportador maior") em especificações mensuráveis: capacidade, dimensões, cargas, ambiente, segurança, manutenção, custo e prazo. Cada requisito é classificado como obrigatório (exigência) ou desejável, e é o critério contra o qual o projeto será avaliado.

## O que é

### Exigências × desejos

- **Exigência (E):** precisa ser atendida; uma solução que não atende é descartada. Ex.: "capacidade mínima de 300 t/h".
- **Desejo (D):** melhora a solução, mas pode ser negociado. Ex.: "troca da correia em menos de 4 h".

### Lista de verificação (categorias)

| Categoria | Perguntas típicas |
|---|---|
| **Função** | O que deve fazer? Capacidade, velocidade, curso, precisão |
| **Geometria** | Espaço disponível, interfaces, alturas, acessos |
| **Cargas e cinemática** | Forças, torques, rotações, choques, ciclos |
| **Energia** | Potência disponível, tensão elétrica, pneumática, hidráulica |
| **Material processado** | Tipo, granulometria, umidade, abrasividade, temperatura, corrosividade |
| **Ambiente** | Temperatura, poeira, água, intempérie, atmosfera explosiva |
| **Segurança** | NR-12, NR-10, proteções, acesso, ruído. Ver [[Segurança de máquinas]] |
| **Fabricação e montagem** | Recursos disponíveis, transporte, içamento, montagem em campo |
| **Operação e manutenção** | Horas de operação, períodos de parada, sobressalentes, padronização |
| **Normas e legislação** | Normas técnicas, NRs, exigências do cliente |
| **Custo e prazo** | Orçamento, data de parada ou de partida |

### Requisito bem escrito

- **Mensurável:** "nível de ruído ≤ 85 dB(A) a 1 m", e não "silencioso".
- **Com origem:** quem pediu ou de onde veio (norma, cliente, operação).
- **Sem solução embutida:** "transmitir 50 kW a 25 rpm", e não "usar um redutor de 3 estágios".

## Por que importa no projeto

- **Requisitos vagos geram projetos discutíveis**: não há critério objetivo para aceitar ou rejeitar.
- **Requisitos esquecidos** (ambiente, manutenção, transporte) aparecem tarde e caro.
- **Em equipamentos que operam em regime sazonal** (períodos de operação contínua intercalados com paradas programadas), o prazo de fabricação e montagem e o tempo de troca de componentes costumam ser requisitos decisivos.

## Como aplicar (passo a passo / regras práticas)

1. **Entreviste** quem pediu, quem opera e quem mantém.
2. **Visite o local:** meça espaços, observe o ambiente e as interfaces.
3. **Use a lista de verificação** para não esquecer categorias.
4. **Escreva os requisitos** com valores, unidades, classificação (E/D) e origem.
5. **Valide** a lista com o solicitante antes de conceber soluções.
6. **Atualize** a lista quando algo mudar, registrando a revisão.

## Norma relacionada

Não há norma obrigatória para a lista de requisitos; a estrutura vem da **literatura de metodologia** (Pahl e Beitz, Back et al.). Normas e NRs aplicáveis entram como requisitos.

## Exemplo prático

**Situação:** lista de requisitos (resumida) para um **novo acionamento de um transportador de esteira**.

| Nº | Requisito | Valor | E/D | Origem |
|---|---|---|---|---|
| 1 | Potência na saída | ≥ 45 kW | E | Cálculo do transportador |
| 2 | Rotação do tambor | 25 rpm ± 3 % | E | Velocidade da esteira |
| 3 | Operação | 24 h/dia, choques moderados | E | Operação |
| 4 | Espaço disponível | 2,5 × 1,5 m em planta | E | Leiaute existente |
| 5 | Ambiente | Poeira e respingos de água, até 45 °C | E | Visita ao local |
| 6 | Proteções | Conforme NR-12 | E | Legislação |
| 7 | Troca do redutor | ≤ 6 h | D | Manutenção |
| 8 | Redutor de modelo já usado no parque | — | D | Padronização |
| 9 | Prazo | Montagem na próxima parada programada | E | Planejamento |

> [!question] Exercício
>
> Reescreva os requisitos vagos abaixo de forma mensurável: (a) "o equipamento deve ser robusto"; (b) "deve ser fácil de manter".
>
> > [!success]- Resolução
> >
> > Exemplos:
> > (a) "Suportar choques de partida de até 2 × o torque nominal e operar 24 h/dia por 6 meses sem paradas corretivas" ou "vida L10 dos rolamentos ≥ 40 000 h".
> > (b) "Troca do rolamento do mancal em até 2 h por dois mecânicos, sem desmontar o eixo"; "pontos de lubrificação acessíveis do piso".

## Erros comuns

- **Requisitos sem valores** ("grande", "resistente", "rápido").
- **Solução embutida** no requisito.
- **Não ouvir operação e manutenção.**
- **Não validar** a lista antes de conceber.

## Ver também

- [[Etapas do projeto]]
- [[Matriz de decisão]]
- [[Segurança de máquinas]]
- [[09-metodologia-de-projeto/index|Índice do módulo 09]]
