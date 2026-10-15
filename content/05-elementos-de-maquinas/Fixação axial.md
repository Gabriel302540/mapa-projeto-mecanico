---
title: Elementos de fixação axial
tags: [elementos, eixo-cubo]
fontes: [DIN 471 e DIN 472 (anéis elásticos para eixos e furos), ISO 2982-2 (porcas e arruelas de trava para rolamentos) ⚠️ verificar, Niemann Elementos de Máquinas (cap. de fixação axial), Budynas e Nisbett Elementos de Máquinas de Shigley (cap. 7), catálogos técnicos de anéis elásticos]
status: rascunho
---

**Resumo:** além de transmitir torque, as peças montadas num eixo precisam ficar paradas na direção axial. Para isso se usam ressaltos, anéis elásticos, porcas com arruelas de trava, buchas espaçadoras, colares e tampas aparafusadas no topo do eixo. Cada solução tem capacidade de carga axial e efeito diferentes sobre a resistência do eixo.

## O que é

| Elemento | Carga axial | Efeito no eixo | Uso típico |
|---|---|---|---|
| **Ressalto do eixo** | Alta | Concentrador (raio de concordância) | Encosto principal de rolamentos e engrenagens |
| **Anel elástico** (DIN 471 eixo / DIN 472 furo) | Baixa a média | **Concentrador severo** (canal, $K_t$ ≈ 5) | Posicionar peças com pouca carga axial; fixar anéis externos de rolamentos |
| **Porca de fixação + arruela de trava** (KM/MB) | Alta | Rosca e rasgo da arruela são concentradores; ficam em geral na ponta | Fixar rolamentos no eixo e em buchas de fixação |
| **Bucha espaçadora** | Alta (por compressão) | Nenhum (só encosta) | Manter distância entre duas peças, transferindo o encosto |
| **Colar com parafuso de fixação** | Baixa | Marca no eixo | Ajustes simples, protótipos |
| **Tampa de topo** (*end plate*) aparafusada na face do eixo | Alta | Furos roscados na ponta (região de momento baixo) | Fixar cubos de acoplamentos, polias e rodas na ponta do eixo |
| **Ajuste com interferência** | Média a alta (por atrito) | Concentração na borda do cubo (fretting) | Cubos e buchas permanentes |
| **Pino transversal** | Média | Furo transversal, concentrador | Casos simples e de baixa carga |

### Anéis elásticos

- Montados em **canais** com dimensões e tolerâncias normalizadas.
- Capacidade limitada pelo canal (esmagamento da borda) e pelo próprio anel (cisalhamento ou deformação).
- **Folga axial:** há sempre uma pequena folga entre o anel e a peça. Para eliminar, usam-se arruelas de compensação ou anéis de espessura selecionada.

### Porcas de fixação de rolamentos

- Porca ranhurada (KM) + arruela de trava com aba interna que entra num rasgo do eixo e abas externas que se dobram nas ranhuras da porca (MB).
- Em tamanhos grandes, placas de trava (KML/MS) ou porcas com parafuso de trava.

## Por que importa no projeto

- **Engrenagens helicoidais e cônicas** geram força axial que precisa ser levada até um rolamento fixo, por uma cadeia de encostos.
- **O canal do anel elástico** em região de momento alto pode ser a origem de uma fratura por fadiga. Ver [[Concentradores de tensão]].
- **Desmontagem no campo:** porcas e tampas de topo são mais práticas que interferências.

## Como aplicar (passo a passo / regras práticas)

1. **Desenhe o caminho da carga axial**: da engrenagem até o rolamento fixo e daí até a carcaça. Cada peça no caminho precisa de encosto adequado.
2. **Use ressaltos** para os encostos principais, com raios compatíveis com as peças. Ver [[Montagem de rolamentos]].
3. **Use anéis elásticos** só onde a carga axial for baixa e **longe das seções de momento alto**.
4. **Use porca + arruela** para fixar o anel interno do rolamento fixo.
5. **Use tampa de topo** para fixar cubos nas pontas de eixo.
6. **Verifique a capacidade** do elemento escolhido no catálogo (anéis) ou por cálculo (parafusos da tampa).

## Norma relacionada

- **DIN 471 / DIN 472**: anéis elásticos para eixos e para furos (dimensões, canais, capacidades). ⚠️ verificar a norma ISO equivalente (ISO 464 / DIN 471 harmonizações).
- **ISO 2982-2**: porcas e arruelas de trava. ⚠️ verificar.

## Exemplo prático

**Situação:** eixo intermediário de um redutor com engrenagem helicoidal gerando **6 kN de força axial**, rolamento fixo de um lado e livre do outro.

- **Engrenagem:** encosta num ressalto do eixo de um lado; do outro, uma **bucha espaçadora** leva o encosto até o anel interno do rolamento fixo.
- **Rolamento fixo:** anel interno preso por **porca KM + arruela MB**; anel externo entre um encosto da carcaça e a tampa.
- **Rolamento livre:** anel interno encostado num ressalto e travado por **anel elástico** (a carga axial nele é praticamente nula); anel externo livre no alojamento.
- A força axial de 6 kN segue: engrenagem → bucha → rolamento fixo → tampa → carcaça. Nenhum anel elástico está no caminho dessa carga.

> [!question] Exercício
>
> Por que não é boa ideia usar um anel elástico para fixar uma engrenagem helicoidal no meio de um eixo, logo ao lado do ponto de maior momento fletor?
>
> > [!success]- Resolução
> >
> > Por dois motivos: (1) o **canal do anel** tem fator de concentração de tensão muito alto (Kt ≈ 5 em flexão), e colocá-lo na seção de maior momento é o caminho mais curto para uma fratura por fadiga; (2) a **força axial** da engrenagem helicoidal pode superar a capacidade do anel. O correto é usar um ressalto e uma bucha espaçadora, levando a carga até o rolamento fixo.

## Erros comuns

- **Anel elástico no caminho de carga axial alta.**
- **Canal de anel em seção de momento alto.**
- **Esquecer de dobrar a aba da arruela de trava.**
- **Tampa de topo sem trava** (os parafusos afrouxam por vibração).

## Ver também

- [[Montagem de rolamentos]]
- [[Concentradores de tensão]]
- [[Chavetas]]
- [[05-elementos-de-maquinas/index|Índice do módulo 05]]
