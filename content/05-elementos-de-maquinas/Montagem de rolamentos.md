---
title: "Rolamentos: montagem e fixação"
tags: [elementos, rolamentos, manutencao]
fontes: [Catálogos técnicos gerais de rolamentos (seções de montagem, desmontagem e lubrificação), manuais de manutenção de rolamentos de fabricantes, ISO 2982-2 (porcas e arruelas de trava) ⚠️ verificar, Budynas e Nisbett Elementos de Máquinas de Shigley (cap. 11)]
status: rascunho
---

**Resumo:** grande parte das falhas prematuras de rolamentos vem da montagem: ajustes errados, golpes de martelo nos anéis, aquecimento excessivo, sujeira e fixação axial mal feita. Esta nota cobre os métodos de montagem, a fixação dos anéis, o uso de buchas de fixação e os cuidados com lubrificação e vedação.

## O que é

### Métodos de montagem

| Método | Quando usar | Cuidados |
|---|---|---|
| **Mecânico a frio** (prensa ou bucha de montagem e martelo) | Rolamentos pequenos (furo até cerca de 80 mm) com interferência leve | A força deve passar **pelo anel que está sendo ajustado**, nunca pelos corpos rolantes |
| **Térmico** (aquecedor por indução, banho de óleo, estufa) | Rolamentos médios e grandes com interferência no eixo | Temperatura típica até cerca de **110–120 °C**; nunca chama direta; rolamentos vedados exigem cuidado com a graxa e as vedações |
| **Hidráulico** (porca hidráulica, injeção de óleo) | Rolamentos grandes em eixos cônicos ou buchas | Controle do deslocamento axial ou da redução de folga |

⚠️ verificar os limites de temperatura no catálogo.

### Fixação axial

- **Anel interno:** encosto no ressalto do eixo + porca de fixação com arruela de trava, anel elástico, tampa de ponta (*end plate*) aparafusada no topo do eixo, ou bucha espaçadora. Ver [[Fixação axial]].
- **Anel externo:** encosto no alojamento + tampa, anel elástico de furo.
- **Rolamento livre:** o anel externo (ou interno, conforme o caso) fica sem encosto de um dos lados, com folga axial para a dilatação.

### Bucha de fixação (*adapter sleeve*)

Bucha cônica com rasgo, montada num **eixo liso** (h9 ou h10), que recebe um rolamento de **furo cônico** (sufixo K). A porca empurra o rolamento sobre o cone, expandindo o anel interno e prendendo-o ao eixo.

- **Vantagens:** eixo sem ressaltos (mais barato e fácil de usinar), posição axial livre, montagem e desmontagem no campo.
- **Controle do aperto:** pela **redução da folga interna radial** (medida com calibre de lâminas nos rolamentos autocompensadores de rolos) ou pelo **ângulo de giro da porca** / deslocamento axial, conforme tabelas do catálogo. Aperto insuficiente faz o anel girar na bucha; aperto excessivo elimina a folga interna e superaquece o rolamento.

### Lubrificação

- **Graxa:** a maioria das aplicações de baixa e média rotação; enchimento de cerca de 30 % a 50 % do espaço livre da caixa (excesso gera aquecimento); relubrificação periódica pelo intervalo do catálogo.
- **Óleo:** rotações altas, temperaturas altas, redutores (banho ou circulação).

## Por que importa no projeto

- **O projeto define a montagem:** chanfros de entrada, raios compatíveis com o rolamento, altura dos ressaltos (para permitir o uso de extrator), furos para injeção de óleo e roscas para porcas de desmontagem.
- **Manutenção no campo** em equipamentos grandes depende de soluções desmontáveis (bucha de fixação, caixas bipartidas).
- **Contaminação** (pó, água, bagaço, produto) é a maior inimiga: o projeto da vedação conta mais que o tamanho do rolamento.

## Como aplicar (passo a passo / regras práticas)

1. **Projete a altura dos ressaltos** para encostar o anel sem tocar na vedação, deixando espaço para o extrator.
2. **Raio do eixo menor que o raio de canto do rolamento** (ou use canal de alívio). Ver [[Concentradores de tensão]].
3. **Defina o arranjo fixo-livre** e deixe folga axial suficiente no livre.
4. **Especifique o método de montagem** e a temperatura no procedimento de manutenção.
5. **Para buchas de fixação**, informe a redução de folga ou o ângulo de aperto da porca.
6. **Defina lubrificante, quantidade e intervalo** de relubrificação.
7. **Escolha a vedação** pelo ambiente (labirinto, retentor, vedações em V, graxa como barreira).

## Norma relacionada

- **Catálogos de fabricantes**: são a referência prática para montagem, ajustes, folgas e lubrificação.
- **ISO 2982-2**: porcas de fixação e arruelas de trava para rolamentos. ⚠️ verificar.
- **ISO 113**: caixas de mancal (dimensões). ⚠️ verificar.

## Exemplo prático

**Situação:** troca de um rolamento **autocompensador de rolos com furo cônico** montado em bucha de fixação no eixo de um transportador.

1. Limpar o eixo e conferir o diâmetro e a cilindricidade na região da bucha.
2. Medir a **folga interna radial** do rolamento novo com calibre de lâminas (entre o rolo de cima e o anel externo).
3. Montar a bucha e o rolamento; apertar a porca até a **redução de folga** indicada no catálogo para aquele tamanho.
4. Conferir a folga residual (não pode ser menor que o mínimo da tabela).
5. Dobrar a aba da arruela de trava num rasgo da porca.
6. Encher a caixa com a quantidade de graxa indicada e montar as vedações.
7. No lado **livre**, deixar o anel externo com espaço axial dos dois lados.

> [!question] Exercício
>
> Por que nunca se deve montar um rolamento no eixo batendo no anel externo?
>
> > [!success]- Resolução
> >
> > Porque a força passaria do anel externo para o interno **através dos corpos rolantes**, criando marcas nas pistas (*brinelling*) logo na montagem. Essas marcas viram ponto de início de fadiga, ruído e vibração. A força de montagem deve ser aplicada no **anel que está sendo ajustado** (no eixo, o anel interno).

## Erros comuns

- **Aquecer com maçarico**, criando pontos superaquecidos e alterando a dureza.
- **Excesso de graxa** (aquecimento) ou graxas incompatíveis misturadas.
- **Bucha de fixação sem controle de aperto.**
- **Esquecer a folga axial do rolamento livre.**
- **Montar com sujeira**: um grão de areia na pista pode reduzir drasticamente a vida.

## Ver também

- [[Seleção de rolamentos]]
- [[Vida de rolamentos]]
- [[Fixação axial]]
- [[Ajustes recomendados]]
- [[05-elementos-de-maquinas/index|Índice do módulo 05]]
