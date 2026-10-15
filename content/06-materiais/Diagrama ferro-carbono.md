---
title: Diagrama ferro-carbono (visão de projeto)
tags: [materiais, metalurgia]
fontes: [Callister e Rethwisch Ciência e Engenharia de Materiais (cap. de diagramas de fases e transformações), Chiaverini Aços e Ferros Fundidos (cap. 1 e 2), Colpaert Metalografia dos Produtos Siderúrgicos Comuns, Krauss Steels — Processing, Structure and Performance]
status: rascunho
---

**Resumo:** o diagrama ferro-carbono mostra quais fases existem no aço e no ferro fundido em cada temperatura e teor de carbono, em equilíbrio. Para o projetista, ele explica por que um aço com mais carbono é mais duro, por que se aquece o aço a uma certa temperatura antes da têmpera, e qual a diferença fundamental entre aço e ferro fundido.

## O que é

### Fases e constituintes

| Nome | O que é | Propriedades |
|---|---|---|
| **Ferrita (α)** | Ferro com estrutura cúbica de corpo centrado; dissolve muito pouco carbono (máx. ≈ 0,02 %) | Mole, dúctil, magnética |
| **Austenita (γ)** | Ferro com estrutura cúbica de faces centradas; dissolve até ≈ 2,1 % de C | Existe em alta temperatura (nos aços comuns); não magnética |
| **Cementita (Fe₃C)** | Carboneto de ferro com 6,67 % de C | Muito dura e frágil |
| **Perlita** | Lamelas alternadas de ferrita e cementita, formadas a partir da austenita com ≈ 0,77 % de C | Combinação de resistência e ductilidade |
| **Martensita** | Estrutura supersaturada de carbono, formada por resfriamento rápido da austenita (têmpera); **não aparece no diagrama de equilíbrio** | Muito dura e frágil antes do revenido |

### Pontos e linhas importantes

| Ponto/linha | Valor aproximado | Significado |
|---|---|---|
| **Eutetoide** | 0,77 % C a **727 °C** | A austenita se transforma toda em perlita |
| **Linha A1** | 727 °C | Abaixo dela, não há austenita em equilíbrio |
| **Linha A3** | De 912 °C (0 % C) até 727 °C (0,77 % C) | Acima dela, aço hipoeutetoide é 100 % austenita |
| **Linha Acm** | De 727 °C (0,77 % C) até 1148 °C (2,1 % C) | Acima dela, aço hipereutetoide é 100 % austenita |
| **Limite aço/ferro fundido** | ≈ 2,1 % C | Máxima solubilidade do C na austenita |
| **Eutético** | 4,3 % C a 1148 °C | Ponto de menor temperatura de fusão; base dos ferros fundidos |

### Classificação pelo carbono

- **Aços hipoeutetoides** (< 0,77 % C): ferrita + perlita. A maioria dos aços de construção mecânica (1020, 1045, 4140).
- **Aço eutetoide** (≈ 0,77 % C): só perlita.
- **Aços hipereutetoides** (0,77 a 2,1 % C): perlita + cementita. Aços para ferramentas e rolamentos.
- **Ferros fundidos** (> 2,1 % C, normalmente 2,5 a 4 %): o excesso de carbono aparece como grafita (cinzento, nodular) ou cementita (branco). Ver [[Ferros fundidos]].

**Regra prática:** em aços recozidos, a fração de perlita cresce com o carbono, e com ela a resistência e a dureza, enquanto a ductilidade e a soldabilidade caem.

## Por que importa no projeto

- **Temperatura de tratamento térmico:** para temperar um aço hipoeutetoide, aquece-se acima de A3 (austenitização completa). Ver [[Têmpera e revenido]].
- **Soldabilidade:** quanto mais carbono, mais martensita se forma na zona afetada pelo calor, e maior o risco de trinca. Ver [[Aços estruturais]].
- **Escolha entre aço e ferro fundido:** ferro fundido é fundível em formas complexas, amortece vibração e é barato, mas é muito menos dúctil.
- **Entender falhas:** a microestrutura vista em análises metalográficas é interpretada com base nesse diagrama.

## Como aplicar (passo a passo / regras práticas)

1. Identifique o **teor de carbono** do material (pela designação: SAE 1045 → 0,45 % C).
2. Situe-o no diagrama (hipo ou hipereutetoide) e estime a microestrutura de equilíbrio.
3. Para tratamentos térmicos, use as temperaturas críticas como referência, mas confirme na ficha técnica do aço (os elementos de liga deslocam as linhas).
4. Lembre que **o diagrama é de equilíbrio**: resfriamentos rápidos produzem estruturas fora dele (bainita, martensita), estudadas nos diagramas TTT e CCT.

## Norma relacionada

O diagrama é um conhecimento de **ciência dos materiais**, não uma norma. As temperaturas de tratamento de cada aço aparecem nas normas e catálogos dos produtores. ⚠️ verificar.

## Exemplo prático

**Situação:** por que um eixo de **SAE 1020** não endurece bem na têmpera, enquanto um de **SAE 1045** endurece?

- A dureza da martensita depende do **teor de carbono**. Com 0,20 % C, a martensita formada tem dureza máxima da ordem de 45 HRC (e na prática, em peças comuns, bem menos, porque o aço carbono tem baixa temperabilidade). Com 0,45 % C, chega a cerca de 55–60 HRC na superfície. ⚠️ verificar curvas de dureza da martensita × carbono.
- Por isso o 1020 é usado com **cementação** (enriquecer a superfície de carbono antes da têmpera), e o 1045 é usado em **têmpera por indução** ou beneficiamento. Ver [[Tratamentos superficiais]].

> [!question] Exercício
>
> Um aço SAE 1060 e um SAE 1020, ambos recozidos. Qual tem mais perlita? Qual é mais fácil de soldar?
>
> > [!success]- Resolução
> >
> > O **1060** (0,60 % C) tem muito mais perlita (está mais perto do eutetoide de 0,77 %), portanto é mais duro e resistente. O **1020** é muito mais fácil de soldar, porque com pouco carbono forma pouca martensita na zona afetada pelo calor e o risco de trinca é baixo.

## Erros comuns

- **Usar o diagrama para prever estruturas de têmpera** (ele é de equilíbrio).
- **Achar que mais carbono é sempre melhor**: aumenta dureza, mas reduz tenacidade e soldabilidade.
- **Ignorar o efeito dos elementos de liga** nas temperaturas críticas.

## Ver também

- [[Classificação dos aços]]
- [[Têmpera e revenido]]
- [[Ferros fundidos]]
- [[06-materiais/index|Índice do módulo 06]]
