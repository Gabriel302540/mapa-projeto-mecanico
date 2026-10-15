---
title: Revestimento duro contra desgaste
tags: [materiais, desgaste, soldagem]
fontes: [AWS A5.13 e A5.21 (metais de adição para revestimento) ⚠️ verificar, ASM Handbook vol. 6 (soldagem — revestimento duro) e vol. 18 (desgaste), Marques, Modenesi e Bracarense Soldagem: Fundamentos e Tecnologia (cap. de revestimentos), catálogos técnicos de consumíveis de revestimento duro]
status: rascunho
---

**Resumo:** revestimento duro (*hardfacing*) é a deposição, por soldagem, de uma camada de liga resistente ao desgaste sobre uma peça de aço comum. É muito usado em peças que sofrem abrasão e impacto — facas, martelos, rolos, chutes, caçambas. A escolha da liga depende do tipo de desgaste predominante: abrasão, impacto, atrito metal-metal, erosão ou corrosão combinada.

## O que é

### Mecanismos de desgaste

| Mecanismo | Descrição | Exemplo |
|---|---|---|
| **Abrasão de baixa tensão** | Partículas duras deslizam sobre a superfície | Chutes, calhas, transportadores de material arenoso |
| **Abrasão de alta tensão (moagem)** | Partículas esmagadas entre superfícies | Rolos de esmagamento, moinhos |
| **Impacto** | Golpes repetidos | Martelos, britadores, facas de picadores |
| **Metal-metal (adesivo)** | Deslizamento entre peças metálicas | Pinos, buchas, guias |
| **Erosão** | Partículas em fluxo | Bombas de polpa, curvas de tubulação |

Na prática, quase sempre há combinação (abrasão + impacto, abrasão + corrosão).

### Famílias de ligas

| Liga | Dureza típica | Resistência à abrasão | Resistência ao impacto | Uso |
|---|---|---|---|---|
| **Aço ao manganês austenítico** (11–14 % Mn, tipo Hadfield) | ≈ 200 HB depositado; **encrua** até ≈ 450–550 HB em serviço | Média | **Excelente** | Martelos, britadores, reconstrução de peças de manganês; camada de base |
| **Aços martensíticos (Cr-Mo)** | 40 – 60 HRC | Média | Boa | Recuperação de dimensões, rolos e roletes, metal-metal |
| **Ferros com carbonetos de cromo** (alto Cr, alto C) | 55 – 65 HRC | **Muito alta** | Baixa a média | Abrasão: chutes, facas, raspadores, rolos |
| **Ligas com carbonetos complexos** (Cr + Nb, Mo, W, V) | 60 – 70 HRC | **Excelente** | Média | Abrasão severa, inclusive em temperatura |
| **Carboneto de tungstênio** em matriz | Partículas muito duras | **Extrema** | Baixa | Ferramentas de corte de material abrasivo, bordas de facas |
| **Ligas de cobalto** (tipo Stellite) | 40 – 55 HRC | Boa | Boa | Desgaste em alta temperatura + corrosão; sedes de válvulas |

⚠️ verificar valores nos catálogos dos consumíveis.

### Particularidades

- **Trincas de alívio** (*relief checks*): os depósitos de carbonetos de cromo apresentam trincas transversais finas, que **são normais** e aliviam tensões. Não devem se propagar para o metal de base.
- **Camada de amanteigamento** (*buttering*): uma camada intermediária tenaz (aço inoxidável austenítico ou de baixa liga) entre o metal de base e a liga dura, para evitar que as trincas cheguem ao metal de base e para aceitar diluição.
- **Diluição:** a primeira camada mistura-se com o metal de base e fica menos dura; normalmente são necessárias duas ou três camadas.
- **Pré-aquecimento** do metal de base conforme seu carbono equivalente (ver [[Aços estruturais]]).
- **Usinabilidade:** ligas acima de ≈ 50 HRC só podem ser retificadas, não usinadas.

### Processos

Eletrodo revestido (manual, versátil), arame tubular (produtivo, campo e oficina), arco submerso (grandes áreas cilíndricas, automático), plasma de arco transferido — PTA (alta qualidade, baixa diluição), aspersão térmica (camadas finas sem fusão do metal de base).

## Por que importa no projeto

- **Peças de desgaste custam caro e param o equipamento.** O revestimento duro permite usar metal de base barato e tenaz, renovando só a superfície.
- **Rolos de esmagamento e moagem** costumam receber cordões de solda de revestimento duro na superfície dos frisos (com textura rugosa intencional, que aumenta a "pega" do material e reduz o desgaste), renovados periodicamente com o equipamento em operação ou parado. Ver [[Ferros fundidos]].
- **Facas e martelos** de picadores e desfibradores recebem ligas de alta abrasão nas bordas e base tenaz.
- **Projeto para recuperação:** prever sobremetal, acesso para soldagem e referências de medição para restaurar o perfil.

## Como aplicar (passo a passo / regras práticas)

1. **Identifique o mecanismo de desgaste** dominante (observe a peça gasta: riscos, amassamento, lascamento).
2. **Escolha a família de liga**: impacto → manganês; abrasão → carbonetos de cromo/complexos; combinação → camada de base tenaz + cobertura dura.
3. **Verifique a compatibilidade com o metal de base** (pré-aquecimento, amanteigamento).
4. **Defina espessura total e número de camadas**, e o padrão dos cordões (contínuo, em espinha, em pontos), conforme o fluxo do material.
5. **Especifique no desenho ou procedimento**: consumível (classificação AWS ou do fabricante), dureza esperada, espessura, padrão e pré-aquecimento.

## Norma relacionada

- **AWS A5.13** (eletrodos para revestimento) e **AWS A5.21** (arames e varetas para revestimento). ⚠️ verificar.
- **EN 14700**: consumíveis para revestimento duro (classificação europeia). ⚠️ verificar.
- Os **catálogos dos fabricantes** de consumíveis são a principal referência prática.

## Exemplo prático

**Situação:** a borda de uma **faca de picador** (corte de material vegetal fibroso com terra e areia) desgasta em poucos dias.

- **Mecanismo:** abrasão severa (areia) + impacto moderado.
- **Solução:** faca de aço de médio carbono ou baixa liga (base tenaz), com **revestimento de carbonetos de cromo ou complexos** na borda, em duas camadas, sobre **amanteigamento** austenítico; pré-aquecimento conforme o CE do metal de base.
- **Resultado esperado:** borda dura e resistente à abrasão, com núcleo capaz de absorver os impactos sem quebrar.

> [!question] Exercício
>
> Um martelo de britador sofre impactos fortes e abrasão moderada. Um técnico propõe revestir com carbonetos de cromo (60 HRC) diretamente. Qual o problema e o que você sugere?
>
> > [!success]- Resolução
> >
> > Ligas de **carbonetos de cromo** são frágeis ao **impacto forte**: o revestimento tende a lascar e destacar. Para impacto dominante, a melhor base é o **aço ao manganês austenítico**, que é tenaz e encrua em serviço. Se a abrasão também for relevante, pode-se usar manganês como camada principal e uma cobertura fina de liga dura só nas regiões de maior abrasão, ou ligas martensíticas tenazes.

## Erros comuns

- **Escolher a liga mais dura** para todo tipo de desgaste.
- **Soldar liga dura diretamente** sobre aço de alto carbono sem pré-aquecimento ou amanteigamento.
- **Considerar trincas de alívio como defeito** (são esperadas em carbonetos de cromo), ou o contrário: ignorar trincas que avançam para o metal de base.
- **Muitas camadas de liga frágil**, que destacam em bloco.

## Ver também

- [[Tratamentos superficiais]]
- [[Ferros fundidos]]
- [[Aços estruturais]]
- [[07-processos-fabricacao/index|Processos de fabricação]]
- [[06-materiais/index|Índice do módulo 06]]
