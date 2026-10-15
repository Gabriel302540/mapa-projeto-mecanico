---
title: Têmpera e revenido
tags: [materiais, tratamento-termico]
fontes: [Chiaverini Tratamentos Térmicos das Ligas Metálicas, Callister e Rethwisch Ciência e Engenharia de Materiais (cap. de transformações de fases), Krauss Steels — Processing, Structure and Performance, ASM Handbook vol. 4 (tratamentos térmicos), ASTM A255 (ensaio Jominy)]
status: rascunho
---

**Resumo:** a têmpera aquece o aço até a austenita e o resfria rapidamente, formando martensita: muito dura, mas frágil. O revenido reaquece a peça a uma temperatura mais baixa, trocando parte da dureza por tenacidade. A combinação (beneficiamento) é o tratamento mais importante dos aços de construção mecânica.

## O que é

### Etapas

1. **Austenitização:** aquecer acima de **A3** (aços hipoeutetoides), tipicamente A3 + 30 a 50 °C, e manter o tempo necessário para a peça inteira atingir a temperatura. Para 1045 e 4140, em torno de **830 a 870 °C**. ⚠️ verificar na ficha do aço.
2. **Resfriamento rápido (têmpera)** em água, salmoura, polímero ou óleo. A austenita vira **martensita**, se o resfriamento for mais rápido que a velocidade crítica do aço.
3. **Revenido:** reaquecer abaixo de A1 (150 a 680 °C), manter e resfriar. Reduz tensões internas e fragilidade; ajusta dureza e tenacidade.

### Meios de têmpera

| Meio | Severidade | Uso | Risco |
|---|---|---|---|
| Água / salmoura | Alta | Aços carbono | Trincas e distorção |
| Polímero (solução aquosa) | Intermediária, ajustável | Aços carbono e baixa liga | Controle da concentração |
| Óleo | Moderada | Aços ligados (4140, 4340) | Menor risco de trinca |
| Ar / gás | Baixa | Aços de altíssima temperabilidade (ferramentas) | Mínima distorção |

### Temperabilidade

É a capacidade de o aço formar martensita **em profundidade**. Medida pelo **ensaio Jominy** (uma barra temperada só numa ponta; mede-se a dureza ao longo do comprimento). Elementos de liga (Cr, Mo, Ni, Mn, B) aumentam a temperabilidade.

**Efeito de massa:** em peças grossas, o núcleo resfria devagar e não vira martensita. Um aço carbono temperado em Ø150 tem praticamente só a superfície endurecida.

### Revenido: dureza × tenacidade

| Faixa de revenido | Resultado típico |
|---|---|
| 150 – 250 °C | Alívio de tensões, dureza alta mantida (ferramentas, peças de desgaste) |
| 250 – 400 °C | **Evitar** em muitos aços: fragilidade da martensita revenida |
| 450 – 550 °C | Em alguns aços ligados, risco de **fragilidade ao revenido** (resfriar rápido após o revenido ajuda) |
| 550 – 680 °C | **Beneficiamento:** resistência média-alta e boa tenacidade (eixos, engrenagens beneficiadas, 25–35 HRC) |

⚠️ verificar as faixas na ficha técnica do aço.

**Beneficiamento** = têmpera + revenido alto. É a condição de entrega mais comum de barras de 4140 e 4340 para eixos.

## Por que importa no projeto

- **Resistência à fadiga e ao desgaste** sobem muito com o beneficiamento.
- **Distorção e trincas:** peças com variações bruscas de seção, cantos vivos e furos próximos à borda trincam na têmpera. O projeto deve prever raios e seções uniformes.
- **Usinagem:** até cerca de 32–35 HRC, a peça ainda é usinável com ferramentas comuns. Acima, a usinagem final é feita por retificação ou com ferramentas especiais.
- **Sequência de fabricação:** desbaste → tratamento → acabamento (sobremetal para compensar distorção e eliminar a camada descarbonetada).

## Como aplicar (passo a passo / regras práticas)

1. **Escolha o aço pela temperabilidade** necessária para a seção da peça.
2. **Especifique o resultado**, não o processo: "temperado e revenido, 28–32 HRC" (ou faixa de resistência à tração). Deixe temperaturas para o tratador, salvo exigência.
3. **Indique onde medir** a dureza (superfície, núcleo, posição).
4. **Projete para o tratamento:** raios, seções uniformes, furos de alívio para gases em cavidades.
5. **Preveja sobremetal** para usinagem final após o tratamento.
6. **Exija relatório** de dureza (e, se crítico, ensaio de tração em corpo de prova do mesmo lote).

## Norma relacionada

- **ASTM A255**: ensaio Jominy de temperabilidade.
- **EN 10083**: aços para têmpera e revenido, com propriedades por faixa de diâmetro.
- **ISO 6508 / ISO 6506**: ensaios de dureza Rockwell e Brinell.

## Exemplo prático

**Situação:** especificar o material de um **pino de articulação** Ø80 × 400 mm, sujeito a flexão alternada e desgaste na região da bucha.

- **Material:** SAE 4140 (temperabilidade suficiente para Ø80 em óleo).
- **Tratamento:** beneficiado a **28–32 HRC** em toda a seção (resistência à fadiga, ainda usinável).
- **Região da bucha:** **têmpera por indução** a 50–55 HRC, camada de 2–3 mm (ver [[Tratamentos superficiais]]), seguida de retificação.
- **Desenho:** "SAE 4140 T&R 28–32 HRC; região X temperada por indução 50–55 HRC, profundidade efetiva 2–3 mm; retificar após tratamento". ⚠️ verificar valores com o fornecedor de tratamento.

> [!question] Exercício
>
> Por que uma peça temperada nunca deve ser usada sem revenido?
>
> > [!success]- Resolução
> >
> > Porque a **martensita recém-formada** é extremamente dura, **frágil** e cheia de **tensões internas** (da transformação e do resfriamento rápido). Sem revenido, a peça pode trincar sozinha horas ou dias depois (trinca retardada) ou quebrar com qualquer choque. O revenido alivia as tensões e dá tenacidade.

## Erros comuns

- **Especificar dureza alta demais** num aço sem temperabilidade para a seção.
- **Cantos vivos e variações bruscas de seção** em peças que serão temperadas.
- **Revenir na faixa de fragilização.**
- **Usinar tudo antes do tratamento** sem sobremetal (distorção).
- **Não especificar onde medir** a dureza.

## Ver também

- [[Normalização e recozimento]]
- [[Tratamentos superficiais]]
- [[Aços para construção mecânica]]
- [[06-materiais/index|Índice do módulo 06]]
