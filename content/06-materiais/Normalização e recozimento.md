---
title: Normalização e recozimento
tags: [materiais, tratamento-termico]
fontes: [Chiaverini Tratamentos Térmicos das Ligas Metálicas, ASM Handbook vol. 4 (tratamentos térmicos), AWS D1.1 e ASME Seção VIII (tratamento térmico pós-soldagem) ⚠️ verificar, Callister e Rethwisch Ciência e Engenharia de Materiais]
status: rascunho
---

**Resumo:** normalização e recozimento são tratamentos de aquecimento seguidos de resfriamento lento ou ao ar, usados para refinar e homogeneizar a estrutura, amolecer o aço para usinagem ou aliviar tensões internas de soldagem e usinagem. Não endurecem; preparam o material ou estabilizam a peça.

## O que é

| Tratamento | Temperatura típica | Resfriamento | Objetivo |
|---|---|---|---|
| **Normalização** | Acima de A3 (≈ 850–900 °C para aços médio carbono) | **Ao ar** | Refinar o grão, homogeneizar a estrutura de forjados, fundidos e laminados; melhorar a usinabilidade e a resposta à têmpera |
| **Recozimento pleno** | Acima de A3 | **No forno**, muito lento | Máxima maciez e ductilidade; aliviar o encruamento |
| **Recozimento de esferoidização** | Logo abaixo ou oscilando em torno de A1 (≈ 700 °C), longo tempo | Lento | Cementita em glóbulos: melhor usinabilidade de aços de **alto carbono** (52100, aços-ferramenta) |
| **Alívio de tensões** | Abaixo de A1, tipicamente **550–650 °C** | Lento e controlado | Reduzir tensões residuais de soldagem, usinagem pesada ou conformação, **sem mudar a microestrutura** |

⚠️ verificar temperaturas na ficha técnica do aço e no código de fabricação aplicável.

### Tratamento térmico pós-soldagem (TTPS / PWHT)

É um alívio de tensões aplicado a estruturas e vasos soldados. Reduz tensões residuais (que podem chegar perto do escoamento), diminui a dureza da zona afetada pelo calor e o risco de trincas por hidrogênio e corrosão sob tensão. Os códigos (ASME, AWS) definem quando é obrigatório (por espessura e material), a temperatura, o tempo por polegada de espessura e as taxas de aquecimento e resfriamento.

## Por que importa no projeto

- **Estabilidade dimensional:** uma base soldada usinada sem alívio de tensões pode empenar depois da usinagem, quando as tensões residuais se redistribuem.
- **Usinabilidade:** barras de aço de alto carbono chegam esferoidizadas para facilitar a usinagem.
- **Forjados e fundidos** normalizados têm estrutura mais uniforme e tenacidade melhor.
- **Vasos de pressão e peças críticas** podem exigir TTPS por código.

## Como aplicar (passo a passo / regras práticas)

1. **Estruturas soldadas que serão usinadas com precisão** (bases, carcaças, corpos de mancais soldados): especifique **alívio de tensões antes da usinagem final**.
2. **Peças forjadas:** especifique normalização (ou beneficiamento) conforme a norma do produto.
3. **Aços de alto carbono para usinar:** compre esferoidizados.
4. **Vasos e tubulações:** siga o código quanto a TTPS.
5. **Na sequência de fabricação:** soldar → aliviar tensões → usinar.

## Norma relacionada

- **ASME Seção VIII / AWS D1.1**: exigências de tratamento térmico pós-soldagem. ⚠️ verificar.
- **Fichas técnicas dos aços** e **normas de produtos forjados** (ASTM A668 e similares).

## Exemplo prático

**Situação:** a **base soldada** de um redutor (chapas de A36 de 25 a 50 mm, cerca de 3 m de comprimento) tem as faces de apoio usinadas com planeza de 0,1 mm. Após alguns dias, as faces apresentaram empeno de 0,6 mm.

- **Causa:** tensões residuais de soldagem liberadas parcialmente pela usinagem (remoção de material) e ao longo do tempo.
- **Correção de processo:** soldar → **alívio de tensões** em forno (≈ 600 °C, tempo conforme espessura, resfriamento lento) → usinagem final.
- **Desenho:** nota "Aliviar tensões após soldagem e antes da usinagem final".

> [!question] Exercício
>
> Qual a diferença essencial entre normalização e alívio de tensões quanto à temperatura e ao efeito na microestrutura?
>
> > [!success]- Resolução
> >
> > - **Normalização:** aquecimento **acima de A3** (austenitização completa) e resfriamento ao ar. A microestrutura é **refeita** (grão mais fino e uniforme).
> > - **Alívio de tensões:** aquecimento **abaixo de A1** (sem formar austenita). A microestrutura **não muda**; só as tensões residuais são reduzidas pela fluência e recuperação do material.

## Erros comuns

- **Usinar estruturas soldadas de precisão sem alívio de tensões.**
- **Confundir normalização com alívio de tensões.**
- **Aliviar tensões após a usinagem final** (a peça empena e perde as tolerâncias).
- **Aquecer acima de A1** pensando em "aliviar melhor", alterando a estrutura e a dureza.

## Ver também

- [[Têmpera e revenido]]
- [[Aços estruturais]]
- [[07-processos-fabricacao/index|Processos de fabricação]]
- [[06-materiais/index|Índice do módulo 06]]
