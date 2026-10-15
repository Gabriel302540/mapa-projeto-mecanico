---
title: Aços para construção mecânica
tags: [materiais, acos]
fontes: [Budynas e Nisbett Elementos de Máquinas de Shigley (apêndice de propriedades de materiais), Chiaverini Aços e Ferros Fundidos (cap. de aços para construção mecânica), EN 10083-2 e EN 10083-3 (aços para beneficiamento), ASM Handbook vol. 1, catálogos técnicos de produtores de aço]
status: rascunho
---

**Resumo:** um pequeno grupo de aços cobre a maioria das peças de máquinas: 1020 (geral e cementação), 1045 (eixos e peças médias), 4140 (eixos e engrenagens beneficiados), 4340 (peças grandes e muito solicitadas), 8620 (engrenagens cementadas) e 52100 (rolamentos). Esta nota compara suas propriedades típicas, tratamentos e aplicações.

## O que é

### Propriedades típicas

| Aço | Condição | $S_{ut}$ (MPa) | $S_y$ (MPa) | Dureza típica |
|---|---|---|---|---|
| **1020** | Laminado a quente | 380 | 210 | ≈ 110 HB |
| **1020** | Trefilado a frio | 470 | 390 | ≈ 130 HB |
| **1045** | Laminado a quente | 570 | 310 | ≈ 165 HB |
| **1045** | Trefilado a frio | 630 | 530 | ≈ 180 HB |
| **4140** | Beneficiado (revenido alto) | ≈ 900 – 1100 | ≈ 650 – 900 | ≈ 28 – 34 HRC |
| **4340** | Beneficiado (revenido alto) | ≈ 1000 – 1200 | ≈ 850 – 1000 | ≈ 30 – 38 HRC |
| **8620** | Cementado e temperado | Núcleo ≈ 800 – 1100 | — | Superfície 58 – 62 HRC |

Valores **típicos**, da ordem dos tabelados em Shigley e catálogos; as propriedades reais dependem da bitola e do tratamento. ⚠️ verificar no certificado do material e na norma.

### Guia de aplicação

| Aço | Pontos fortes | Limitações | Aplicações |
|---|---|---|---|
| **1020** | Barato, soldável, usinável | Baixa resistência; não endurece bem na têmpera | Peças pouco solicitadas, pinos, buchas, peças cementadas simples |
| **1045** | Resistência média, endurece por indução | Temperabilidade baixa (só a superfície endurece em seções grossas); soldagem exige cuidado | Eixos médios, pinos, engrenagens pouco solicitadas, peças temperadas por indução |
| **4140** | Boa temperabilidade, resistência alta após beneficiamento | Mais caro; soldagem exige procedimento | **Eixos de transmissão**, engrenagens, parafusos especiais, pinos de alta carga |
| **4340** | Alta temperabilidade e tenacidade, até em seções grandes | Caro | Eixos grandes e muito solicitados, peças sujeitas a choque |
| **8620** | Núcleo tenaz + superfície muito dura após cementação | Exige cementação controlada; distorção | **Engrenagens**, pinhões, eixos estriados |
| **52100** | Altíssima dureza e resistência à fadiga de contato | Frágil em seções grandes; usado temperado | Rolamentos, buchas de alta dureza |

### Temperabilidade e efeito de massa

**Temperabilidade** é a capacidade de formar martensita em profundidade. Aços carbono (1045) só temperam uma camada superficial em seções grossas; aços ligados (4140, 4340) temperam até o núcleo em diâmetros maiores. Por isso, **um eixo de Ø200 de 1045 "temperado" tem núcleo praticamente sem melhoria**, enquanto um de 4340 fica beneficiado em toda a seção. Ver [[Têmpera e revenido]].

## Por que importa no projeto

- **Eixos de transmissão grandes** costumam ser de 4140 ou 4340 beneficiados, para resistir à fadiga com dimensões razoáveis.
- **Peças de reposição:** substituir 4140 beneficiado por 1045 "porque é parecido" pode reduzir pela metade o limite de fadiga.
- **Custo:** 1045 e 1020 são os mais baratos e disponíveis; o salto de custo para 4140 costuma se pagar em eixos críticos.

## Como aplicar (passo a passo / regras práticas)

1. **Peça pouco solicitada, soldável:** 1020.
2. **Eixo médio, carga moderada:** 1045 (normalizado ou trefilado), temperado por indução nos assentos se houver desgaste.
3. **Eixo de transmissão com fadiga e choque:** 4140 beneficiado (28–32 HRC é uma faixa comum, que ainda permite usinagem).
4. **Eixo grande (> 200 mm) e muito solicitado:** 4340 beneficiado.
5. **Engrenagem com alta carga de contato:** 8620 cementado e temperado (ou 4140 temperado por indução/nitretado).
6. **Especifique sempre** material + condição + dureza no desenho.

## Norma relacionada

- **SAE J404 / NBR NM 87**: composição. Ver [[Classificação dos aços]].
- **EN 10083-2/-3**: aços para beneficiamento (C45, 42CrMo4, 34CrNiMo6), com propriedades por faixa de diâmetro.
- **EN 10084**: aços para cementação.

## Exemplo prático

**Situação:** comparar o limite de fadiga corrigido de um eixo de Ø90 usinado, em **1045 trefilado** ($S_{ut}$ = 630 MPa) e em **4140 beneficiado** ($S_{ut}$ ≈ 950 MPa ⚠️), com os mesmos fatores de tamanho (0,745) e confiabilidade (0,868).

| | 1045 | 4140 |
|---|---|---|
| $S_e' = 0{,}5\,S_{ut}$ | 315 | 475 |
| $k_a = 4{,}51\,S_{ut}^{-0{,}265}$ | 0,82 | 0,74 |
| $S_e$ | ≈ 167 MPa | ≈ 227 MPa |

O 4140 dá cerca de **36 % mais limite de fadiga**, o que, pela fórmula de Goodman, permite reduzir o diâmetro em cerca de 10 % para o mesmo coeficiente de segurança, ou aumentar bastante a margem. Repare que o ganho é menor que a razão das resistências (950/630 = 1,5), porque o fator de superfície penaliza mais o aço mais resistente. Ver [[Fadiga de eixos]].

> [!question] Exercício
>
> Por que se usa 8620 cementado, e não 4140 temperado por completo, para engrenagens muito carregadas?
>
> > [!success]- Resolução
> >
> > Porque a engrenagem precisa de **superfície muito dura** (58–62 HRC) para resistir ao pitting e ao desgaste, **e núcleo tenaz** para resistir à flexão e a choques no pé do dente. O 8620 tem pouco carbono (núcleo tenaz) e a cementação enriquece só a camada superficial, que fica muito dura após a têmpera. Um 4140 temperado por completo até 60 HRC ficaria frágil demais no núcleo.

## Erros comuns

- **Especificar "aço 1045 temperado"** para eixos grossos, esperando dureza no núcleo.
- **Usar 4140 recozido** (mole) achando que é o 4140 beneficiado.
- **Soldar 4140 ou 4340** sem procedimento qualificado.
- **Esquecer que o fator de superfície** penaliza mais os aços de alta resistência.

## Ver também

- [[Classificação dos aços]]
- [[Têmpera e revenido]]
- [[Tratamentos superficiais]]
- [[Fadiga de eixos]]
- [[06-materiais/index|Índice do módulo 06]]
