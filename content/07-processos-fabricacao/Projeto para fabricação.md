---
title: Projeto para fabricação
tags: [fabricacao, metodologia]
fontes: [Boothroyd, Dewhurst e Knight Product Design for Manufacture and Assembly, Bralla Design for Manufacturability Handbook, Pahl, Beitz et al. Projeto na Engenharia (cap. de projeto para fabricação), Kalpakjian e Schmid Manufacturing Engineering and Technology]
status: rascunho
---

**Resumo:** projeto para fabricação e montagem (DFM/DFA) é um conjunto de regras práticas para desenhar peças que sejam fáceis, rápidas e baratas de fabricar, inspecionar e montar, sem perder a função. Boa parte do custo de um produto é decidida na prancheta, não na oficina.

## O que é

### Princípios gerais

1. **Simplificar:** menos peças, formas simples, menos operações.
2. **Padronizar:** materiais, chapas, perfis, parafusos, rolamentos, furos e raios comuns.
3. **Tolerância só onde a função exige.** Ver [[Tolerâncias por processo]].
4. **Pensar no processo** desde o início (usinar, soldar, fundir, dobrar).
5. **Facilitar a fixação e a medição** (superfícies de referência claras).
6. **Facilitar a montagem e a manutenção** (acesso, ordem lógica, peças que só montam de um jeito).

### Regras práticas por processo

**Usinagem**
- Raios internos compatíveis com ferramentas; cantos internos vivos só onde indispensável. Ver [[Fresamento]].
- Usinar o máximo de superfícies numa mesma fixação.
- Evitar furos profundos e estreitos, roscas cegas profundas e furos que começam em faces inclinadas.
- Ressaltos de usinagem (faces elevadas) em peças fundidas e soldadas.
- Canais de saída para rosca e rebolo.

**Soldagem e caldeiraria**
- Minimizar o volume de solda; preferir dobras a soldas. Ver [[Dobra de chapas]].
- Garantir acesso da tocha e do eletrodo; evitar soldas em espaços fechados.
- Equilibrar soldas para reduzir distorção; prever alívio de tensões antes de usinar.
- Usar espessuras e chapas comerciais; aproveitar a chapa no arranjo.

**Fundição**
- Espessuras de parede uniformes; transições suaves; raios generosos.
- Ângulos de saída para extrair o modelo.
- Sobremetal nas superfícies a usinar; referências de usinagem.

**Montagem (DFA)**
- Reduzir o número de peças e de fixadores diferentes.
- Chanfros e guias de entrada; peças simétricas ou com detalhe que impeça montagem invertida (*poka-yoke*).
- Montagem numa única direção, de preferência de cima para baixo.
- Usar componentes comerciais (catálogo) em vez de peças especiais.

**Manutenção**
- Acesso a pontos de lubrificação, ajuste e troca.
- Peças de desgaste substituíveis (aparafusadas), não soldadas.
- Olhais e pontos de içamento em peças pesadas.
- Soluções desmontáveis em mancais (caixas bipartidas, buchas de fixação).

## Por que importa no projeto

- **Cerca de 70 % do custo de fabricação** é determinado nas decisões de projeto (ordem de grandeza citada na literatura de DFM).
- **Retrabalho e não conformidades** na oficina muitas vezes são consequência de um projeto difícil de fabricar.
- **Paradas de manutenção** são mais curtas quando o projeto prevê acesso e troca fácil.

## Como aplicar (passo a passo / regras práticas)

1. **Converse com a oficina** antes de liberar o desenho: processo, máquinas, capacidade.
2. **Revise o desenho com uma lista de verificação** (raios, tolerâncias, acesso, padronização).
3. **Questione cada peça:** ela precisa existir separada? Pode ser comprada? Pode ser igual a outra já existente?
4. **Questione cada tolerância e cada acabamento:** a função exige isso?
5. **Simule a montagem e a manutenção** (no CAD 3D ou mentalmente): por onde entra cada peça, onde fica a chave, onde se apoia o equipamento de içamento.

## Norma relacionada

DFM/DFA é uma **metodologia de projeto**, apoiada na literatura (Boothroyd e Dewhurst, Bralla, Pahl e Beitz). As normas de tolerâncias (ISO 2768, ISO 13920) e de componentes padronizados são suas ferramentas.

## Exemplo prático

**Situação:** um **suporte de mancal** foi projetado como conjunto soldado de 7 chapas, com a base usinada e dois furos de chumbador.

**Revisão DFM:**

| Antes | Depois | Ganho |
|---|---|---|
| 7 chapas cortadas e soldadas | 3 peças: uma chapa dobrada em U + base + nervura | Menos solda e distorção |
| Furos dos chumbadores Ø22 H7 | Furos oblongos Ø22 × 40 (permitem alinhamento na montagem), tolerância geral | Montagem mais fácil, menos usinagem |
| Base usinada inteira | Só as faces de apoio do mancal usinadas (ressaltos) | Menos tempo de fresadora |
| Chapas de 9,5 e 11 mm | Todas de 9,5 mm (padrão do estoque) | Compras e corte mais simples |
| Sem alívio de tensões | Alívio antes da usinagem das faces | Planeza garantida |

> [!question] Exercício
>
> Cite três mudanças de projeto que facilitariam a troca rápida de um rolamento num mancal de difícil acesso.
>
> > [!success]- Resolução
> >
> > Exemplos: (1) **caixa de mancal bipartida**, que permite retirar o rolamento sem desmontar o eixo inteiro; (2) **rolamento em bucha de fixação** num eixo liso, eliminando prensa e aquecimento; (3) **acesso para ferramentas** (chave de gancho, extrator, aquecedor) e **ponto de içamento** acima do conjunto; (4) **furos de extração** roscados na tampa; (5) **referências de alinhamento** (pinos ou calços marcados) para remontar sem realinhar.

## Erros comuns

- **Projetar sem conhecer a oficina** e seus equipamentos.
- **Tolerâncias e acabamentos finos por hábito.**
- **Peças especiais onde existe componente de catálogo.**
- **Esquecer a manutenção:** peça boa de fabricar, mas impossível de trocar no campo.

## Ver também

- [[Tolerâncias por processo]]
- [[Caldeiraria]]
- [[09-metodologia-de-projeto/index|Metodologia de projeto]]
- [[07-processos-fabricacao/index|Índice do módulo 07]]
